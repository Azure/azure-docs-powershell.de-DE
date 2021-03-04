---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: 2816f34c8a6148d67a5bed397e573b07fa2e7004
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936256"
---
# <span data-ttu-id="2d789-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="2d789-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="2d789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d789-102">SYNOPSIS</span></span>
<span data-ttu-id="2d789-103">Dieses Cmdlet startet ein fortlaufendes Upgrade für alle Erweiterungen des angegebenen Virtual Machine Scale Set auf die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="2d789-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="2d789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d789-104">SYNTAX</span></span>

### <span data-ttu-id="2d789-105">StandardParameter</span><span class="sxs-lookup"><span data-stu-id="2d789-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d789-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d789-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d789-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d789-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d789-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d789-108">DESCRIPTION</span></span>
<span data-ttu-id="2d789-109">Startet ein fortlaufendes Upgrade, um alle Erweiterungen auf dieser Skalierungsskala für virtuelle Computer auf die neueste verfügbare Version zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="2d789-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="2d789-110">Erweiterungen, die bereits die neueste verfügbare Version ausführen, sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2d789-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="2d789-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d789-111">EXAMPLES</span></span>

### <span data-ttu-id="2d789-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d789-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="2d789-113">Dieses Beispiel ruft den vorhandenen VM-Skalierungssatz "MyVmssName" ab und fügt eine Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d789-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="2d789-114">Mit dem endgültigen Befehl wird der Upgradevorgang für das Fortlaufende Upgrade der Erweiterung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d789-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="2d789-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d789-115">PARAMETERS</span></span>

### <span data-ttu-id="2d789-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d789-116">-AsJob</span></span>
<span data-ttu-id="2d789-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2d789-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d789-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d789-118">-DefaultProfile</span></span>
<span data-ttu-id="2d789-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d789-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d789-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d789-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d789-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2d789-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d789-122">-ResourceId</span></span>
<span data-ttu-id="2d789-123">Die Ressourcen-ID des VM-Skalierungssatzobjekts.</span><span class="sxs-lookup"><span data-stu-id="2d789-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d789-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2d789-125">Das VM-Skalierungssatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="2d789-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2d789-126">-VMScaleSetName</span></span>
<span data-ttu-id="2d789-127">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="2d789-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d789-128">-Confirm</span></span>
<span data-ttu-id="2d789-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d789-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d789-130">-WhatIf</span></span>
<span data-ttu-id="2d789-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d789-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d789-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d789-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d789-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d789-133">CommonParameters</span></span>
<span data-ttu-id="2d789-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d789-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d789-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d789-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d789-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d789-136">INPUTS</span></span>

### <span data-ttu-id="2d789-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2d789-137">System.String</span></span>

### <span data-ttu-id="2d789-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2d789-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2d789-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d789-139">OUTPUTS</span></span>

### <span data-ttu-id="2d789-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2d789-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2d789-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d789-141">NOTES</span></span>

## <span data-ttu-id="2d789-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d789-142">RELATED LINKS</span></span>
