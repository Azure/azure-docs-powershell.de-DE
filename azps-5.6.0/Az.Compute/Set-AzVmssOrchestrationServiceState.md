---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934488"
---
# <span data-ttu-id="55dfb-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="55dfb-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="55dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="55dfb-103">Legt den Orchestrierungsdienststatus für den VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="55dfb-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="55dfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55dfb-104">SYNTAX</span></span>

### <span data-ttu-id="55dfb-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="55dfb-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55dfb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="55dfb-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55dfb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="55dfb-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55dfb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55dfb-108">DESCRIPTION</span></span>
<span data-ttu-id="55dfb-109">Legt den Orchestrierungsdienststatus für den VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="55dfb-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="55dfb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55dfb-110">EXAMPLES</span></span>

### <span data-ttu-id="55dfb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55dfb-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="55dfb-112">Mit diesem Befehl wird der Dienst für automatische Reparaturen auf dem VMSS "vmss1" in der Ressourcengruppe "rg" angehalten.</span><span class="sxs-lookup"><span data-stu-id="55dfb-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="55dfb-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55dfb-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="55dfb-114">Mit diesem Befehl wird der Dienst "Automatische Reparaturen" auf dem VMSS "vmss1" in der Ressourcengruppe "rg" fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="55dfb-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="55dfb-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="55dfb-115">PARAMETERS</span></span>

### <span data-ttu-id="55dfb-116">-Aktion</span><span class="sxs-lookup"><span data-stu-id="55dfb-116">-Action</span></span>
<span data-ttu-id="55dfb-117">Die aktion, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55dfb-117">The action to be performed.</span></span>  <span data-ttu-id="55dfb-118">Mögliche Werte sind: Fortsetzen, Anhalten.</span><span class="sxs-lookup"><span data-stu-id="55dfb-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55dfb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55dfb-119">-AsJob</span></span>
<span data-ttu-id="55dfb-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="55dfb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55dfb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dfb-121">-DefaultProfile</span></span>
<span data-ttu-id="55dfb-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55dfb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55dfb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55dfb-123">-InputObject</span></span>
<span data-ttu-id="55dfb-124">Das lokale Objekt des Skalierungssets für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="55dfb-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="55dfb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55dfb-125">-ResourceGroupName</span></span>
<span data-ttu-id="55dfb-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55dfb-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="55dfb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55dfb-127">-ResourceId</span></span>
<span data-ttu-id="55dfb-128">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="55dfb-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="55dfb-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="55dfb-129">-ServiceName</span></span>
<span data-ttu-id="55dfb-130">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="55dfb-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55dfb-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="55dfb-131">-VMScaleSetName</span></span>
<span data-ttu-id="55dfb-132">Der Name des Skalierungssets für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="55dfb-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="55dfb-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="55dfb-133">-Confirm</span></span>
<span data-ttu-id="55dfb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55dfb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55dfb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55dfb-135">-WhatIf</span></span>
<span data-ttu-id="55dfb-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55dfb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55dfb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55dfb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55dfb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dfb-138">CommonParameters</span></span>
<span data-ttu-id="55dfb-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55dfb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dfb-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55dfb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dfb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55dfb-141">INPUTS</span></span>

### <span data-ttu-id="55dfb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="55dfb-142">System.String</span></span>

### <span data-ttu-id="55dfb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="55dfb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="55dfb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55dfb-144">OUTPUTS</span></span>

### <span data-ttu-id="55dfb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="55dfb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="55dfb-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="55dfb-146">NOTES</span></span>

## <span data-ttu-id="55dfb-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="55dfb-147">RELATED LINKS</span></span>
