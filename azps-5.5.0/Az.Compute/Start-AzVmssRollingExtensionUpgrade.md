---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167852"
---
# <span data-ttu-id="4ee53-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="4ee53-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="4ee53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee53-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee53-103">Dieses Cmdlet startet ein rolliertes Upgrade für alle Erweiterungen des angegebenen Virtual Machine Scale Set auf die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4ee53-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="4ee53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ee53-104">SYNTAX</span></span>

### <span data-ttu-id="4ee53-105">StandardParameter</span><span class="sxs-lookup"><span data-stu-id="4ee53-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee53-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ee53-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee53-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee53-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee53-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ee53-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee53-109">Startet ein fortlaufendes Upgrade, um alle Erweiterungen auf diesem Maßstab des virtuellen Computers auf die neueste verfügbare Version zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="4ee53-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="4ee53-110">Erweiterungen, auf denen bereits die neueste verfügbare Version ausgeführt wird, sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="4ee53-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="4ee53-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ee53-111">EXAMPLES</span></span>

### <span data-ttu-id="4ee53-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ee53-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="4ee53-113">In diesem Beispiel wird der vorhandene VM-Skalierungssatz "MyVmssName" bekommt und eine Erweiterung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4ee53-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="4ee53-114">Der letzte Befehl führt den Upgradeprozess für den Erweiterungsrollup aus.</span><span class="sxs-lookup"><span data-stu-id="4ee53-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="4ee53-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee53-115">PARAMETERS</span></span>

### <span data-ttu-id="4ee53-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ee53-116">-AsJob</span></span>
<span data-ttu-id="4ee53-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4ee53-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee53-118">-DefaultProfile</span></span>
<span data-ttu-id="4ee53-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ee53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee53-120">-ResourceGroupName</span></span>
<span data-ttu-id="4ee53-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4ee53-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ee53-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee53-122">-ResourceId</span></span>
<span data-ttu-id="4ee53-123">Die Ressourcen-ID des Objekts für den VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="4ee53-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="4ee53-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ee53-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4ee53-125">Das Objekt für den VM-Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="4ee53-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="4ee53-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ee53-126">-VMScaleSetName</span></span>
<span data-ttu-id="4ee53-127">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="4ee53-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="4ee53-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ee53-128">-Confirm</span></span>
<span data-ttu-id="4ee53-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ee53-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee53-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ee53-130">-WhatIf</span></span>
<span data-ttu-id="4ee53-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ee53-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee53-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ee53-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee53-133">CommonParameters</span></span>
<span data-ttu-id="4ee53-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee53-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ee53-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee53-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee53-136">INPUTS</span></span>

### <span data-ttu-id="4ee53-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4ee53-137">System.String</span></span>

### <span data-ttu-id="4ee53-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ee53-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4ee53-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee53-139">OUTPUTS</span></span>

### <span data-ttu-id="4ee53-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4ee53-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4ee53-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ee53-141">NOTES</span></span>

## <span data-ttu-id="4ee53-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ee53-142">RELATED LINKS</span></span>
