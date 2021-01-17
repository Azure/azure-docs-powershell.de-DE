---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470880"
---
# <span data-ttu-id="70fe4-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="70fe4-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="70fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="70fe4-103">Run command on the Virtual Machine Scale Set VM.</span><span class="sxs-lookup"><span data-stu-id="70fe4-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="70fe4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70fe4-104">SYNTAX</span></span>

### <span data-ttu-id="70fe4-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="70fe4-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70fe4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="70fe4-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70fe4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="70fe4-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70fe4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70fe4-108">DESCRIPTION</span></span>
<span data-ttu-id="70fe4-109">Rufen Sie einen Ausführungsbefehl auf der Virtual Machine Scale Set VM auf.</span><span class="sxs-lookup"><span data-stu-id="70fe4-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="70fe4-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70fe4-110">EXAMPLES</span></span>

### <span data-ttu-id="70fe4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70fe4-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="70fe4-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, wobei das Skript 'sample.ps1' und die Parameter auf der ID '0' VM im Skalierungssatz des virtuellen Computers 'vmssname' in der Ressourcengruppe 'rgname' überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="70fe4-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="70fe4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="70fe4-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="70fe4-114">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, wobei das Skript 'sample.ps1' und die Parameter auf der ID '0' VM im Skalierungssatz des virtuellen Computers 'vmssname' in der Ressourcengruppe 'rgname' überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="70fe4-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="70fe4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70fe4-115">PARAMETERS</span></span>

### <span data-ttu-id="70fe4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70fe4-116">-AsJob</span></span>
<span data-ttu-id="70fe4-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="70fe4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70fe4-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="70fe4-118">-CommandId</span></span>
<span data-ttu-id="70fe4-119">Die Befehls-ID "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="70fe4-119">The run command id.</span></span>

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

### <span data-ttu-id="70fe4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fe4-120">-DefaultProfile</span></span>
<span data-ttu-id="70fe4-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70fe4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70fe4-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="70fe4-122">-InstanceId</span></span>
<span data-ttu-id="70fe4-123">Die Instanz-ID der virtuellen Computerskalen-VM.</span><span class="sxs-lookup"><span data-stu-id="70fe4-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="70fe4-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="70fe4-124">-Parameter</span></span>
<span data-ttu-id="70fe4-125">Die Parameter des Befehls "Ausführen".</span><span class="sxs-lookup"><span data-stu-id="70fe4-125">The run command parameters.</span></span>

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

### <span data-ttu-id="70fe4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70fe4-126">-ResourceGroupName</span></span>
<span data-ttu-id="70fe4-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70fe4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="70fe4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70fe4-128">-ResourceId</span></span>
<span data-ttu-id="70fe4-129">Die Ressourcen-ID für den virtuellen Computerskalensatz VM</span><span class="sxs-lookup"><span data-stu-id="70fe4-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="70fe4-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="70fe4-130">-ScriptPath</span></span>
<span data-ttu-id="70fe4-131">Pfad des auszuführende Skripts.</span><span class="sxs-lookup"><span data-stu-id="70fe4-131">Path of the script to be executed.</span></span>  <span data-ttu-id="70fe4-132">Wenn dieser Wert angegeben wird, überschreibt das angegebene Skript das Standardskript des Befehls.</span><span class="sxs-lookup"><span data-stu-id="70fe4-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="70fe4-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="70fe4-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="70fe4-134">Das PS Virtual Machine Scale Set VM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="70fe4-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="70fe4-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="70fe4-135">-VMScaleSetName</span></span>
<span data-ttu-id="70fe4-136">Der Name der virtuellen Computerskalen-VM.</span><span class="sxs-lookup"><span data-stu-id="70fe4-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="70fe4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70fe4-137">-Confirm</span></span>
<span data-ttu-id="70fe4-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70fe4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70fe4-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70fe4-139">-WhatIf</span></span>
<span data-ttu-id="70fe4-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70fe4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70fe4-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70fe4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70fe4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fe4-142">CommonParameters</span></span>
<span data-ttu-id="70fe4-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70fe4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fe4-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70fe4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fe4-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70fe4-145">INPUTS</span></span>

### <span data-ttu-id="70fe4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="70fe4-146">System.String</span></span>

### <span data-ttu-id="70fe4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="70fe4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="70fe4-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70fe4-148">OUTPUTS</span></span>

### <span data-ttu-id="70fe4-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="70fe4-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="70fe4-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70fe4-150">NOTES</span></span>

## <span data-ttu-id="70fe4-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70fe4-151">RELATED LINKS</span></span>
