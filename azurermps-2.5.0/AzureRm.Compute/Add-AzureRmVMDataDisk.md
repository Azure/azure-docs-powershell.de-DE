---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: d644f0bdb770ec1c6b26656cb7bf8709ee369a05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849784"
---
# <span data-ttu-id="d342b-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d342b-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="d342b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d342b-102">SYNOPSIS</span></span>
<span data-ttu-id="d342b-103">Fügt einen Daten Datenträger zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="d342b-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d342b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d342b-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d342b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d342b-105">DESCRIPTION</span></span>
<span data-ttu-id="d342b-106">Mit dem Cmdlet **Add-AzureRmVMDataDisk** wird ein Daten Datenträger zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d342b-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="d342b-107">Sie können einen Datenträger hinzufügen, wenn Sie einen virtuellen Computer erstellen, oder Sie können einen Daten Datenträger zu einem vorhandenen virtuellen Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d342b-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="d342b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d342b-108">EXAMPLES</span></span>

### <span data-ttu-id="d342b-109">Beispiel 1: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d342b-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="d342b-110">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d342b-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d342b-111">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="d342b-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d342b-112">Die nächsten drei Befehle weisen den $DataDiskVhdUri 01-, $DataDiskVhdUri 02-und $DataDiskVhdUri 03-Variablen Pfade mit drei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="d342b-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="d342b-113">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="d342b-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="d342b-114">Die letzten drei Befehle fügen jeweils einen Datenträger zum virtuellen Computer hinzu, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d342b-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d342b-115">Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="d342b-116">Der URI jedes Datenträgers wird in $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d342b-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="d342b-117">Beispiel 2: Hinzufügen eines Datenlaufwerks zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="d342b-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d342b-118">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) ab.</span><span class="sxs-lookup"><span data-stu-id="d342b-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="d342b-119">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d342b-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="d342b-120">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="d342b-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="d342b-121">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d342b-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="d342b-122">Beispiel 3: Hinzufügen eines Datenlaufwerks zu einem neuen virtuellen Computer aus einem generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="d342b-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="d342b-123">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d342b-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d342b-124">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="d342b-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d342b-125">In den nächsten beiden Befehlen werden den $DataImageUri-und $DataDiskUri Variablen Pfade für das Daten Bild und die Datenlaufwerke zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d342b-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="d342b-126">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d342b-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="d342b-127">Mit den letzten Befehlen wird dem virtuellen Computer, der in $VirtualMachine gespeichert ist, ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d342b-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d342b-128">Der Befehl gibt den Namen und den Speicherort für den Datenträger und andere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="d342b-129">Beispiel 4: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="d342b-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="d342b-130">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d342b-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d342b-131">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="d342b-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="d342b-132">Die nächsten Befehle weisen der $DataDiskUri-Variablen Pfade des Daten Datenträgers zu.</span><span class="sxs-lookup"><span data-stu-id="d342b-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="d342b-133">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="d342b-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="d342b-134">Der letzte Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="d342b-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d342b-135">Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="d342b-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="d342b-136">PARAMETERS</span></span>

### <span data-ttu-id="d342b-137">-Caching</span><span class="sxs-lookup"><span data-stu-id="d342b-137">-Caching</span></span>
<span data-ttu-id="d342b-138">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="d342b-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d342b-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d342b-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d342b-140">ReadOnly</span></span>
- <span data-ttu-id="d342b-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d342b-141">ReadWrite</span></span>
- <span data-ttu-id="d342b-142">Keine</span><span class="sxs-lookup"><span data-stu-id="d342b-142">None</span></span>

