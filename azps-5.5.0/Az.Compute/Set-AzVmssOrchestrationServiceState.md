---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164172"
---
# <span data-ttu-id="17ace-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="17ace-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="17ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ace-102">SYNOPSIS</span></span>
<span data-ttu-id="17ace-103">Legt den Zustand des Orchestrierungsdiensts für die VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="17ace-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="17ace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17ace-104">SYNTAX</span></span>

### <span data-ttu-id="17ace-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="17ace-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17ace-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="17ace-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17ace-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="17ace-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17ace-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17ace-108">DESCRIPTION</span></span>
<span data-ttu-id="17ace-109">Legt den Zustand des Orchestrierungsdiensts für die VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="17ace-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="17ace-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17ace-110">EXAMPLES</span></span>

### <span data-ttu-id="17ace-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17ace-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="17ace-112">Dieser Befehl setzt den Dienst für automatische Reparaturen auf der VMSS "vmss1" in der Ressourcengruppe "rg" an.</span><span class="sxs-lookup"><span data-stu-id="17ace-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="17ace-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="17ace-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="17ace-114">Dieser Befehl setzt den Dienst für automatische Reparaturen auf der VMSS "vmss1" in der Ressourcengruppe "rg" fort.</span><span class="sxs-lookup"><span data-stu-id="17ace-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="17ace-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17ace-115">PARAMETERS</span></span>

### <span data-ttu-id="17ace-116">-Aktion</span><span class="sxs-lookup"><span data-stu-id="17ace-116">-Action</span></span>
<span data-ttu-id="17ace-117">Die aktion, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17ace-117">The action to be performed.</span></span>  <span data-ttu-id="17ace-118">Mögliche Werte: "Fortsetzen", "Anhalten".</span><span class="sxs-lookup"><span data-stu-id="17ace-118">Possible values are: Resume, Suspend.</span></span>

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

### <span data-ttu-id="17ace-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17ace-119">-AsJob</span></span>
<span data-ttu-id="17ace-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="17ace-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17ace-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ace-121">-DefaultProfile</span></span>
<span data-ttu-id="17ace-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17ace-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ace-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17ace-123">-InputObject</span></span>
<span data-ttu-id="17ace-124">Das lokale Objekt des Skalierungssets für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="17ace-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="17ace-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ace-125">-ResourceGroupName</span></span>
<span data-ttu-id="17ace-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="17ace-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="17ace-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17ace-127">-ResourceId</span></span>
<span data-ttu-id="17ace-128">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="17ace-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="17ace-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17ace-129">-ServiceName</span></span>
<span data-ttu-id="17ace-130">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="17ace-130">The name of the service.</span></span>

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

### <span data-ttu-id="17ace-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="17ace-131">-VMScaleSetName</span></span>
<span data-ttu-id="17ace-132">Der Name des Skalierungssets für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="17ace-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="17ace-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17ace-133">-Confirm</span></span>
<span data-ttu-id="17ace-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17ace-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17ace-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="17ace-135">-WhatIf</span></span>
<span data-ttu-id="17ace-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17ace-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17ace-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17ace-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17ace-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ace-138">CommonParameters</span></span>
<span data-ttu-id="17ace-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ace-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ace-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17ace-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ace-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17ace-141">INPUTS</span></span>

### <span data-ttu-id="17ace-142">System.String</span><span class="sxs-lookup"><span data-stu-id="17ace-142">System.String</span></span>

### <span data-ttu-id="17ace-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17ace-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17ace-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17ace-144">OUTPUTS</span></span>

### <span data-ttu-id="17ace-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="17ace-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="17ace-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="17ace-146">NOTES</span></span>

## <span data-ttu-id="17ace-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="17ace-147">RELATED LINKS</span></span>
