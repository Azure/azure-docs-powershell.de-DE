---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179290"
---
# <span data-ttu-id="b803c-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b803c-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="b803c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b803c-102">SYNOPSIS</span></span>
<span data-ttu-id="b803c-103">Fügt einen Daten Datenträger zu einer VMSS-VM hinzu.</span><span class="sxs-lookup"><span data-stu-id="b803c-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="b803c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b803c-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b803c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b803c-105">DESCRIPTION</span></span>
<span data-ttu-id="b803c-106">Das Cmdlet **Add-AzVmssVMDataDisk** fügt einen Daten Datenträger zu einem VMSS-VM hinzu.</span><span class="sxs-lookup"><span data-stu-id="b803c-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="b803c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b803c-107">EXAMPLES</span></span>

### <span data-ttu-id="b803c-108">Beispiel 1: Hinzufügen eines verwalteten Daten Datenträgers zu einer VMSS-VM</span><span class="sxs-lookup"><span data-stu-id="b803c-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="b803c-109">Der erste Befehl ruft einen vorhandenen verwalteten Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="b803c-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="b803c-110">Der nächste Befehl ruft eine vorhandene VMSS-VM ab, die durch den Ressourcengruppennamen, den VMSS-Namen und die Instanz-ID angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b803c-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b803c-111">Der nächste Befehl fügt den verwalteten Datenträger der VMSS-VM hinzu, die lokal in $VmssVM gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b803c-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="b803c-112">Der endgültige Befehl aktualisiert die VMSS-VM mit hinzugefügtem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="b803c-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="b803c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b803c-113">PARAMETERS</span></span>

### <span data-ttu-id="b803c-114">-Caching</span><span class="sxs-lookup"><span data-stu-id="b803c-114">-Caching</span></span>
<span data-ttu-id="b803c-115">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b803c-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="b803c-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b803c-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b803c-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b803c-117">ReadOnly</span></span>
- <span data-ttu-id="b803c-118">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b803c-118">ReadWrite</span></span>
- <span data-ttu-id="b803c-119">None der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="b803c-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="b803c-120">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b803c-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="b803c-121">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="b803c-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="b803c-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="b803c-122">-CreateOption</span></span>
<span data-ttu-id="b803c-123">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="b803c-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="b803c-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b803c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b803c-125">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="b803c-125">Attach.</span></span>
<span data-ttu-id="b803c-126">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b803c-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="b803c-127">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="b803c-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="b803c-128">Die *VhdUri* ist alles, was erforderlich ist, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) mitzuteilen, die als Datenträger an den virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b803c-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="b803c-129">Leer.</span><span class="sxs-lookup"><span data-stu-id="b803c-129">Empty.</span></span>
<span data-ttu-id="b803c-130">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b803c-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="b803c-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="b803c-131">FromImage.</span></span>
<span data-ttu-id="b803c-132">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b803c-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="b803c-133">Wenn Sie diese Option angeben, müssen Sie auch den *SourceImageUri* -Parameter angeben, um der Azure-Plattform den Speicherort der VHD mitzuteilen, die als Daten Datenträger angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b803c-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="b803c-134">Der *VhdUri* -Parameter wird als Speicherort verwendet, der angibt, wo die VHD des Daten Datenträgers gespeichert wird, wenn Sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b803c-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="b803c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b803c-135">-DefaultProfile</span></span>
<span data-ttu-id="b803c-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b803c-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b803c-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b803c-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b803c-138">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="b803c-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="b803c-139">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b803c-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="b803c-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b803c-140">-DiskSizeInGB</span></span>
<span data-ttu-id="b803c-141">Gibt die Größe eines leeren Datenträgers an, der an einen virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b803c-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="b803c-142">-LUN</span><span class="sxs-lookup"><span data-stu-id="b803c-142">-Lun</span></span>
<span data-ttu-id="b803c-143">Gibt die logische Einheitsnummer (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="b803c-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="b803c-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b803c-144">-ManagedDiskId</span></span>
<span data-ttu-id="b803c-145">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b803c-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="b803c-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b803c-146">-StorageAccountType</span></span>
<span data-ttu-id="b803c-147">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b803c-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="b803c-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b803c-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="b803c-149">Gibt das VM-Objekt für den lokalen virtuellen Computer an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b803c-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="b803c-150">Sie können das Cmdlet **Get-AzVmssVM** verwenden, um ein VM-Objekt für einen virtuellen Computer-Skalierungs Satz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b803c-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="b803c-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b803c-151">-WriteAccelerator</span></span>
<span data-ttu-id="b803c-152">Gibt an, ob WriteAccelerator auf einem verwalteten Daten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b803c-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="b803c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b803c-153">CommonParameters</span></span>
<span data-ttu-id="b803c-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b803c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b803c-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b803c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b803c-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b803c-156">INPUTS</span></span>

### <span data-ttu-id="b803c-157">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b803c-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="b803c-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b803c-158">System.Int32</span></span>

### <span data-ttu-id="b803c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="b803c-159">System.String</span></span>

### <span data-ttu-id="b803c-160">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="b803c-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="b803c-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b803c-161">OUTPUTS</span></span>

### <span data-ttu-id="b803c-162">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b803c-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b803c-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="b803c-163">NOTES</span></span>

## <span data-ttu-id="b803c-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b803c-164">RELATED LINKS</span></span>
