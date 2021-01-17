---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473150"
---
# <span data-ttu-id="70f9d-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="70f9d-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="70f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="70f9d-103">Fügt einem virtuellen Computer einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="70f9d-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="70f9d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70f9d-104">SYNTAX</span></span>

### <span data-ttu-id="70f9d-105">VmNormalDiskParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="70f9d-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70f9d-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="70f9d-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70f9d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70f9d-107">DESCRIPTION</span></span>
<span data-ttu-id="70f9d-108">Das **Cmdlet "Add-AzVMDataDisk"** fügt einem virtuellen Computer einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="70f9d-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="70f9d-109">Sie können einen Datenträger hinzufügen, wenn Sie einen virtuellen Computer erstellen, oder Sie können einem vorhandenen virtuellen Computer einen Datenträger hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="70f9d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70f9d-110">EXAMPLES</span></span>

### <span data-ttu-id="70f9d-111">Beispiel 1: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="70f9d-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="70f9d-112">Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="70f9d-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70f9d-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="70f9d-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="70f9d-114">Mit den nächsten drei Befehlen werden den Variablen $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 Pfade von drei Datenträgern zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="70f9d-115">Dieser Ansatz ist nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="70f9d-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="70f9d-116">Mit den letzten drei Befehlen wird dem virtuellen Computer, der auf dem Computer gespeichert ist, jeweils ein Datenträger $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70f9d-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70f9d-117">Der Befehl gibt den Namen und Speicherort des Datenträgers sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="70f9d-118">Der URI der einzelnen Datenträger wird in $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70f9d-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="70f9d-119">Beispiel 2: Hinzufügen eines Datenträgers zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="70f9d-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="70f9d-120">Der erste Befehl ruft den virtuellen Computer "VirtualMachine07" mithilfe des [Get-AzVM-Cmdlets](./Get-AzVM.md) ab.</span><span class="sxs-lookup"><span data-stu-id="70f9d-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="70f9d-121">Der Befehl speichert den virtuellen Computer in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="70f9d-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70f9d-122">Der zweite Befehl fügt dem virtuellen Computer, der auf der Festplatte gespeichert ist, einen $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70f9d-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70f9d-123">Der letzte Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="70f9d-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="70f9d-124">Beispiel 3: Hinzufügen eines Datenträgers zu einem neuen virtuellen Computer aus einem generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="70f9d-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="70f9d-125">Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="70f9d-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70f9d-126">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="70f9d-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="70f9d-127">Mit den nächsten beiden Befehlen werden Pfade für das Datenbild und die Datenträger den $DataImageUri und $DataDiskUri Zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="70f9d-128">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="70f9d-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="70f9d-129">Mit den endgültigen Befehlen wird dem virtuellen Computer, der auf dem Computer gespeichert ist, ein Datenträger $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70f9d-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70f9d-130">Der Befehl gibt den Namen und speicherort für den Datenträger und andere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="70f9d-131">Beispiel 4: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="70f9d-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="70f9d-132">Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="70f9d-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="70f9d-133">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="70f9d-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="70f9d-134">Mit den nächsten Befehlen werden pfade des Datenträgers zur $DataDiskUri zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="70f9d-135">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="70f9d-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="70f9d-136">Mit dem letzten Befehl wird dem virtuellen Computer, der auf dem Computer gespeichert ist, ein $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="70f9d-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="70f9d-137">Der Befehl gibt den Namen und Speicherort des Datenträgers sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="70f9d-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70f9d-138">PARAMETERS</span></span>

