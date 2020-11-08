---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: c1fbc45a9d82733f73a13b13985bdd6746f4c075
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010213"
---
# <span data-ttu-id="4936a-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="4936a-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="4936a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4936a-102">SYNOPSIS</span></span>
<span data-ttu-id="4936a-103">Legt den Orchestrierungs Dienstzustand für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="4936a-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="4936a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4936a-104">SYNTAX</span></span>

### <span data-ttu-id="4936a-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="4936a-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4936a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4936a-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4936a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4936a-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4936a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4936a-108">DESCRIPTION</span></span>
<span data-ttu-id="4936a-109">Legt den Orchestrierungs Dienstzustand für VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="4936a-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="4936a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4936a-110">EXAMPLES</span></span>

### <span data-ttu-id="4936a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4936a-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="4936a-112">Dieser Befehl unterbricht den automatischen Reparaturdienst auf der VMSS "vmss1" in der Ressourcengruppe "RG".</span><span class="sxs-lookup"><span data-stu-id="4936a-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="4936a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4936a-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="4936a-114">Dieser Befehl setzt den automatischen Reparaturdienst auf der VMSS "vmss1" in der Ressourcengruppe "RG" fort.</span><span class="sxs-lookup"><span data-stu-id="4936a-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="4936a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4936a-115">PARAMETERS</span></span>

### <span data-ttu-id="4936a-116">– Aktion</span><span class="sxs-lookup"><span data-stu-id="4936a-116">-Action</span></span>
<span data-ttu-id="4936a-117">Die auszuführende Aktion.</span><span class="sxs-lookup"><span data-stu-id="4936a-117">The action to be performed.</span></span>  <span data-ttu-id="4936a-118">Mögliche Werte sind: Resume, Suspend.</span><span class="sxs-lookup"><span data-stu-id="4936a-118">Possible values are: Resume, Suspend.</span></span>

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

### <span data-ttu-id="4936a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4936a-119">-AsJob</span></span>
<span data-ttu-id="4936a-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4936a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4936a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4936a-121">-DefaultProfile</span></span>
<span data-ttu-id="4936a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4936a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4936a-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4936a-123">-InputObject</span></span>
<span data-ttu-id="4936a-124">Das lokale Objekt des Skalierungs Satzes der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="4936a-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4936a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4936a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4936a-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4936a-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4936a-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4936a-127">-ResourceId</span></span>
<span data-ttu-id="4936a-128">Die ID der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4936a-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="4936a-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4936a-129">-ServiceName</span></span>
<span data-ttu-id="4936a-130">Der Name des Diensts.</span><span class="sxs-lookup"><span data-stu-id="4936a-130">The name of the service.</span></span>

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

### <span data-ttu-id="4936a-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4936a-131">-VMScaleSetName</span></span>
<span data-ttu-id="4936a-132">Der Name des Skalierungs Satzes für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4936a-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="4936a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4936a-133">-Confirm</span></span>
<span data-ttu-id="4936a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4936a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4936a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4936a-135">-WhatIf</span></span>
<span data-ttu-id="4936a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4936a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4936a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4936a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4936a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4936a-138">CommonParameters</span></span>
<span data-ttu-id="4936a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4936a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4936a-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4936a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4936a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4936a-141">INPUTS</span></span>

### <span data-ttu-id="4936a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4936a-142">System.String</span></span>

### <span data-ttu-id="4936a-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4936a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4936a-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4936a-144">OUTPUTS</span></span>

### <span data-ttu-id="4936a-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4936a-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4936a-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="4936a-146">NOTES</span></span>

## <span data-ttu-id="4936a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4936a-147">RELATED LINKS</span></span>
