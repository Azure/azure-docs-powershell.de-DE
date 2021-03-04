---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 30b3ee76a538b4db69e79397bff65e723a9bf908
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946234"
---
# <span data-ttu-id="f9f82-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f9f82-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="f9f82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f82-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f82-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9f82-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="f9f82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9f82-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f82-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9f82-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f82-106">Das **Cmdlet Remove-AzVMDscExtension** entfernt einen Dsc-Erweiterungshandler (Desired State Configuration) von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9f82-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="f9f82-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f9f82-107">EXAMPLES</span></span>

### <span data-ttu-id="f9f82-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="f9f82-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="f9f82-109">Mit diesem Befehl wird die Erweiterung DSC auf dem virtuellen Computer mit dem Namen VM07 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9f82-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="f9f82-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9f82-110">PARAMETERS</span></span>

### <span data-ttu-id="f9f82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f82-111">-DefaultProfile</span></span>
<span data-ttu-id="f9f82-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9f82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9f82-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f9f82-113">-Name</span></span>
<span data-ttu-id="f9f82-114">Gibt den Namen der DSC-Erweiterung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f9f82-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="f9f82-115">Das Set-AzVMDscExtension-Cmdlet legt diesen Namen auf Microsoft.Powershell.DSC fest. Dies ist der Standardwert, der von **Remove-AzVMDscExtension verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="f9f82-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="f9f82-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f9f82-116">-NoWait</span></span>
<span data-ttu-id="f9f82-117">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f9f82-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f9f82-118">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f9f82-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f9f82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f82-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9f82-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f9f82-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f9f82-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9f82-121">-VMName</span></span>
<span data-ttu-id="f9f82-122">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9f82-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="f9f82-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9f82-123">-Confirm</span></span>
<span data-ttu-id="f9f82-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9f82-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f82-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f82-125">-WhatIf</span></span>
<span data-ttu-id="f9f82-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9f82-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f82-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9f82-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f82-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f82-128">CommonParameters</span></span>
<span data-ttu-id="f9f82-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9f82-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f82-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9f82-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f82-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f9f82-131">INPUTS</span></span>

### <span data-ttu-id="f9f82-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9f82-132">System.String</span></span>

## <span data-ttu-id="f9f82-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f9f82-133">OUTPUTS</span></span>

### <span data-ttu-id="f9f82-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9f82-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f9f82-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f9f82-135">NOTES</span></span>

## <span data-ttu-id="f9f82-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f9f82-136">RELATED LINKS</span></span>

[<span data-ttu-id="f9f82-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f9f82-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="f9f82-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f9f82-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


