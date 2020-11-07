---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: ff6945369f16e9c7996ab9be80dcefce759926a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661432"
---
# <span data-ttu-id="ddd70-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="ddd70-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="ddd70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddd70-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd70-103">Legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ddd70-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="ddd70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd70-104">SYNTAX</span></span>

### <span data-ttu-id="ddd70-105">DefaultParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ddd70-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd70-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="ddd70-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd70-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd70-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd70-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="ddd70-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd70-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd70-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd70-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddd70-110">DESCRIPTION</span></span>
<span data-ttu-id="ddd70-111">Das Cmdlet " **Set-AzVMOSDisk** " legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ddd70-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="ddd70-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddd70-112">EXAMPLES</span></span>

### <span data-ttu-id="ddd70-113">Beispiel 1: Einrichten von Eigenschaften auf einem virtuellen Computer vom Platt Form Abbild</span><span class="sxs-lookup"><span data-stu-id="ddd70-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="ddd70-114">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ddd70-115">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ddd70-116">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="ddd70-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ddd70-117">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ddd70-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ddd70-118">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="ddd70-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="ddd70-119">Beispiel 2: Festlegen von Eigenschaften auf einem virtuellen Computer vom generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="ddd70-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="ddd70-120">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ddd70-121">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ddd70-122">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="ddd70-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ddd70-123">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ddd70-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ddd70-124">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="ddd70-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="ddd70-125">Beispiel 3: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="ddd70-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="ddd70-126">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="ddd70-127">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ddd70-128">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="ddd70-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ddd70-129">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ddd70-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="ddd70-130">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="ddd70-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="ddd70-131">Beispiel 4: Festlegen der Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="ddd70-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="ddd70-132">In diesem Beispiel werden die Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ddd70-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="ddd70-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddd70-133">PARAMETERS</span></span>