### <span data-ttu-id="70f9d-139">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="70f9d-139">-Caching</span></span>
<span data-ttu-id="70f9d-140">Gibt den Cachemodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="70f9d-141">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="70f9d-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70f9d-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="70f9d-142">ReadOnly</span></span>
- <span data-ttu-id="70f9d-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="70f9d-143">ReadWrite</span></span>
- <span data-ttu-id="70f9d-144">Keine Der Standardwert ist "ReadWrite".</span><span class="sxs-lookup"><span data-stu-id="70f9d-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="70f9d-145">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="70f9d-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="70f9d-146">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="70f9d-146">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="70f9d-147">-CreateOption</span></span>
<span data-ttu-id="70f9d-148">Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="70f9d-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="70f9d-149">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="70f9d-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="70f9d-150">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-150">Attach.</span></span>
<span data-ttu-id="70f9d-151">Geben Sie diese Option an, um einen virtuellen Computer von einem speziellen Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="70f9d-152">Wenn Sie diese Option angeben, geben Sie nicht den *Parameter "SourceImageUri"* an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="70f9d-153">Der *VhdUri* ist alles, was benötigt wird, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) zu mitteilen, die als Datenträger an den virtuellen Computer anfügen soll.</span><span class="sxs-lookup"><span data-stu-id="70f9d-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="70f9d-154">Leer.</span><span class="sxs-lookup"><span data-stu-id="70f9d-154">Empty.</span></span>
<span data-ttu-id="70f9d-155">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="70f9d-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="70f9d-156">FromImage.</span></span>
<span data-ttu-id="70f9d-157">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="70f9d-158">Wenn Sie diese Option angeben, müssen Sie auch den *Parameter "SourceImageUri"* angeben, um der Azure-Plattform den Speicherort der VHD anzugeben, die als Datenträger anfügen werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f9d-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="70f9d-159">Der *Parameter "VhdUri"* wird als Speicherort verwendet, an dem die Festplatte VHD gespeichert wird, wenn sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70f9d-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70f9d-160">-DefaultProfile</span></span>
<span data-ttu-id="70f9d-161">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70f9d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70f9d-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="70f9d-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="70f9d-163">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="70f9d-164">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="70f9d-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="70f9d-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="70f9d-165">-DiskSizeInGB</span></span>
<span data-ttu-id="70f9d-166">Gibt die Größe (in Gigabyte) eines leeren Datenträgers an, der an einen virtuellen Computer anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="70f9d-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="70f9d-167">-Lun</span></span>
<span data-ttu-id="70f9d-168">Gibt die Logische Einheitennummer (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="70f9d-169">-ManagedDiskId</span></span>
<span data-ttu-id="70f9d-170">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-171">-Name</span><span class="sxs-lookup"><span data-stu-id="70f9d-171">-Name</span></span>
<span data-ttu-id="70f9d-172">Gibt den Namen des hinzuzufügenden Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="70f9d-173">-SourceImageUri</span></span>
<span data-ttu-id="70f9d-174">Gibt den Quell-URI des Datenträgers an, den dieses Cmdlet anfügen soll.</span><span class="sxs-lookup"><span data-stu-id="70f9d-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="70f9d-175">-StorageAccountType</span></span>
<span data-ttu-id="70f9d-176">Gibt den Speicherkontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="70f9d-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="70f9d-177">-VhdUri</span></span>
<span data-ttu-id="70f9d-178">Gibt den URI (Uniform Resource Identifier) für die virtuelle Festplattendatei (VHD) an, die erstellt wird, wenn ein Plattformbild oder ein Benutzerbild verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70f9d-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="70f9d-179">Dieses Cmdlet kopiert das große Binärobjekt (BLOB) des Bilds an diesen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="70f9d-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="70f9d-180">Dies ist der Ort, an dem der virtuelle Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="70f9d-180">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-181">-VM</span><span class="sxs-lookup"><span data-stu-id="70f9d-181">-VM</span></span>
<span data-ttu-id="70f9d-182">Gibt das Objekt des lokalen virtuellen Computers an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f9d-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="70f9d-183">Sie können das **Get-AzVM-Cmdlet** verwenden, um ein Objekt des virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="70f9d-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="70f9d-184">Sie können das **Cmdlet "New-AzVMConfig"** verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70f9d-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="70f9d-185">-WriteAccelerator</span></span>
<span data-ttu-id="70f9d-186">Gibt an, ob WriteAccelerator auf einem verwalteten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f9d-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70f9d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70f9d-187">CommonParameters</span></span>
<span data-ttu-id="70f9d-188">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70f9d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70f9d-189">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70f9d-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70f9d-190">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70f9d-190">INPUTS</span></span>

### <span data-ttu-id="70f9d-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="70f9d-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="70f9d-192">System.String</span><span class="sxs-lookup"><span data-stu-id="70f9d-192">System.String</span></span>

### <span data-ttu-id="70f9d-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="70f9d-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="70f9d-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="70f9d-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="70f9d-195">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70f9d-195">OUTPUTS</span></span>

### <span data-ttu-id="70f9d-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="70f9d-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="70f9d-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="70f9d-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="70f9d-198">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70f9d-198">NOTES</span></span>

## <span data-ttu-id="70f9d-199">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70f9d-199">RELATED LINKS</span></span>

[<span data-ttu-id="70f9d-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="70f9d-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="70f9d-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="70f9d-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="70f9d-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="70f9d-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
