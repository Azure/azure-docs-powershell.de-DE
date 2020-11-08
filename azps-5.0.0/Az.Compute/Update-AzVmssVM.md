---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176962"
---
# <span data-ttu-id="a558f-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="a558f-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="a558f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a558f-102">SYNOPSIS</span></span>
<span data-ttu-id="a558f-103">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="a558f-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="a558f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a558f-104">SYNTAX</span></span>

### <span data-ttu-id="a558f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a558f-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a558f-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="a558f-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a558f-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="a558f-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a558f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a558f-108">DESCRIPTION</span></span>
<span data-ttu-id="a558f-109">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="a558f-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="a558f-110">Im Moment ist das einzige zulässige Update das Hinzufügen eines verwalteten Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="a558f-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="a558f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a558f-111">EXAMPLES</span></span>

### <span data-ttu-id="a558f-112">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a558f-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="a558f-113">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="a558f-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="a558f-114">Mit dem nächsten Befehl wird ein Datenträgerobjekt mit dem verwalteten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="a558f-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="a558f-115">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a558f-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="a558f-116">Der endgültige Befehl aktualisiert die VMSS-VM durch Hinzufügen eines neuen Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="a558f-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="a558f-117">Beispiel 2: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a558f-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="a558f-118">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="a558f-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="a558f-119">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a558f-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="a558f-120">Der nächste Befehl fügt den verwalteten Datenträger der VMSS-VM hinzu, die lokal in $VmssVM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a558f-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="a558f-121">Der endgültige Befehl aktualisiert die VMSS-VM mit hinzugefügtem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a558f-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="a558f-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a558f-122">Example 3</span></span>

<span data-ttu-id="a558f-123">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="a558f-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="a558f-124">automatisch</span><span class="sxs-lookup"><span data-stu-id="a558f-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="a558f-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="a558f-125">PARAMETERS</span></span>

### <span data-ttu-id="a558f-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a558f-126">-AsJob</span></span>
<span data-ttu-id="a558f-127">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a558f-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a558f-128">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="a558f-128">-DataDisk</span></span>

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

### <span data-ttu-id="a558f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a558f-129">-DefaultProfile</span></span>
<span data-ttu-id="a558f-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a558f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a558f-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a558f-131">-InstanceId</span></span>
<span data-ttu-id="a558f-132">Gibt die Instanz-ID einer VMSS-VM an.</span><span class="sxs-lookup"><span data-stu-id="a558f-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="a558f-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="a558f-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="a558f-134">Gibt an, dass der VM-Skalierungs Satz virtueller Computer nicht während eines Skalierungsvorgangs zum Löschen berücksichtigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="a558f-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558f-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="a558f-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="a558f-136">Gibt an, dass Modellaktualisierungen oder Aktionen (einschließlich Scale-in), die auf der VMSS initiiert wurden, nicht auf die VMSS-VM angewendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="a558f-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a558f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a558f-137">-ResourceGroupName</span></span>
<span data-ttu-id="a558f-138">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="a558f-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="a558f-139">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a558f-139">-ResourceId</span></span>
<span data-ttu-id="a558f-140">Die Ressourcen-ID für den virtuellen Maschinen-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="a558f-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="a558f-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a558f-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="a558f-142">Skalierungs Satz des lokalen virtuellen Computers (VM-Objekt)</span><span class="sxs-lookup"><span data-stu-id="a558f-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="a558f-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a558f-143">-VMScaleSetName</span></span>
<span data-ttu-id="a558f-144">Der Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="a558f-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="a558f-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a558f-145">-Confirm</span></span>
<span data-ttu-id="a558f-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a558f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a558f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a558f-147">-WhatIf</span></span>
<span data-ttu-id="a558f-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a558f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a558f-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a558f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a558f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a558f-150">CommonParameters</span></span>
<span data-ttu-id="a558f-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a558f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a558f-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a558f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a558f-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a558f-153">INPUTS</span></span>

### <span data-ttu-id="a558f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a558f-154">System.String</span></span>

### <span data-ttu-id="a558f-155">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="a558f-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="a558f-156">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a558f-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a558f-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a558f-157">OUTPUTS</span></span>

### <span data-ttu-id="a558f-158">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="a558f-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="a558f-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="a558f-159">NOTES</span></span>

## <span data-ttu-id="a558f-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a558f-160">RELATED LINKS</span></span>