<span data-ttu-id="d342b-143">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d342b-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="d342b-144">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d342b-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="d342b-145">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="d342b-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-146">-Createoption</span><span class="sxs-lookup"><span data-stu-id="d342b-146">-CreateOption</span></span>
<span data-ttu-id="d342b-147">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="d342b-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="d342b-148">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d342b-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d342b-149">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="d342b-149">Attach.</span></span>
<span data-ttu-id="d342b-150">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d342b-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="d342b-151">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="d342b-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="d342b-152">Die *VhdUri* ist alles, was erforderlich ist, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) mitzuteilen, die als Datenträger an den virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="d342b-153">Leer.</span><span class="sxs-lookup"><span data-stu-id="d342b-153">Empty.</span></span>
<span data-ttu-id="d342b-154">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d342b-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="d342b-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="d342b-155">FromImage.</span></span>
<span data-ttu-id="d342b-156">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d342b-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="d342b-157">Wenn Sie diese Option angeben, müssen Sie auch den *SourceImageUri* -Parameter angeben, um der Azure-Plattform den Speicherort der VHD mitzuteilen, die als Daten Datenträger angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="d342b-158">Der *VhdUri* -Parameter wird als Speicherort verwendet, der angibt, wo die VHD des Daten Datenträgers gespeichert wird, wenn Sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d342b-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d342b-159">-DefaultProfile</span></span>
<span data-ttu-id="d342b-160">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d342b-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d342b-161">-DiskSizeInGB</span></span>
<span data-ttu-id="d342b-162">Gibt die Größe eines leeren Datenträgers an, der an einen virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-163">-LUN</span><span class="sxs-lookup"><span data-stu-id="d342b-163">-Lun</span></span>
<span data-ttu-id="d342b-164">Gibt die logische Einheitsnummer (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="d342b-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-165">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d342b-165">-ManagedDiskId</span></span>
<span data-ttu-id="d342b-166">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-166">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-167">-Name</span><span class="sxs-lookup"><span data-stu-id="d342b-167">-Name</span></span>
<span data-ttu-id="d342b-168">Gibt den Namen des hinzuzufügenden Daten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-168">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-169">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="d342b-169">-SourceImageUri</span></span>
<span data-ttu-id="d342b-170">Gibt den Quell-URI des Datenträgers an, der von diesem Cmdlet angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d342b-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d342b-171">-StorageAccountType</span></span>
<span data-ttu-id="d342b-172">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="d342b-172">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d342b-173">-VhdUri</span></span>
<span data-ttu-id="d342b-174">Gibt den Uniform Resource Identifier (URI) für die VHD-Datei (Virtual Hard Disk) an, die beim Verwenden eines Platt Form Bilds oder eines Benutzerbilds erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="d342b-175">Dieses Cmdlet kopiert das BLOB-Objekt (Binary Large Object) an diesen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d342b-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="d342b-176">Dies ist der Speicherort, an dem der virtuelle Computer gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-176">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-177">-VM</span><span class="sxs-lookup"><span data-stu-id="d342b-177">-VM</span></span>
<span data-ttu-id="d342b-178">Gibt das Objekt des lokalen virtuellen Computers an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="d342b-179">Sie können das Cmdlet **Get-AzureRmVM** verwenden, um ein Objekt eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d342b-179">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="d342b-180">Sie können das Cmdlet **New-AzureRmVMConfig** verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d342b-180">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="d342b-181">-WriteAccelerator</span></span>
<span data-ttu-id="d342b-182">Gibt an, ob WriteAccelerator auf dem Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d342b-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d342b-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d342b-183">CommonParameters</span></span>
<span data-ttu-id="d342b-184">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d342b-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d342b-185">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d342b-185">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d342b-186">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d342b-186">INPUTS</span></span>

### <span data-ttu-id="d342b-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d342b-187">PSVirtualMachine</span></span>
<span data-ttu-id="d342b-188">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d342b-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d342b-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d342b-189">OUTPUTS</span></span>

### <span data-ttu-id="d342b-190">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d342b-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d342b-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="d342b-191">NOTES</span></span>

## <span data-ttu-id="d342b-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d342b-192">RELATED LINKS</span></span>

[<span data-ttu-id="d342b-193">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d342b-193">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="d342b-194">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d342b-194">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="d342b-195">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="d342b-195">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
