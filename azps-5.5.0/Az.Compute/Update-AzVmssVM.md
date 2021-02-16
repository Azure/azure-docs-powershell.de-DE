---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162188"
---
# <span data-ttu-id="fa7f0-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="fa7f0-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="fa7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7f0-103">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="fa7f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa7f0-104">SYNTAX</span></span>

### <span data-ttu-id="fa7f0-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa7f0-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7f0-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fa7f0-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa7f0-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="fa7f0-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa7f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa7f0-108">DESCRIPTION</span></span>
<span data-ttu-id="fa7f0-109">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="fa7f0-110">Derzeit ist das einzige zulässige Update das Hinzufügen eines verwalteten Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="fa7f0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa7f0-111">EXAMPLES</span></span>

### <span data-ttu-id="fa7f0-112">Beispiel 1: Hinzufügen eines verwalteten Datenspeichers zu einer Vmss VM mithilfe New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fa7f0-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="fa7f0-113">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="fa7f0-114">Der nächste Befehl erstellt ein Datenträgerobjekt mit dem verwalteten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="fa7f0-115">Der nächste Befehl ruft eine vorhandene Vmss VM ab, die durch den Namen der Ressourcengruppe, den Namen der vmss und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="fa7f0-116">Der letzte Befehl aktualisiert die Vmss VM, indem ein neuer Datenträger hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="fa7f0-117">Beispiel 2: Hinzufügen eines verwalteten Datenspeichers zu einer Vmss VM mithilfe Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fa7f0-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="fa7f0-118">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="fa7f0-119">Der nächste Befehl ruft eine vorhandene Vmss VM ab, die durch den Namen der Ressourcengruppe, den Namen der vmss und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="fa7f0-120">Der nächste Befehl fügt den verwalteten Datenträger der vmss VM hinzu, die lokal in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="fa7f0-121">Der letzte Befehl aktualisiert die Vmss VM mit dem hinzugefügten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="fa7f0-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fa7f0-122">Example 3</span></span>

<span data-ttu-id="fa7f0-123">Aktualisiert den Zustand einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="fa7f0-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="fa7f0-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="fa7f0-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa7f0-125">PARAMETERS</span></span>

### <span data-ttu-id="fa7f0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa7f0-126">-AsJob</span></span>
<span data-ttu-id="fa7f0-127">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa7f0-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa7f0-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="fa7f0-128">-DataDisk</span></span>

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

### <span data-ttu-id="fa7f0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7f0-129">-DefaultProfile</span></span>
<span data-ttu-id="fa7f0-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa7f0-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="fa7f0-131">-InstanceId</span></span>
<span data-ttu-id="fa7f0-132">Gibt die Instanz-ID einer VMSS VM an.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="fa7f0-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="fa7f0-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="fa7f0-134">Gibt an, dass die vm für den virtuellen Computermaßstab nicht zum Löschen während eines Scale-In-Vorgangs in Betracht gezogen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="fa7f0-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="fa7f0-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="fa7f0-136">Gibt an, dass auf dem VMSS initiierte Modellupdates oder -aktionen (einschließlich Scale-In) nicht auf die VMSS VM angewendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="fa7f0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7f0-137">-ResourceGroupName</span></span>
<span data-ttu-id="fa7f0-138">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="fa7f0-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa7f0-139">-ResourceId</span></span>
<span data-ttu-id="fa7f0-140">Die Ressourcen-ID für den virtuellen Computerskalensatz VM</span><span class="sxs-lookup"><span data-stu-id="fa7f0-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="fa7f0-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fa7f0-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="fa7f0-142">Local virtual machine scale set VM object</span><span class="sxs-lookup"><span data-stu-id="fa7f0-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="fa7f0-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fa7f0-143">-VMScaleSetName</span></span>
<span data-ttu-id="fa7f0-144">Der Name des Skalierungssets für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="fa7f0-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="fa7f0-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa7f0-145">-Confirm</span></span>
<span data-ttu-id="fa7f0-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa7f0-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa7f0-147">-WhatIf</span></span>
<span data-ttu-id="fa7f0-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7f0-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa7f0-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7f0-150">CommonParameters</span></span>
<span data-ttu-id="fa7f0-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7f0-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7f0-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa7f0-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7f0-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa7f0-153">INPUTS</span></span>

### <span data-ttu-id="fa7f0-154">System.String</span><span class="sxs-lookup"><span data-stu-id="fa7f0-154">System.String</span></span>

### <span data-ttu-id="fa7f0-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="fa7f0-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="fa7f0-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fa7f0-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fa7f0-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa7f0-157">OUTPUTS</span></span>

### <span data-ttu-id="fa7f0-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fa7f0-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fa7f0-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa7f0-159">NOTES</span></span>

## <span data-ttu-id="fa7f0-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa7f0-160">RELATED LINKS</span></span>
