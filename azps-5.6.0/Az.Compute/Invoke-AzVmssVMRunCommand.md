---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: ea4674adaf1069a4681ab4943ad16685540378ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933064"
---
# <span data-ttu-id="3520f-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="3520f-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="3520f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3520f-102">SYNOPSIS</span></span>
<span data-ttu-id="3520f-103">Ausführen des Befehls auf der VIRTUELLEN Computer-Skalierungssatz-VM.</span><span class="sxs-lookup"><span data-stu-id="3520f-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="3520f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3520f-104">SYNTAX</span></span>

### <span data-ttu-id="3520f-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="3520f-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3520f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3520f-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3520f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3520f-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3520f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3520f-108">DESCRIPTION</span></span>
<span data-ttu-id="3520f-109">Rufen Sie einen Ausführungsbefehl auf der VM für den Skalierungssatz virtueller Computer auf.</span><span class="sxs-lookup"><span data-stu-id="3520f-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="3520f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3520f-110">EXAMPLES</span></span>

### <span data-ttu-id="3520f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3520f-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="3520f-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, wobei das Skript "sample.ps1" und die Parameter auf der ID '0' VM im Skalierungssatz des virtuellen Computers von "vmssname" in der Ressourcengruppe "rgname" überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3520f-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="3520f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3520f-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="3520f-114">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, wobei das Skript "sample.ps1" und die Parameter auf der ID '0' VM im Skalierungssatz des virtuellen Computers von "vmssname" in der Ressourcengruppe "rgname" überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3520f-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="3520f-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3520f-115">PARAMETERS</span></span>

### <span data-ttu-id="3520f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3520f-116">-AsJob</span></span>
<span data-ttu-id="3520f-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3520f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3520f-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="3520f-118">-CommandId</span></span>
<span data-ttu-id="3520f-119">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="3520f-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3520f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3520f-120">-DefaultProfile</span></span>
<span data-ttu-id="3520f-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3520f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3520f-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3520f-122">-InstanceId</span></span>
<span data-ttu-id="3520f-123">Die Instanz-ID der Skalierungssatz-VM für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="3520f-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3520f-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3520f-124">-Parameter</span></span>
<span data-ttu-id="3520f-125">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="3520f-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3520f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3520f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3520f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3520f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3520f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3520f-128">-ResourceId</span></span>
<span data-ttu-id="3520f-129">Die Ressourcen-ID für den virtuellen Computerskalensatz VM</span><span class="sxs-lookup"><span data-stu-id="3520f-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="3520f-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="3520f-130">-ScriptPath</span></span>
<span data-ttu-id="3520f-131">Pfad des skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3520f-131">Path of the script to be executed.</span></span>  <span data-ttu-id="3520f-132">Wenn dieser Wert angegeben wird, überschreibt das angegebene Skript das Standardskript des Befehls.</span><span class="sxs-lookup"><span data-stu-id="3520f-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3520f-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="3520f-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="3520f-134">Das PS Virtual Machine Scale Set VM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3520f-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3520f-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3520f-135">-VMScaleSetName</span></span>
<span data-ttu-id="3520f-136">Der Name der Skalierungssatz-VM für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="3520f-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="3520f-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3520f-137">-Confirm</span></span>
<span data-ttu-id="3520f-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3520f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3520f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3520f-139">-WhatIf</span></span>
<span data-ttu-id="3520f-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3520f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3520f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3520f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3520f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3520f-142">CommonParameters</span></span>
<span data-ttu-id="3520f-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3520f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3520f-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3520f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3520f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3520f-145">INPUTS</span></span>

### <span data-ttu-id="3520f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3520f-146">System.String</span></span>

### <span data-ttu-id="3520f-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="3520f-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="3520f-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3520f-148">OUTPUTS</span></span>

### <span data-ttu-id="3520f-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="3520f-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="3520f-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3520f-150">NOTES</span></span>

## <span data-ttu-id="3520f-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3520f-151">RELATED LINKS</span></span>
