---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: 43e92594d8a67dbb3ade0b66a065b8c6c097d60d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307992"
---
# <span data-ttu-id="71a17-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="71a17-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="71a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71a17-102">SYNOPSIS</span></span>
<span data-ttu-id="71a17-103">Walk to update domain walk to update virtual machines in a service fabric virtual machine scale set.</span><span class="sxs-lookup"><span data-stu-id="71a17-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="71a17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71a17-104">SYNTAX</span></span>

### <span data-ttu-id="71a17-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="71a17-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71a17-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="71a17-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a17-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="71a17-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a17-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71a17-108">DESCRIPTION</span></span>
<span data-ttu-id="71a17-109">Erzwingen Sie die Manuelle Aktualisierungsdomäne der Plattform, um virtuelle Computer in einem Service Fabric-Scale-Set für virtuelle Computer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="71a17-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="71a17-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="71a17-110">EXAMPLES</span></span>

### <span data-ttu-id="71a17-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71a17-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="71a17-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span><span class="sxs-lookup"><span data-stu-id="71a17-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="71a17-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="71a17-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="71a17-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span><span class="sxs-lookup"><span data-stu-id="71a17-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="71a17-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="71a17-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="71a17-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span><span class="sxs-lookup"><span data-stu-id="71a17-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="71a17-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71a17-117">PARAMETERS</span></span>

### <span data-ttu-id="71a17-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a17-118">-AsJob</span></span>
<span data-ttu-id="71a17-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="71a17-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71a17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a17-120">-DefaultProfile</span></span>
<span data-ttu-id="71a17-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="71a17-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a17-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="71a17-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="71a17-123">Die Domäne für plattformupdates, für die eine manuelle Wiederherstellungsanleitung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="71a17-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a17-124">-ResourceGroupName</span></span>
<span data-ttu-id="71a17-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71a17-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a17-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71a17-126">-ResourceId</span></span>
<span data-ttu-id="71a17-127">Die Ressourcen-ID für den Skalierungssatz des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="71a17-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a17-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="71a17-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="71a17-129">Objekt für den Maßstabssatz für einen lokalen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="71a17-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71a17-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="71a17-130">-VMScaleSetName</span></span>
<span data-ttu-id="71a17-131">Der Name des Skalierungssets für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="71a17-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a17-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71a17-132">-Confirm</span></span>
<span data-ttu-id="71a17-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71a17-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a17-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="71a17-134">-WhatIf</span></span>
<span data-ttu-id="71a17-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71a17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a17-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71a17-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a17-137">CommonParameters</span></span>
<span data-ttu-id="71a17-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a17-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71a17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a17-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="71a17-140">INPUTS</span></span>

### <span data-ttu-id="71a17-141">System.String</span><span class="sxs-lookup"><span data-stu-id="71a17-141">System.String</span></span>

### <span data-ttu-id="71a17-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="71a17-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="71a17-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="71a17-143">OUTPUTS</span></span>

### <span data-ttu-id="71a17-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryResponse</span><span class="sxs-lookup"><span data-stu-id="71a17-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="71a17-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="71a17-145">NOTES</span></span>

## <span data-ttu-id="71a17-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="71a17-146">RELATED LINKS</span></span>
