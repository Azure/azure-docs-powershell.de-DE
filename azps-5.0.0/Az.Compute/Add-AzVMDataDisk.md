---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300363"
---
# <span data-ttu-id="b2026-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b2026-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="b2026-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2026-102">SYNOPSIS</span></span>
<span data-ttu-id="b2026-103">Fügt einen Daten Datenträger zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2026-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="b2026-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2026-104">SYNTAX</span></span>

### <span data-ttu-id="b2026-105">VmNormalDiskParameterSetName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2026-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2026-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b2026-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2026-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2026-107">DESCRIPTION</span></span>
<span data-ttu-id="b2026-108">Mit dem Cmdlet **Add-AzVMDataDisk** wird ein Daten Datenträger zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b2026-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="b2026-109">Sie können einen Datenträger hinzufügen, wenn Sie einen virtuellen Computer erstellen, oder Sie können einen Daten Datenträger zu einem vorhandenen virtuellen Computer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b2026-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="b2026-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2026-110">EXAMPLES</span></span>

### <span data-ttu-id="b2026-111">Beispiel 1: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b2026-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="b2026-112">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2026-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b2026-113">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="b2026-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b2026-114">Die nächsten drei Befehle weisen den $DataDiskVhdUri 01-, $DataDiskVhdUri 02-und $DataDiskVhdUri 03-Variablen Pfade mit drei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="b2026-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="b2026-115">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="b2026-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b2026-116">Die letzten drei Befehle fügen jeweils einen Datenträger zum virtuellen Computer hinzu, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b2026-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b2026-117">Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="b2026-118">Der URI jedes Datenträgers wird in $DataDiskVhdUri 01, $DataDiskVhdUri 02 und $DataDiskVhdUri 03 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b2026-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="b2026-119">Beispiel 2: Hinzufügen eines Datenlaufwerks zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="b2026-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b2026-120">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 mit dem Cmdlet [Get-AzVM](./Get-AzVM.md) ab.</span><span class="sxs-lookup"><span data-stu-id="b2026-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b2026-121">Der Befehl speichert den virtuellen Computer in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2026-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b2026-122">Der zweite Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2026-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b2026-123">Der endgültige Befehl aktualisiert den Zustand des virtuellen Computers, der in $VirtualMachine in ResourceGroup11 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b2026-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="b2026-124">Beispiel 3: Hinzufügen eines Datenlaufwerks zu einem neuen virtuellen Computer aus einem generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="b2026-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="b2026-125">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2026-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b2026-126">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="b2026-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b2026-127">In den nächsten beiden Befehlen werden den $DataImageUri-und $DataDiskUri Variablen Pfade für das Daten Bild und die Datenlaufwerke zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b2026-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="b2026-128">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="b2026-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b2026-129">Mit den letzten Befehlen wird dem virtuellen Computer, der in $VirtualMachine gespeichert ist, ein Daten Datenträger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b2026-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b2026-130">Der Befehl gibt den Namen und den Speicherort für den Datenträger und andere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="b2026-131">Beispiel 4: Hinzufügen von Datenträgern zu einem neuen virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="b2026-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="b2026-132">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b2026-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b2026-133">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="b2026-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b2026-134">Die nächsten Befehle weisen der $DataDiskUri-Variablen Pfade des Daten Datenträgers zu.</span><span class="sxs-lookup"><span data-stu-id="b2026-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="b2026-135">Dieser Ansatz wird verwendet, um die Lesbarkeit der folgenden Befehle zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="b2026-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b2026-136">Der letzte Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Daten Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="b2026-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b2026-137">Der Befehl gibt den Namen und den Speicherort für den Datenträger sowie weitere Eigenschaften des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="b2026-138">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2026-138">PARAMETERS</span></span>

