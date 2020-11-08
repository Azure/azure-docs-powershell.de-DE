---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003879"
---
# <span data-ttu-id="71e19-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71e19-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="71e19-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71e19-102">SYNOPSIS</span></span>
<span data-ttu-id="71e19-103">Entfernt einen DSC-Erweiterungshandler von einem virtuellen Computer in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71e19-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="71e19-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71e19-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71e19-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71e19-105">DESCRIPTION</span></span>
<span data-ttu-id="71e19-106">Mit dem Cmdlet **Remove-AzVMDscExtension** wird der Erweiterungshandler für die gewünschte Zustands Konfiguration (DSC) von einem virtuellen Computer in einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="71e19-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="71e19-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71e19-107">EXAMPLES</span></span>

### <span data-ttu-id="71e19-108">Beispiel 1: Entfernen einer DSC-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="71e19-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="71e19-109">Dieser Befehl entfernt die Erweiterung mit dem Namen DSC auf dem virtuellen Computer mit dem Namen VM07.</span><span class="sxs-lookup"><span data-stu-id="71e19-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="71e19-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="71e19-110">PARAMETERS</span></span>

### <span data-ttu-id="71e19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e19-111">-DefaultProfile</span></span>
<span data-ttu-id="71e19-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71e19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71e19-113">-Name</span><span class="sxs-lookup"><span data-stu-id="71e19-113">-Name</span></span>
<span data-ttu-id="71e19-114">Gibt den Namen der DSC-Erweiterung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="71e19-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="71e19-115">Mit dem Set-AzVMDscExtension-Cmdlet wird dieser Name auf Microsoft. PowerShell. DSC festgelegt, bei dem es sich um den Standardwert handelt, der von **Remove-AzVMDscExtension** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71e19-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="71e19-116">-Nowait</span><span class="sxs-lookup"><span data-stu-id="71e19-116">-NoWait</span></span>
<span data-ttu-id="71e19-117">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="71e19-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="71e19-118">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="71e19-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="71e19-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e19-119">-ResourceGroupName</span></span>
<span data-ttu-id="71e19-120">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="71e19-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="71e19-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="71e19-121">-VMName</span></span>
<span data-ttu-id="71e19-122">Gibt den Namen eines virtuellen Computers an, von dem dieses Cmdlet die DSC-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="71e19-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="71e19-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71e19-123">-Confirm</span></span>
<span data-ttu-id="71e19-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71e19-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e19-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e19-125">-WhatIf</span></span>
<span data-ttu-id="71e19-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71e19-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e19-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71e19-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e19-128">CommonParameters</span></span>
<span data-ttu-id="71e19-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e19-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71e19-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e19-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71e19-131">INPUTS</span></span>

### <span data-ttu-id="71e19-132">System. String</span><span class="sxs-lookup"><span data-stu-id="71e19-132">System.String</span></span>

## <span data-ttu-id="71e19-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71e19-133">OUTPUTS</span></span>

### <span data-ttu-id="71e19-134">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71e19-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="71e19-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="71e19-135">NOTES</span></span>

## <span data-ttu-id="71e19-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71e19-136">RELATED LINKS</span></span>

[<span data-ttu-id="71e19-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71e19-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="71e19-138">Satz-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="71e19-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


