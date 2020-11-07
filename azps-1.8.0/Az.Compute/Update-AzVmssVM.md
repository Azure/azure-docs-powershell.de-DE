---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: d5dc3afe69495e5fef8c0a1ad5a9d155fd15d295
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661401"
---
# <span data-ttu-id="6b9d8-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="6b9d8-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="6b9d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9d8-103">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="6b9d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b9d8-104">SYNTAX</span></span>

### <span data-ttu-id="6b9d8-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b9d8-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9d8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6b9d8-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9d8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6b9d8-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b9d8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b9d8-108">DESCRIPTION</span></span>
<span data-ttu-id="6b9d8-109">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="6b9d8-110">Im Moment ist das einzige zulässige Update das Hinzufügen eines verwalteten Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="6b9d8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b9d8-111">EXAMPLES</span></span>

### <span data-ttu-id="6b9d8-112">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b9d8-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="6b9d8-113">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="6b9d8-114">Mit dem nächsten Befehl wird ein Datenträgerobjekt mit dem verwalteten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="6b9d8-115">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="6b9d8-116">Der endgültige Befehl aktualisiert die VMSS-VM durch Hinzufügen eines neuen Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="6b9d8-117">Beispiel 2: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b9d8-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="6b9d8-118">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="6b9d8-119">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="6b9d8-120">Der nächste Befehl fügt den verwalteten Datenträger der VMSS-VM hinzu, die lokal in $VmssVM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="6b9d8-121">Der endgültige Befehl aktualisiert die VMSS-VM mit hinzugefügtem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="6b9d8-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b9d8-122">PARAMETERS</span></span>

### <span data-ttu-id="6b9d8-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b9d8-123">-AsJob</span></span>
<span data-ttu-id="6b9d8-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6b9d8-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b9d8-125">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="6b9d8-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9d8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9d8-126">-DefaultProfile</span></span>
<span data-ttu-id="6b9d8-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9d8-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6b9d8-128">-InstanceId</span></span>
<span data-ttu-id="6b9d8-129">Gibt die Instanz-ID einer VMSS-VM an.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-129">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="6b9d8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9d8-130">-ResourceGroupName</span></span>
<span data-ttu-id="6b9d8-131">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="6b9d8-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6b9d8-132">-ResourceId</span></span>
<span data-ttu-id="6b9d8-133">Die Ressourcen-ID für den virtuellen Maschinen-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="6b9d8-133">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="6b9d8-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="6b9d8-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="6b9d8-135">Skalierungs Satz des lokalen virtuellen Computers (VM-Objekt)</span><span class="sxs-lookup"><span data-stu-id="6b9d8-135">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9d8-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6b9d8-136">-VMScaleSetName</span></span>
<span data-ttu-id="6b9d8-137">Der Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="6b9d8-137">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="6b9d8-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b9d8-138">-Confirm</span></span>
<span data-ttu-id="6b9d8-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9d8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9d8-140">-WhatIf</span></span>
<span data-ttu-id="6b9d8-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9d8-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9d8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9d8-143">CommonParameters</span></span>
<span data-ttu-id="6b9d8-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b9d8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9d8-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b9d8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9d8-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b9d8-146">INPUTS</span></span>

### <span data-ttu-id="6b9d8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6b9d8-147">System.String</span></span>

### <span data-ttu-id="6b9d8-148">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="6b9d8-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="6b9d8-149">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="6b9d8-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="6b9d8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b9d8-150">OUTPUTS</span></span>

### <span data-ttu-id="6b9d8-151">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="6b9d8-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="6b9d8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b9d8-152">NOTES</span></span>

## <span data-ttu-id="6b9d8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b9d8-153">RELATED LINKS</span></span>