### <span data-ttu-id="ddd70-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="ddd70-134">-Caching</span></span>
<span data-ttu-id="ddd70-135">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="ddd70-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ddd70-136">Valid values are:</span></span> 
- <span data-ttu-id="ddd70-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ddd70-137">ReadOnly</span></span>
- <span data-ttu-id="ddd70-138">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ddd70-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="ddd70-139">Durch Ändern des Caching-Werts wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ddd70-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="ddd70-140">Diese Einstellung wirkt sich auf die Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="ddd70-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-141">-Createoption</span><span class="sxs-lookup"><span data-stu-id="ddd70-141">-CreateOption</span></span>
<span data-ttu-id="ddd70-142">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="ddd70-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="ddd70-143">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ddd70-143">Valid values are:</span></span> 
- <span data-ttu-id="ddd70-144">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-144">Attach.</span></span>
<span data-ttu-id="ddd70-145">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="ddd70-146">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="ddd70-147">Verwenden Sie stattdessen das Set-AzVMSourceImage-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd70-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="ddd70-148">Sie müssen auch die *Windows* -oder *Linux* -Parameter verwenden, um der Azure-Plattform den Typ des Betriebssystems auf der virtuellen Festplatte mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="ddd70-149">Der *VhdUri* -Parameter genügt, um der Azure-Plattform den Speicherort des anzufügenden Datenträgers mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="ddd70-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="ddd70-150">FromImage.</span></span>
<span data-ttu-id="ddd70-151">Geben Sie diese Option an, um einen virtuellen Computer aus einem Platt Form Bild oder einem generalisierten Benutzerbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="ddd70-152">Im Fall eines generalisierten Benutzerbilds müssen Sie auch den *SourceImageUri* -Parameter und entweder die *Windows* -oder *Linux* -Parameter angeben, um der Azure-Plattform den Speicherort und den Typ der VHD des Betriebssystems festzulegen, anstatt das Cmdlet " **AzVMSourceImage** " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddd70-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="ddd70-153">Im Fall eines Platt Form Bilds genügt der *VhdUri* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ddd70-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="ddd70-154">Leer.</span><span class="sxs-lookup"><span data-stu-id="ddd70-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd70-155">-DefaultProfile</span></span>
<span data-ttu-id="ddd70-156">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ddd70-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd70-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="ddd70-157">-DiffDiskSetting</span></span>
<span data-ttu-id="ddd70-158">Gibt die differenzierenden Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="ddd70-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ddd70-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="ddd70-160">Gibt den Speicherort des Datenträger Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ddd70-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="ddd70-162">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Datenträgerverschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ddd70-163">-DiskSizeInGB</span></span>
<span data-ttu-id="ddd70-164">Gibt die Größe des Betriebssystemdatenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-164">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ddd70-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ddd70-166">Gibt den Speicherort des Schlüssel Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-166">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ddd70-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="ddd70-168">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Schlüssel Verschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="ddd70-169">-Linux</span></span>
<span data-ttu-id="ddd70-170">Gibt an, dass das Betriebssystem des Benutzer Abbilds Linux ist.</span><span class="sxs-lookup"><span data-stu-id="ddd70-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="ddd70-171">Geben Sie diesen Parameter für die Bereitstellung von auf dem Bild basierenden Benutzern an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-171">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ddd70-172">-ManagedDiskId</span></span>
<span data-ttu-id="ddd70-173">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="ddd70-174">-Name</span><span class="sxs-lookup"><span data-stu-id="ddd70-174">-Name</span></span>
<span data-ttu-id="ddd70-175">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-175">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="ddd70-176">-SourceImageUri</span></span>
<span data-ttu-id="ddd70-177">Gibt den URI der VHD für Benutzerbild Szenarien an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-177">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ddd70-178">-StorageAccountType</span></span>
<span data-ttu-id="ddd70-179">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="ddd70-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="ddd70-180">-VhdUri</span></span>
<span data-ttu-id="ddd70-181">Gibt den Uniform Resource Identifier (URI) einer virtuellen Festplatte (VHD) an.</span><span class="sxs-lookup"><span data-stu-id="ddd70-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="ddd70-182">Bei einem bildbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die erstellt werden soll, wenn ein Platt Form Bild oder Benutzerbild angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ddd70-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="ddd70-183">Hierbei handelt es sich um den Speicherort, an dem das BLOB (Image Binary Large Object) kopiert wird, um den virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="ddd70-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="ddd70-184">Bei einem Startszenario für einen datenträgerbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die vom virtuellen Computer zum Starten direkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ddd70-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-185">-VM</span><span class="sxs-lookup"><span data-stu-id="ddd70-185">-VM</span></span>
<span data-ttu-id="ddd70-186">Gibt das Objekt des lokalen virtuellen Computers an, auf dem die Datenträgereigenschaften des Betriebssystems festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ddd70-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="ddd70-187">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ddd70-187">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="ddd70-188">-Windows</span></span>
<span data-ttu-id="ddd70-189">Gibt an, dass das Betriebssystem des Benutzer Abbilds Windows ist.</span><span class="sxs-lookup"><span data-stu-id="ddd70-189">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd70-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ddd70-190">-WriteAccelerator</span></span>
<span data-ttu-id="ddd70-191">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddd70-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="ddd70-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd70-192">CommonParameters</span></span>
<span data-ttu-id="ddd70-193">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd70-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd70-194">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd70-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd70-195">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddd70-195">INPUTS</span></span>

### <span data-ttu-id="ddd70-196">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ddd70-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ddd70-197">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd70-197">System.String</span></span>

## <span data-ttu-id="ddd70-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddd70-198">OUTPUTS</span></span>

### <span data-ttu-id="ddd70-199">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ddd70-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ddd70-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddd70-200">NOTES</span></span>

## <span data-ttu-id="ddd70-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddd70-201">RELATED LINKS</span></span>

[<span data-ttu-id="ddd70-202">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ddd70-202">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ddd70-203">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ddd70-203">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="ddd70-204">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ddd70-204">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


