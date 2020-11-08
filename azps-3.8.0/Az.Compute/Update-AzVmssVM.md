---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: 0a7b11edad8fd19087b634111a67bc704abf6bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004791"
---
# <span data-ttu-id="13871-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="13871-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="13871-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13871-102">SYNOPSIS</span></span>
<span data-ttu-id="13871-103">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="13871-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="13871-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13871-104">SYNTAX</span></span>

### <span data-ttu-id="13871-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="13871-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13871-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="13871-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13871-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="13871-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13871-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13871-108">DESCRIPTION</span></span>
<span data-ttu-id="13871-109">Aktualisiert den Zustand einer VMSS-VM.</span><span class="sxs-lookup"><span data-stu-id="13871-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="13871-110">Im Moment ist das einzige zulässige Update das Hinzufügen eines verwalteten Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="13871-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="13871-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13871-111">EXAMPLES</span></span>

### <span data-ttu-id="13871-112">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="13871-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="13871-113">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="13871-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="13871-114">Mit dem nächsten Befehl wird ein Datenträgerobjekt mit dem verwalteten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="13871-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="13871-115">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13871-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="13871-116">Der endgültige Befehl aktualisiert die VMSS-VM durch Hinzufügen eines neuen Daten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="13871-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="13871-117">Beispiel 2: Hinzufügen eines verwalteten Daten Datenträgers zu einem VMSS-VM mithilfe von Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="13871-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="13871-118">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="13871-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="13871-119">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13871-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="13871-120">Der nächste Befehl fügt den verwalteten Datenträger der VMSS-VM hinzu, die lokal in $VmssVM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="13871-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="13871-121">Der endgültige Befehl aktualisiert die VMSS-VM mit hinzugefügtem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="13871-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="13871-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="13871-122">PARAMETERS</span></span>

### <span data-ttu-id="13871-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13871-123">-AsJob</span></span>
<span data-ttu-id="13871-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="13871-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13871-125">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="13871-125">-DataDisk</span></span>

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

### <span data-ttu-id="13871-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13871-126">-DefaultProfile</span></span>
<span data-ttu-id="13871-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13871-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13871-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="13871-128">-InstanceId</span></span>
<span data-ttu-id="13871-129">Gibt die Instanz-ID einer VMSS-VM an.</span><span class="sxs-lookup"><span data-stu-id="13871-129">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="13871-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="13871-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="13871-131">Gibt an, dass der VM-Skalierungs Satz virtueller Computer nicht während eines Skalierungsvorgangs zum Löschen berücksichtigt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="13871-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="13871-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="13871-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="13871-133">Gibt an, dass Modellaktualisierungen oder Aktionen (einschließlich Scale-in), die auf der VMSS initiiert wurden, nicht auf die VMSS-VM angewendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="13871-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="13871-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13871-134">-ResourceGroupName</span></span>
<span data-ttu-id="13871-135">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="13871-135">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="13871-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="13871-136">-ResourceId</span></span>
<span data-ttu-id="13871-137">Die Ressourcen-ID für den virtuellen Maschinen-Skalierungs Satz VM</span><span class="sxs-lookup"><span data-stu-id="13871-137">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="13871-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="13871-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="13871-139">Skalierungs Satz des lokalen virtuellen Computers (VM-Objekt)</span><span class="sxs-lookup"><span data-stu-id="13871-139">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="13871-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13871-140">-VMScaleSetName</span></span>
<span data-ttu-id="13871-141">Der Name des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="13871-141">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="13871-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13871-142">-Confirm</span></span>
<span data-ttu-id="13871-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13871-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13871-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13871-144">-WhatIf</span></span>
<span data-ttu-id="13871-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13871-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13871-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13871-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13871-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13871-147">CommonParameters</span></span>
<span data-ttu-id="13871-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13871-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13871-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13871-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13871-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13871-150">INPUTS</span></span>

### <span data-ttu-id="13871-151">System. String</span><span class="sxs-lookup"><span data-stu-id="13871-151">System.String</span></span>

### <span data-ttu-id="13871-152">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="13871-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="13871-153">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="13871-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="13871-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13871-154">OUTPUTS</span></span>

### <span data-ttu-id="13871-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="13871-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="13871-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="13871-156">NOTES</span></span>

## <span data-ttu-id="13871-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13871-157">RELATED LINKS</span></span>
