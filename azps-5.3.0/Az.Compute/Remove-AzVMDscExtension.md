---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473003"
---
# <span data-ttu-id="ec111-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec111-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="ec111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec111-102">SYNOPSIS</span></span>
<span data-ttu-id="ec111-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec111-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ec111-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec111-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec111-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec111-105">DESCRIPTION</span></span>
<span data-ttu-id="ec111-106">Das **Cmdlet "Remove-AzVMDscExtension"** entfernt einen Erweiterungshandler für die Gewünschte Zustandskonfiguration (Desired State Configuration, DSC) von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec111-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="ec111-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec111-107">EXAMPLES</span></span>

### <span data-ttu-id="ec111-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ec111-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ec111-109">Mit diesem Befehl wird die Erweiterung DSC auf dem virtuellen Computer VM07 entfernt.</span><span class="sxs-lookup"><span data-stu-id="ec111-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="ec111-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec111-110">PARAMETERS</span></span>

### <span data-ttu-id="ec111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec111-111">-DefaultProfile</span></span>
<span data-ttu-id="ec111-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec111-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ec111-113">-Name</span></span>
<span data-ttu-id="ec111-114">Gibt den Namen der DSC-Erweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ec111-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="ec111-115">Das Set-AzVMDscExtension-Cmdlet legt diesen Namen auf "Microsoft.Powershell.DSC" fest. Dies ist der Standardwert, der von **"Remove-AzVMDscExtension" verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="ec111-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec111-116">-NoWait</span></span>
<span data-ttu-id="ec111-117">Startet den Vorgang und kehrt unmittelbar vor Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="ec111-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ec111-118">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ec111-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec111-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec111-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="ec111-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ec111-121">-VMName</span></span>
<span data-ttu-id="ec111-122">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die ERWEITERUNG DSC entfernt.</span><span class="sxs-lookup"><span data-stu-id="ec111-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec111-123">-Confirm</span></span>
<span data-ttu-id="ec111-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec111-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ec111-125">-WhatIf</span></span>
<span data-ttu-id="ec111-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec111-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec111-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec111-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec111-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec111-128">CommonParameters</span></span>
<span data-ttu-id="ec111-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec111-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec111-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec111-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec111-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec111-131">INPUTS</span></span>

### <span data-ttu-id="ec111-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ec111-132">System.String</span></span>

## <span data-ttu-id="ec111-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec111-133">OUTPUTS</span></span>

### <span data-ttu-id="ec111-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ec111-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ec111-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ec111-135">NOTES</span></span>

## <span data-ttu-id="ec111-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ec111-136">RELATED LINKS</span></span>

[<span data-ttu-id="ec111-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec111-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="ec111-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec111-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


