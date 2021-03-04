---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: 6c483e4146f4bb3ed7207fa5dc0805db239a63d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920595"
---
# <span data-ttu-id="f1b03-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="f1b03-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="f1b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b03-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b03-103">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="f1b03-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="f1b03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b03-104">SYNTAX</span></span>

### <span data-ttu-id="f1b03-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1b03-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1b03-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f1b03-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1b03-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f1b03-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1b03-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1b03-108">DESCRIPTION</span></span>
<span data-ttu-id="f1b03-109">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="f1b03-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="f1b03-110">Derzeit ist das einzige zulässige Update das Hinzufügen eines verwalteten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="f1b03-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="f1b03-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1b03-111">EXAMPLES</span></span>

### <span data-ttu-id="f1b03-112">Beispiel 1: Hinzufügen eines verwalteten Datenträgers zu einer Vmss-VM mithilfe New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1b03-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="f1b03-113">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="f1b03-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f1b03-114">Mit dem nächsten Befehl wird ein Datenträgerobjekt mit dem verwalteten Datenträger erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1b03-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="f1b03-115">Der nächste Befehl ruft eine vorhandene Vmss-VM ab, die vom Ressourcengruppennamen, dem Vmss-Namen und der Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1b03-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f1b03-116">Mit dem letzten Befehl wird die VM vmss aktualisiert, indem ein neuer Datenträger hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b03-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="f1b03-117">Beispiel 2: Hinzufügen eines verwalteten Datenträgers zu einer Vmss-VM mithilfe Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f1b03-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="f1b03-118">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="f1b03-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="f1b03-119">Der nächste Befehl ruft eine vorhandene Vmss-VM ab, die vom Ressourcengruppennamen, dem Vmss-Namen und der Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f1b03-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="f1b03-120">Mit dem nächsten Befehl wird der verwalteten Festplatte der vmss VM, die lokal in der Datei gespeichert ist, $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="f1b03-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="f1b03-121">Mit dem letzten Befehl wird die Vmss-VM mit dem hinzugefügten Datenträger aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f1b03-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="f1b03-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f1b03-122">Example 3</span></span>

<span data-ttu-id="f1b03-123">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="f1b03-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="f1b03-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="f1b03-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="f1b03-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1b03-125">PARAMETERS</span></span>

### <span data-ttu-id="f1b03-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1b03-126">-AsJob</span></span>
<span data-ttu-id="f1b03-127">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f1b03-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1b03-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="f1b03-128">-DataDisk</span></span>

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

### <span data-ttu-id="f1b03-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b03-129">-DefaultProfile</span></span>
<span data-ttu-id="f1b03-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1b03-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b03-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f1b03-131">-InstanceId</span></span>
<span data-ttu-id="f1b03-132">Gibt die Instanz-ID einer VMSS-VM an.</span><span class="sxs-lookup"><span data-stu-id="f1b03-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="f1b03-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="f1b03-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="f1b03-134">Gibt an, dass die VM für den Skalierungssatz für virtuelle Computer während eines Skalierungsvorgangs nicht zum Löschen in Betracht gezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="f1b03-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="f1b03-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="f1b03-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="f1b03-136">Gibt an, dass Modellupdates oder Aktionen (einschließlich scale-in), die auf dem VMSS initiiert wurden, nicht auf die VMSS-VM angewendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="f1b03-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="f1b03-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b03-137">-ResourceGroupName</span></span>
<span data-ttu-id="f1b03-138">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f1b03-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="f1b03-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1b03-139">-ResourceId</span></span>
<span data-ttu-id="f1b03-140">Die Ressourcen-ID für den virtuellen Computerskalensatz VM</span><span class="sxs-lookup"><span data-stu-id="f1b03-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="f1b03-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f1b03-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="f1b03-142">Vm-Objekt für den Skalierungssatz für lokale virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="f1b03-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="f1b03-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f1b03-143">-VMScaleSetName</span></span>
<span data-ttu-id="f1b03-144">Der Name des Skalierungssets für virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="f1b03-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="f1b03-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1b03-145">-Confirm</span></span>
<span data-ttu-id="f1b03-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1b03-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1b03-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b03-147">-WhatIf</span></span>
<span data-ttu-id="f1b03-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1b03-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b03-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1b03-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1b03-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b03-150">CommonParameters</span></span>
<span data-ttu-id="f1b03-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b03-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b03-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1b03-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b03-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1b03-153">INPUTS</span></span>

### <span data-ttu-id="f1b03-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f1b03-154">System.String</span></span>

### <span data-ttu-id="f1b03-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="f1b03-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="f1b03-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f1b03-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f1b03-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1b03-157">OUTPUTS</span></span>

### <span data-ttu-id="f1b03-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="f1b03-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="f1b03-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1b03-159">NOTES</span></span>

## <span data-ttu-id="f1b03-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1b03-160">RELATED LINKS</span></span>
