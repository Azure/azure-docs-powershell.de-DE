---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176999"
---
# <span data-ttu-id="12776-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="12776-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="12776-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12776-102">SYNOPSIS</span></span>
<span data-ttu-id="12776-103">Befehl "ausführen" auf dem VM-Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="12776-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="12776-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12776-104">SYNTAX</span></span>

### <span data-ttu-id="12776-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="12776-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12776-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="12776-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12776-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="12776-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12776-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12776-108">DESCRIPTION</span></span>
<span data-ttu-id="12776-109">Aufrufen eines Befehls "ausführen" auf dem virtuellen Computer mit Skalierungs Satz</span><span class="sxs-lookup"><span data-stu-id="12776-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="12776-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12776-110">EXAMPLES</span></span>

### <span data-ttu-id="12776-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12776-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="12776-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter für die ID "0" VM im Skalierungs Satz der virtuellen Maschine "vmssname" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="12776-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="12776-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12776-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="12776-114">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter für die ID "0" VM im Skalierungs Satz der virtuellen Maschine "vmssname" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="12776-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="12776-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="12776-115">PARAMETERS</span></span>

### <span data-ttu-id="12776-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12776-116">-AsJob</span></span>
<span data-ttu-id="12776-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12776-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12776-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="12776-118">-CommandId</span></span>
<span data-ttu-id="12776-119">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="12776-119">The run command id.</span></span>

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

### <span data-ttu-id="12776-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12776-120">-DefaultProfile</span></span>
<span data-ttu-id="12776-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12776-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12776-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="12776-122">-InstanceId</span></span>
<span data-ttu-id="12776-123">Die Instanz-ID des VM-Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="12776-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="12776-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="12776-124">-Parameter</span></span>
<span data-ttu-id="12776-125">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="12776-125">The run command parameters.</span></span>

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

### <span data-ttu-id="12776-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12776-126">-ResourceGroupName</span></span>
<span data-ttu-id="12776-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12776-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="12776-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12776-128">-ResourceId</span></span>
<span data-ttu-id="12776-129">Die Ressourcen-ID für den virtuellen Maschinen-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="12776-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="12776-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="12776-130">-ScriptPath</span></span>
<span data-ttu-id="12776-131">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12776-131">Path of the script to be executed.</span></span>  <span data-ttu-id="12776-132">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="12776-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="12776-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="12776-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="12776-134">Das VM-Objekt "Scale" des PS-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="12776-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="12776-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="12776-135">-VMScaleSetName</span></span>
<span data-ttu-id="12776-136">Der Name des VM-Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="12776-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="12776-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12776-137">-Confirm</span></span>
<span data-ttu-id="12776-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12776-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12776-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12776-139">-WhatIf</span></span>
<span data-ttu-id="12776-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12776-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12776-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12776-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12776-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12776-142">CommonParameters</span></span>
<span data-ttu-id="12776-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12776-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12776-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12776-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12776-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12776-145">INPUTS</span></span>

### <span data-ttu-id="12776-146">System. String</span><span class="sxs-lookup"><span data-stu-id="12776-146">System.String</span></span>

### <span data-ttu-id="12776-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="12776-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="12776-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12776-148">OUTPUTS</span></span>

### <span data-ttu-id="12776-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="12776-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="12776-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="12776-150">NOTES</span></span>

## <span data-ttu-id="12776-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12776-151">RELATED LINKS</span></span>
