---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 81f9e57bd2d815616cfc856246ff6950230f7112
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661574"
---
# <span data-ttu-id="4a3a2-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4a3a2-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="4a3a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a3a2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3a2-103">Fügt einen Daten Datenträger zu einer VMSS-VM hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="4a3a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a3a2-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a3a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a3a2-105">DESCRIPTION</span></span>
<span data-ttu-id="4a3a2-106">Das Cmdlet **Add-AzVmssVMDataDisk** fügt einen Daten Datenträger zu einem VMSS-VM hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="4a3a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a3a2-107">EXAMPLES</span></span>

### <span data-ttu-id="4a3a2-108">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einer VMSS-VM</span><span class="sxs-lookup"><span data-stu-id="4a3a2-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="4a3a2-109">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="4a3a2-110">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4a3a2-111">Der nächste Befehl fügt den verwalteten Datenträger der VMSS-VM hinzu, die lokal in $VmssVM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="4a3a2-112">Der endgültige Befehl aktualisiert die VMSS-VM mit hinzugefügtem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="4a3a2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a3a2-113">PARAMETERS</span></span>

### <span data-ttu-id="4a3a2-114">-Caching</span><span class="sxs-lookup"><span data-stu-id="4a3a2-114">-Caching</span></span>
<span data-ttu-id="4a3a2-115">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="4a3a2-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a3a2-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a3a2-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4a3a2-117">ReadOnly</span></span>
- <span data-ttu-id="4a3a2-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4a3a2-118">ReadWrite</span></span>
- <span data-ttu-id="4a3a2-119">None der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="4a3a2-120">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="4a3a2-121">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="4a3a2-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="4a3a2-122">-CreateOption</span></span>
<span data-ttu-id="4a3a2-123">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="4a3a2-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4a3a2-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a3a2-125">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-125">Attach.</span></span>
<span data-ttu-id="4a3a2-126">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="4a3a2-127">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="4a3a2-128">Die *VhdUri* ist alles, was erforderlich ist, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) mitzuteilen, die als Datenträger an den virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="4a3a2-129">Leer.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-129">Empty.</span></span>
<span data-ttu-id="4a3a2-130">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="4a3a2-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-131">FromImage.</span></span>
<span data-ttu-id="4a3a2-132">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="4a3a2-133">Wenn Sie diese Option angeben, müssen Sie auch den *SourceImageUri* -Parameter angeben, um der Azure-Plattform den Speicherort der VHD mitzuteilen, die als Daten Datenträger angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="4a3a2-134">Der *VhdUri* -Parameter wird als Speicherort verwendet, der angibt, wo die VHD des Daten Datenträgers gespeichert wird, wenn Sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="4a3a2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3a2-135">-DefaultProfile</span></span>
<span data-ttu-id="4a3a2-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a3a2-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4a3a2-137">-DiskSizeInGB</span></span>
<span data-ttu-id="4a3a2-138">Gibt die Größe eines leeren Datenträgers an, der an einen virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="4a3a2-139">-LUN</span><span class="sxs-lookup"><span data-stu-id="4a3a2-139">-Lun</span></span>
<span data-ttu-id="4a3a2-140">Gibt die logische Einheitsnummer (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="4a3a2-141">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4a3a2-141">-ManagedDiskId</span></span>
<span data-ttu-id="4a3a2-142">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-142">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="4a3a2-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4a3a2-143">-StorageAccountType</span></span>
<span data-ttu-id="4a3a2-144">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-144">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="4a3a2-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4a3a2-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="4a3a2-146">Gibt das VM-Objekt für den lokalen virtuellen Computer an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="4a3a2-147">Sie können das Cmdlet **Get-AzVmssVM** verwenden, um ein VM-Objekt für einen virtuellen Computer-Skalierungs Satz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-147">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="4a3a2-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4a3a2-148">-WriteAccelerator</span></span>
<span data-ttu-id="4a3a2-149">Gibt an, ob WriteAccelerator auf einem verwalteten Daten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="4a3a2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3a2-150">CommonParameters</span></span>
<span data-ttu-id="4a3a2-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a3a2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3a2-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3a2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3a2-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a3a2-153">INPUTS</span></span>

### <span data-ttu-id="4a3a2-154">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4a3a2-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="4a3a2-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4a3a2-155">System.Int32</span></span>

### <span data-ttu-id="4a3a2-156">System. String</span><span class="sxs-lookup"><span data-stu-id="4a3a2-156">System.String</span></span>

### <span data-ttu-id="4a3a2-157">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="4a3a2-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="4a3a2-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a3a2-158">OUTPUTS</span></span>

### <span data-ttu-id="4a3a2-159">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4a3a2-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4a3a2-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a3a2-160">NOTES</span></span>

## <span data-ttu-id="4a3a2-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a3a2-161">RELATED LINKS</span></span>