### <span data-ttu-id="b2026-139">-Caching</span><span class="sxs-lookup"><span data-stu-id="b2026-139">-Caching</span></span>
<span data-ttu-id="b2026-140">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="b2026-141">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2026-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2026-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b2026-142">ReadOnly</span></span>
- <span data-ttu-id="b2026-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b2026-143">ReadWrite</span></span>
- <span data-ttu-id="b2026-144">None der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="b2026-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="b2026-145">Wenn Sie diesen Wert ändern, wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b2026-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="b2026-146">Diese Einstellung wirkt sich auf die Konsistenz und Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="b2026-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="b2026-147">-Createoption</span><span class="sxs-lookup"><span data-stu-id="b2026-147">-CreateOption</span></span>
<span data-ttu-id="b2026-148">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="b2026-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="b2026-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b2026-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b2026-150">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="b2026-150">Attach.</span></span>
<span data-ttu-id="b2026-151">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2026-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="b2026-152">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="b2026-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="b2026-153">Die *VhdUri* ist alles, was erforderlich ist, um der Azure-Plattform den Speicherort der virtuellen Festplatte (VHD) mitzuteilen, die als Datenträger an den virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="b2026-154">Leer.</span><span class="sxs-lookup"><span data-stu-id="b2026-154">Empty.</span></span>
<span data-ttu-id="b2026-155">Geben Sie dies an, um einen leeren Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2026-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="b2026-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="b2026-156">FromImage.</span></span>
<span data-ttu-id="b2026-157">Geben Sie diese Option an, um einen virtuellen Computer aus einem generalisierten Bild oder Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2026-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="b2026-158">Wenn Sie diese Option angeben, müssen Sie auch den *SourceImageUri* -Parameter angeben, um der Azure-Plattform den Speicherort der VHD mitzuteilen, die als Daten Datenträger angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="b2026-159">Der *VhdUri* -Parameter wird als Speicherort verwendet, der angibt, wo die VHD des Daten Datenträgers gespeichert wird, wenn Sie vom virtuellen Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2026-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="b2026-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2026-160">-DefaultProfile</span></span>
<span data-ttu-id="b2026-161">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b2026-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2026-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b2026-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b2026-163">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="b2026-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="b2026-164">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b2026-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="b2026-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b2026-165">-DiskSizeInGB</span></span>
<span data-ttu-id="b2026-166">Gibt die Größe eines leeren Datenträgers an, der an einen virtuellen Computer angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="b2026-167">-LUN</span><span class="sxs-lookup"><span data-stu-id="b2026-167">-Lun</span></span>
<span data-ttu-id="b2026-168">Gibt die logische Einheitsnummer (LUN) für einen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="b2026-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="b2026-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b2026-169">-ManagedDiskId</span></span>
<span data-ttu-id="b2026-170">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="b2026-171">-Name</span><span class="sxs-lookup"><span data-stu-id="b2026-171">-Name</span></span>
<span data-ttu-id="b2026-172">Gibt den Namen des hinzuzufügenden Daten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="b2026-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="b2026-173">-SourceImageUri</span></span>
<span data-ttu-id="b2026-174">Gibt den Quell-URI des Datenträgers an, der von diesem Cmdlet angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b2026-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="b2026-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b2026-175">-StorageAccountType</span></span>
<span data-ttu-id="b2026-176">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="b2026-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="b2026-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b2026-177">-VhdUri</span></span>
<span data-ttu-id="b2026-178">Gibt den Uniform Resource Identifier (URI) für die VHD-Datei (Virtual Hard Disk) an, die beim Verwenden eines Platt Form Bilds oder eines Benutzerbilds erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="b2026-179">Dieses Cmdlet kopiert das BLOB-Objekt (Binary Large Object) an diesen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="b2026-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="b2026-180">Dies ist der Speicherort, an dem der virtuelle Computer gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="b2026-181">-VM</span><span class="sxs-lookup"><span data-stu-id="b2026-181">-VM</span></span>
<span data-ttu-id="b2026-182">Gibt das Objekt des lokalen virtuellen Computers an, dem ein Datenträger hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="b2026-183">Sie können das Cmdlet **Get-AzVM** verwenden, um ein Objekt eines virtuellen Computers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b2026-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="b2026-184">Sie können das Cmdlet **New-AzVMConfig** verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2026-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="b2026-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b2026-185">-WriteAccelerator</span></span>
<span data-ttu-id="b2026-186">Gibt an, ob WriteAccelerator auf einem verwalteten Daten Datenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2026-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="b2026-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2026-187">CommonParameters</span></span>
<span data-ttu-id="b2026-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2026-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2026-189">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2026-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2026-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2026-190">INPUTS</span></span>

### <span data-ttu-id="b2026-191">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b2026-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b2026-192">System. String</span><span class="sxs-lookup"><span data-stu-id="b2026-192">System.String</span></span>

### <span data-ttu-id="b2026-193">Microsoft. Azure. Management. Compute. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="b2026-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="b2026-194">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2026-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b2026-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2026-195">OUTPUTS</span></span>

### <span data-ttu-id="b2026-196">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b2026-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b2026-197">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b2026-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b2026-198">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2026-198">NOTES</span></span>

## <span data-ttu-id="b2026-199">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2026-199">RELATED LINKS</span></span>

[<span data-ttu-id="b2026-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b2026-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="b2026-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b2026-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b2026-202">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b2026-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
