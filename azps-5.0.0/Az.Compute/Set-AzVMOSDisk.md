---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296500"
---
# <span data-ttu-id="a52ef-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="a52ef-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="a52ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a52ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a52ef-103">Legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a52ef-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="a52ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a52ef-104">SYNTAX</span></span>

### <span data-ttu-id="a52ef-105">DefaultParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a52ef-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52ef-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="a52ef-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52ef-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a52ef-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52ef-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="a52ef-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a52ef-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a52ef-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52ef-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a52ef-110">DESCRIPTION</span></span>
<span data-ttu-id="a52ef-111">Das Cmdlet " **Set-AzVMOSDisk** " legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a52ef-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="a52ef-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a52ef-112">EXAMPLES</span></span>

### <span data-ttu-id="a52ef-113">Beispiel 1: Einrichten von Eigenschaften auf einem virtuellen Computer vom Platt Form Abbild</span><span class="sxs-lookup"><span data-stu-id="a52ef-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a52ef-114">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a52ef-115">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a52ef-116">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a52ef-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a52ef-117">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a52ef-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a52ef-118">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="a52ef-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a52ef-119">Beispiel 2: Festlegen von Eigenschaften auf einem virtuellen Computer vom generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="a52ef-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a52ef-120">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a52ef-121">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a52ef-122">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a52ef-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a52ef-123">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a52ef-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a52ef-124">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="a52ef-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a52ef-125">Beispiel 3: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="a52ef-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a52ef-126">Der erste Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet13 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a52ef-127">Der zweite Befehl erstellt ein Objekt eines virtuellen Computers und speichert es in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a52ef-128">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a52ef-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a52ef-129">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a52ef-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a52ef-130">Der endgültige Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine fest.</span><span class="sxs-lookup"><span data-stu-id="a52ef-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a52ef-131">Beispiel 4: Festlegen der Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger</span><span class="sxs-lookup"><span data-stu-id="a52ef-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="a52ef-132">In diesem Beispiel werden die Datenträger Verschlüsselungseinstellungen auf einem virtuellen Computer-Betriebssystemdatenträger festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a52ef-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="a52ef-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="a52ef-133">PARAMETERS</span></span>

### <span data-ttu-id="a52ef-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="a52ef-134">-Caching</span></span>
<span data-ttu-id="a52ef-135">Gibt den Zwischenspeichermodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="a52ef-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a52ef-136">Valid values are:</span></span> 
- <span data-ttu-id="a52ef-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a52ef-137">ReadOnly</span></span>
- <span data-ttu-id="a52ef-138">ReadWrite der Standardwert ist ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a52ef-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="a52ef-139">Durch Ändern des Caching-Werts wird der virtuelle Computer neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="a52ef-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="a52ef-140">Diese Einstellung wirkt sich auf die Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="a52ef-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="a52ef-141">-Createoption</span><span class="sxs-lookup"><span data-stu-id="a52ef-141">-CreateOption</span></span>
<span data-ttu-id="a52ef-142">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="a52ef-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="a52ef-143">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a52ef-143">Valid values are:</span></span> 
- <span data-ttu-id="a52ef-144">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-144">Attach.</span></span>
<span data-ttu-id="a52ef-145">Geben Sie diese Option an, um einen virtuellen Computer von einem spezialisierten Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="a52ef-146">Wenn Sie diese Option angeben, geben Sie den *SourceImageUri* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="a52ef-147">Verwenden Sie stattdessen das Set-AzVMSourceImage-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52ef-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="a52ef-148">Sie müssen auch die *Windows* -oder *Linux* -Parameter verwenden, um der Azure-Plattform den Typ des Betriebssystems auf der virtuellen Festplatte mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="a52ef-149">Der *VhdUri* -Parameter genügt, um der Azure-Plattform den Speicherort des anzufügenden Datenträgers mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="a52ef-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="a52ef-150">FromImage.</span></span>
<span data-ttu-id="a52ef-151">Geben Sie diese Option an, um einen virtuellen Computer aus einem Platt Form Bild oder einem generalisierten Benutzerbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="a52ef-152">Im Fall eines generalisierten Benutzerbilds müssen Sie auch den *SourceImageUri* -Parameter und entweder die *Windows* -oder *Linux* -Parameter angeben, um der Azure-Plattform den Speicherort und den Typ der VHD des Betriebssystems festzulegen, anstatt das Cmdlet " **AzVMSourceImage** " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a52ef-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="a52ef-153">Im Fall eines Platt Form Bilds genügt der *VhdUri* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="a52ef-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="a52ef-154">Leer.</span><span class="sxs-lookup"><span data-stu-id="a52ef-154">Empty.</span></span>

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

