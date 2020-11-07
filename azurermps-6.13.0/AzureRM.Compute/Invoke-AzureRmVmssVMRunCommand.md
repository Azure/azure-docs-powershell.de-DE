---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVmssVMRunCommand.md
ms.openlocfilehash: 1c1cdeff1e1a73de6947855922a4fed45fe387e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664895"
---
# <span data-ttu-id="51aa4-101">Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="51aa4-101">Invoke-AzureRmVmssVMRunCommand</span></span>

## <span data-ttu-id="51aa4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="51aa4-103">Befehl "ausführen" auf dem VM-Skalierungs Satz der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="51aa4-103">Run command on the Virtual Machine Scale Set VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51aa4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51aa4-104">SYNTAX</span></span>

### <span data-ttu-id="51aa4-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="51aa4-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51aa4-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="51aa4-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51aa4-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="51aa4-107">ObjectParameter</span></span>
```
Invoke-AzureRmVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51aa4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51aa4-108">DESCRIPTION</span></span>
<span data-ttu-id="51aa4-109">Aufrufen eines Befehls "ausführen" auf dem virtuellen Computer mit Skalierungs Satz</span><span class="sxs-lookup"><span data-stu-id="51aa4-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="51aa4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51aa4-110">EXAMPLES</span></span>

### <span data-ttu-id="51aa4-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51aa4-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="51aa4-112">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter für die ID "0" VM im Skalierungs Satz der virtuellen Maschine "vmssname" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="51aa4-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="51aa4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51aa4-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzureRmVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="51aa4-114">Rufen Sie einen Ausführungsbefehl von RunPowerShellScript auf, indem Sie das Skript "sample.ps1" und die Parameter für die ID "0" VM im Skalierungs Satz der virtuellen Maschine "vmssname" in der Ressourcengruppe "rgname" überschreiben.</span><span class="sxs-lookup"><span data-stu-id="51aa4-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="51aa4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="51aa4-115">PARAMETERS</span></span>

### <span data-ttu-id="51aa4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51aa4-116">-AsJob</span></span>
<span data-ttu-id="51aa4-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="51aa4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51aa4-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="51aa4-118">-CommandId</span></span>
<span data-ttu-id="51aa4-119">Die Befehls-ID ausführen.</span><span class="sxs-lookup"><span data-stu-id="51aa4-119">The run command id.</span></span>

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

### <span data-ttu-id="51aa4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51aa4-120">-DefaultProfile</span></span>
<span data-ttu-id="51aa4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51aa4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51aa4-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="51aa4-122">-InstanceId</span></span>
<span data-ttu-id="51aa4-123">Die Instanz-ID des VM-Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="51aa4-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="51aa4-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="51aa4-124">-Parameter</span></span>
<span data-ttu-id="51aa4-125">Die Parameter des Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="51aa4-125">The run command parameters.</span></span>

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

### <span data-ttu-id="51aa4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51aa4-126">-ResourceGroupName</span></span>
<span data-ttu-id="51aa4-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="51aa4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="51aa4-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="51aa4-128">-ResourceId</span></span>
<span data-ttu-id="51aa4-129">Die Ressourcen-ID für den virtuellen Maschinen-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="51aa4-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="51aa4-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="51aa4-130">-ScriptPath</span></span>
<span data-ttu-id="51aa4-131">Der Pfad des Skripts, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51aa4-131">Path of the script to be executed.</span></span>  <span data-ttu-id="51aa4-132">Wenn dieser Wert angegeben wird, wird das Standardskript des Befehls vom angegebenen Skript überschrieben.</span><span class="sxs-lookup"><span data-stu-id="51aa4-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="51aa4-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="51aa4-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="51aa4-134">Das VM-Objekt "Scale" des PS-virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="51aa4-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="51aa4-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="51aa4-135">-VMScaleSetName</span></span>
<span data-ttu-id="51aa4-136">Der Name des VM-Skalierungs Satzes für virtuelle Maschinen.</span><span class="sxs-lookup"><span data-stu-id="51aa4-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="51aa4-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51aa4-137">-Confirm</span></span>
<span data-ttu-id="51aa4-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51aa4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51aa4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51aa4-139">-WhatIf</span></span>
<span data-ttu-id="51aa4-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51aa4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51aa4-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51aa4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51aa4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51aa4-142">CommonParameters</span></span>
<span data-ttu-id="51aa4-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51aa4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51aa4-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51aa4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51aa4-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51aa4-145">INPUTS</span></span>

### <span data-ttu-id="51aa4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="51aa4-146">System.String</span></span>

### <span data-ttu-id="51aa4-147">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="51aa4-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="51aa4-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51aa4-148">OUTPUTS</span></span>

### <span data-ttu-id="51aa4-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="51aa4-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="51aa4-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="51aa4-150">NOTES</span></span>

## <span data-ttu-id="51aa4-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51aa4-151">RELATED LINKS</span></span>
