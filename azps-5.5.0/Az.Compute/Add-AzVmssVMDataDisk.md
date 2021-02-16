---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162324"
---
# <span data-ttu-id="e80ab-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e80ab-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="e80ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e80ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e80ab-103">Fügt einen Datendatenträger einer Vmss VM hinzu.</span><span class="sxs-lookup"><span data-stu-id="e80ab-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e80ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e80ab-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e80ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e80ab-105">DESCRIPTION</span></span>
<span data-ttu-id="e80ab-106">Das **Cmdlet "Add-AzVmssVMDataDisk"** fügt einer Vmss VM einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="e80ab-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="e80ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e80ab-107">EXAMPLES</span></span>

### <span data-ttu-id="e80ab-108">Beispiel 1: Hinzufügen eines verwalteten Datenspeichers zu einer Vmss VM.</span><span class="sxs-lookup"><span data-stu-id="e80ab-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="e80ab-109">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="e80ab-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e80ab-110">Der nächste Befehl ruft eine vorhandene Vmss VM ab, die durch den Namen der Ressourcengruppe, den Namen der vmss und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e80ab-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e80ab-111">Der nächste Befehl fügt den verwalteten Datenträger der vmss VM hinzu, die lokal in $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="e80ab-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="e80ab-112">Der letzte Befehl aktualisiert die Vmss VM mit dem hinzugefügten Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e80ab-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="e80ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e80ab-113">PARAMETERS</span></span>

### <span data-ttu-id="e80ab-114">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="e80ab-114">-Caching</span></span>
<span data-ttu-id="e80ab-115">Gibt den Zwischenspeicherungsmodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="e80ab-116">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="e80ab-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e80ab-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e80ab-117">ReadOnly</span></span>
- <span data-ttu-id="e80ab-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e80ab-118">ReadWrite</span></span>
- <span data-ttu-id="e80ab-119">Keine Der Standardwert ist "ReadWrite".</span><span class="sxs-lookup"><span data-stu-id="e80ab-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="e80ab-120">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="e80ab-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e80ab-121">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="e80ab-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80ab-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e80ab-122">-CreateOption</span></span>
<span data-ttu-id="e80ab-123">Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="e80ab-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="e80ab-124">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="e80ab-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e80ab-125">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="e80ab-125">Attach.</span></span>
<span data-ttu-id="e80ab-126">Geben Sie diese Option an, um einen virtuellen Computer von einem speziellen Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e80ab-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e80ab-127">Wenn Sie diese Option angeben, geben Sie nicht den *Parameter "SourceImageUri"* an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e80ab-128">Der *VhdUri* ist alles, was benötigt wird, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) zu mitteilen, die als Datenträger an den virtuellen Computer anfügen soll.</span><span class="sxs-lookup"><span data-stu-id="e80ab-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="e80ab-129">Leer</span><span class="sxs-lookup"><span data-stu-id="e80ab-129">Empty.</span></span>
<span data-ttu-id="e80ab-130">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e80ab-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="e80ab-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e80ab-131">FromImage.</span></span>
<span data-ttu-id="e80ab-132">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e80ab-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="e80ab-133">Wenn Sie diese Option angeben, müssen Sie auch den *Parameter "SourceImageUri"* angeben, um der Azure-Plattform den Speicherort der VHD anzugeben, die als Datenträger anfügen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e80ab-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="e80ab-134">Der *Parameter "VhdUri"* wird als Speicherort verwendet, an dem die Festplatte VHD gespeichert wird, wenn sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e80ab-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="e80ab-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80ab-135">-DefaultProfile</span></span>
<span data-ttu-id="e80ab-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e80ab-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e80ab-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e80ab-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e80ab-138">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e80ab-139">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e80ab-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e80ab-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e80ab-140">-DiskSizeInGB</span></span>
<span data-ttu-id="e80ab-141">Gibt die Größe (in Gigabyte) eines leeren Datenträgers an, der an einen virtuellen Computer anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="e80ab-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80ab-142">-Lun</span><span class="sxs-lookup"><span data-stu-id="e80ab-142">-Lun</span></span>
<span data-ttu-id="e80ab-143">Gibt die Wahrheitsnummer einer Einheit (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80ab-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e80ab-144">-ManagedDiskId</span></span>
<span data-ttu-id="e80ab-145">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e80ab-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e80ab-146">-StorageAccountType</span></span>
<span data-ttu-id="e80ab-147">Gibt den Speicherkontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e80ab-147">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e80ab-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e80ab-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="e80ab-149">Gibt das Virtuelle Computerskalensatz-Objekt für den lokalen virtuellen Computer an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e80ab-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="e80ab-150">Sie können das **Get-AzVmssVM-Cmdlet** verwenden, um ein Virtual Machine Scale Set -VM-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e80ab-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e80ab-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e80ab-151">-WriteAccelerator</span></span>
<span data-ttu-id="e80ab-152">Gibt an, ob WriteAccelerator auf einem verwalteten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e80ab-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="e80ab-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80ab-153">CommonParameters</span></span>
<span data-ttu-id="e80ab-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80ab-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80ab-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e80ab-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80ab-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e80ab-156">INPUTS</span></span>

### <span data-ttu-id="e80ab-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e80ab-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="e80ab-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e80ab-158">System.Int32</span></span>

### <span data-ttu-id="e80ab-159">System.String</span><span class="sxs-lookup"><span data-stu-id="e80ab-159">System.String</span></span>

### <span data-ttu-id="e80ab-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="e80ab-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="e80ab-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e80ab-161">OUTPUTS</span></span>

### <span data-ttu-id="e80ab-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="e80ab-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="e80ab-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e80ab-163">NOTES</span></span>

## <span data-ttu-id="e80ab-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e80ab-164">RELATED LINKS</span></span>