### <span data-ttu-id="a52ef-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52ef-155">-DefaultProfile</span></span>
<span data-ttu-id="a52ef-156">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a52ef-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52ef-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="a52ef-157">-DiffDiskSetting</span></span>
<span data-ttu-id="a52ef-158">Gibt die differenzierenden Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="a52ef-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a52ef-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="a52ef-160">Gibt den Speicherort des Datenträger Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="a52ef-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a52ef-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="a52ef-162">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Datenträgerverschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="a52ef-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a52ef-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a52ef-164">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="a52ef-165">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a52ef-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="a52ef-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a52ef-166">-DiskSizeInGB</span></span>
<span data-ttu-id="a52ef-167">Gibt die Größe des Betriebssystemdatenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="a52ef-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a52ef-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a52ef-169">Gibt den Speicherort des Schlüssel Verschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="a52ef-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a52ef-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="a52ef-171">Gibt die Ressourcen-ID des Schlüsseldepots mit dem Schlüssel Verschlüsselungsschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="a52ef-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="a52ef-172">-Linux</span></span>
<span data-ttu-id="a52ef-173">Gibt an, dass das Betriebssystem des Benutzer Abbilds Linux ist.</span><span class="sxs-lookup"><span data-stu-id="a52ef-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="a52ef-174">Geben Sie diesen Parameter für die Bereitstellung von auf dem Bild basierenden Benutzern an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="a52ef-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="a52ef-175">-ManagedDiskId</span></span>
<span data-ttu-id="a52ef-176">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="a52ef-177">-Name</span><span class="sxs-lookup"><span data-stu-id="a52ef-177">-Name</span></span>
<span data-ttu-id="a52ef-178">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="a52ef-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="a52ef-179">-SourceImageUri</span></span>
<span data-ttu-id="a52ef-180">Gibt den URI der VHD für Benutzerbild Szenarien an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="a52ef-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a52ef-181">-StorageAccountType</span></span>
<span data-ttu-id="a52ef-182">Gibt den Speicher Kontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="a52ef-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a52ef-183">-VhdUri</span></span>
<span data-ttu-id="a52ef-184">Gibt den Uniform Resource Identifier (URI) einer virtuellen Festplatte (VHD) an.</span><span class="sxs-lookup"><span data-stu-id="a52ef-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="a52ef-185">Bei einem bildbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die erstellt werden soll, wenn ein Platt Form Bild oder Benutzerbild angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a52ef-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="a52ef-186">Hierbei handelt es sich um den Speicherort, an dem das BLOB (Image Binary Large Object) kopiert wird, um den virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="a52ef-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="a52ef-187">Bei einem Startszenario für einen datenträgerbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die vom virtuellen Computer zum Starten direkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a52ef-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="a52ef-188">-VM</span><span class="sxs-lookup"><span data-stu-id="a52ef-188">-VM</span></span>
<span data-ttu-id="a52ef-189">Gibt das Objekt des lokalen virtuellen Computers an, auf dem die Datenträgereigenschaften des Betriebssystems festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a52ef-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="a52ef-190">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a52ef-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="a52ef-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="a52ef-191">-Windows</span></span>
<span data-ttu-id="a52ef-192">Gibt an, dass das Betriebssystem des Benutzer Abbilds Windows ist.</span><span class="sxs-lookup"><span data-stu-id="a52ef-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="a52ef-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="a52ef-193">-WriteAccelerator</span></span>
<span data-ttu-id="a52ef-194">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a52ef-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="a52ef-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52ef-195">CommonParameters</span></span>
<span data-ttu-id="a52ef-196">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52ef-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52ef-197">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a52ef-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52ef-198">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a52ef-198">INPUTS</span></span>

### <span data-ttu-id="a52ef-199">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a52ef-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a52ef-200">System. String</span><span class="sxs-lookup"><span data-stu-id="a52ef-200">System.String</span></span>

## <span data-ttu-id="a52ef-201">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a52ef-201">OUTPUTS</span></span>

### <span data-ttu-id="a52ef-202">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a52ef-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a52ef-203">Notizen</span><span class="sxs-lookup"><span data-stu-id="a52ef-203">NOTES</span></span>

## <span data-ttu-id="a52ef-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a52ef-204">RELATED LINKS</span></span>

[<span data-ttu-id="a52ef-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a52ef-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a52ef-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a52ef-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a52ef-207">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a52ef-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


