---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478569"
---
# <span data-ttu-id="1b8b7-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="1b8b7-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="1b8b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1b8b7-103">Legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b8b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b8b7-104">SYNTAX</span></span>

### <span data-ttu-id="1b8b7-105">DefaultParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b8b7-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b8b7-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="1b8b7-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b8b7-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b8b7-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="1b8b7-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="1b8b7-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b8b7-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b8b7-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="1b8b7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b8b7-110">DESCRIPTION</span></span>
<span data-ttu-id="1b8b7-111">Das Cmdlet " **Set-AzureRmVMOSDisk** " legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="1b8b7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b8b7-112">EXAMPLES</span></span>

### <span data-ttu-id="1b8b7-113">Beispiel 1: Einrichten von Eigenschaften auf einem virtuellen Computer vom Platt Form Abbild</span><span class="sxs-lookup"><span data-stu-id="1b8b7-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="1b8b7-114">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1b8b7-115">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1b8b7-116">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1b8b7-117">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1b8b7-118">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="1b8b7-119">Beispiel 2: Festlegen von Eigenschaften auf einem virtuellen Computer vom generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="1b8b7-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="1b8b7-120">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1b8b7-121">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1b8b7-122">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1b8b7-123">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1b8b7-124">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="1b8b7-125">Beispiel 3: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="1b8b7-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="1b8b7-126">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="1b8b7-127">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="1b8b7-128">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="1b8b7-129">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="1b8b7-130">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="1b8b7-131">Beispiel 4: Festlegen der Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="1b8b7-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="1b8b7-132">In diesem Beispiel werden die Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="1b8b7-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b8b7-133">PARAMETERS</span></span>

### <span data-ttu-id="1b8b7-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="1b8b7-134">-Caching</span></span>
<span data-ttu-id="1b8b7-135">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="1b8b7-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1b8b7-136">Valid values are:</span></span> 

- <span data-ttu-id="1b8b7-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1b8b7-137">ReadOnly</span></span>
- <span data-ttu-id="1b8b7-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1b8b7-138">ReadWrite</span></span>

<span data-ttu-id="1b8b7-139">Der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="1b8b7-140">Durch Ändern des Caching-Werts wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="1b8b7-141">Diese Einstellung wirkt sich auf die Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-141">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="1b8b7-142">-Createoption</span><span class="sxs-lookup"><span data-stu-id="1b8b7-142">-CreateOption</span></span>
<span data-ttu-id="1b8b7-143">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="1b8b7-144">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1b8b7-144">Valid values are:</span></span> 

- <span data-ttu-id="1b8b7-145">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-145">Attach.</span></span>
<span data-ttu-id="1b8b7-146">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="1b8b7-147">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="1b8b7-148">Verwenden Sie stattdessen das Set-AzureRmVMSourceImage-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="1b8b7-149">Sie müssen auch die *Windows* -oder *Linux* -Parameter verwenden, um der azure2-Plattform den Typ des Betriebssystems auf der VHD mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="1b8b7-150">Der *VhdUri* -Parameter genügt, um der azure2-Plattform den Speicherort des anzufügenden Datenträgers mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="1b8b7-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-151">FromImage.</span></span>
<span data-ttu-id="1b8b7-152">Geben Sie diese Option an, um einen virtuellen Computer aus einem Platt Form Bild oder einem generalisierten Benutzerbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="1b8b7-153">Im Fall eines generalisierten Benutzerbilds müssen Sie auch den *SourceImageUri* -Parameter und entweder die *Windows* -oder *Linux* -Parameter angeben, um der Azure-Plattform den Speicherort und den Typ der VHD des Betriebssystems festzulegen, anstatt das Cmdlet " **AzureRmVMSourceImage** " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="1b8b7-154">Im Fall eines Platt Form Bilds genügt der *VhdUri* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="1b8b7-155">Leer.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="1b8b7-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="1b8b7-157">Gibt den Speicherort des Datenträger Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1b8b7-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="1b8b7-159">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Datenträgerverschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1b8b7-160">-DiskSizeInGB</span></span>
<span data-ttu-id="1b8b7-161">Gibt die Größe des Betriebssystemdatenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="1b8b7-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="1b8b7-163">Gibt den Speicherort des Schlüssel Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1b8b7-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="1b8b7-165">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Schlüssel Verschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="1b8b7-166">-Linux</span></span>
<span data-ttu-id="1b8b7-167">Gibt an, dass das Betriebssystem des Benutzer Abbilds Linux ist.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="1b8b7-168">Geben Sie diesen Parameter für die Bereitstellung von auf dem Bild basierenden Benutzern an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="1b8b7-169">-ManagedDiskId</span></span>
<span data-ttu-id="1b8b7-170">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-171">-Name</span><span class="sxs-lookup"><span data-stu-id="1b8b7-171">-Name</span></span>
<span data-ttu-id="1b8b7-172">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="1b8b7-173">-SourceImageUri</span></span>
<span data-ttu-id="1b8b7-174">Gibt den URI der VHD für Benutzerbild Szenarien an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1b8b7-175">-StorageAccountType</span></span>
<span data-ttu-id="1b8b7-176">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="1b8b7-177">-VhdUri</span></span>
<span data-ttu-id="1b8b7-178">Gibt den Uniform Resource Identifier (URI) einer virtuellen Festplatte (VHD) an.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="1b8b7-179">Bei einem bildbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die erstellt werden soll, wenn ein Platt Form Bild oder Benutzerbild angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="1b8b7-180">Hierbei handelt es sich um den Speicherort, an dem das BLOB (Image Binary Large Object) kopiert wird, um den virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="1b8b7-181">Bei einem Startszenario für einen datenträgerbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die vom virtuellen Computer zum Starten direkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-182">-VM</span><span class="sxs-lookup"><span data-stu-id="1b8b7-182">-VM</span></span>
<span data-ttu-id="1b8b7-183">Gibt das Objekt des lokalen virtuellen Computers an, auf dem die Datenträgereigenschaften des Betriebssystems festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="1b8b7-184">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="1b8b7-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="1b8b7-185">-Windows</span></span>
<span data-ttu-id="1b8b7-186">Gibt an, dass das Betriebssystem des Benutzer Abbilds Windows ist.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b8b7-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b8b7-187">CommonParameters</span></span>
<span data-ttu-id="1b8b7-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b8b7-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b8b7-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b8b7-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b8b7-190">INPUTS</span></span>

### <span data-ttu-id="1b8b7-191">Keine</span><span class="sxs-lookup"><span data-stu-id="1b8b7-191">None</span></span>
<span data-ttu-id="1b8b7-192">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1b8b7-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b8b7-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b8b7-193">OUTPUTS</span></span>

## <span data-ttu-id="1b8b7-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b8b7-194">NOTES</span></span>

## <span data-ttu-id="1b8b7-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b8b7-195">RELATED LINKS</span></span>

[<span data-ttu-id="1b8b7-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1b8b7-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="1b8b7-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1b8b7-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1b8b7-198">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="1b8b7-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


