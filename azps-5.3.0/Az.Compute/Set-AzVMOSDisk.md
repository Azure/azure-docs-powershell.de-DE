---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472944"
---
# <span data-ttu-id="4f37e-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="4f37e-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="4f37e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f37e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f37e-103">Legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4f37e-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="4f37e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f37e-104">SYNTAX</span></span>

### <span data-ttu-id="4f37e-105">DefaultParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f37e-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f37e-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="4f37e-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f37e-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f37e-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f37e-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="4f37e-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f37e-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f37e-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f37e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f37e-110">DESCRIPTION</span></span>
<span data-ttu-id="4f37e-111">Das **Cmdlet Set-AzVMOSDisk** legt die Datenträgereigenschaften des Betriebssystems auf einem virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4f37e-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="4f37e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f37e-112">EXAMPLES</span></span>

### <span data-ttu-id="4f37e-113">Beispiel 1: Festlegen von Eigenschaften auf einem virtuellen Computer über ein Plattformbild</span><span class="sxs-lookup"><span data-stu-id="4f37e-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4f37e-114">Der erste Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet13" in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4f37e-115">Der zweite Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4f37e-116">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4f37e-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4f37e-117">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4f37e-118">Der letzte Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f37e-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4f37e-119">Beispiel 2: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem generalisierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="4f37e-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4f37e-120">Der erste Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet13" in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab und speichert dieses Objekt in der $AvailabilitySet Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4f37e-121">Der zweite Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4f37e-122">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4f37e-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4f37e-123">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4f37e-124">Der letzte Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f37e-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4f37e-125">Beispiel 3: Festlegen von Eigenschaften auf einem virtuellen Computer aus einem speziellen Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="4f37e-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="4f37e-126">Der erste Befehl ruft den Verfügbarkeitssatz namens "AvailabilitySet13" in der Ressourcengruppe mit dem Namen "ResourceGroup11" ab und speichert dieses Objekt in der $AvailabilitySet Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4f37e-127">Der zweite Befehl erstellt ein Objekt des virtuellen Computers und speichert es in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4f37e-128">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4f37e-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4f37e-129">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der in $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4f37e-130">Der letzte Befehl legt die Eigenschaften auf dem virtuellen Computer in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4f37e-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="4f37e-131">Beispiel 4: Festlegen der Einstellungen für die Datenträgerverschlüsselung auf einem Betriebssystemdatenträger eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="4f37e-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="4f37e-132">In diesem Beispiel werden die Einstellungen für die Datenträgerverschlüsselung auf dem Datenträger des Betriebssystems eines virtuellen Computers festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f37e-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="4f37e-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f37e-133">PARAMETERS</span></span>

### <span data-ttu-id="4f37e-134">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="4f37e-134">-Caching</span></span>
<span data-ttu-id="4f37e-135">Gibt den Cachemodus des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="4f37e-136">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4f37e-136">Valid values are:</span></span> 
- <span data-ttu-id="4f37e-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4f37e-137">ReadOnly</span></span>
- <span data-ttu-id="4f37e-138">ReadWrite Der Standardwert ist "ReadWrite".</span><span class="sxs-lookup"><span data-stu-id="4f37e-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="4f37e-139">Eine Änderung des Zwischenspeicherungswerts führt zum Neustart des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4f37e-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="4f37e-140">Diese Einstellung wirkt sich auf die Leistung des Datenträgers aus.</span><span class="sxs-lookup"><span data-stu-id="4f37e-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="4f37e-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4f37e-141">-CreateOption</span></span>
<span data-ttu-id="4f37e-142">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerbild erstellt oder einen vorhandenen Datenträger anfügen soll.</span><span class="sxs-lookup"><span data-stu-id="4f37e-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="4f37e-143">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4f37e-143">Valid values are:</span></span> 
- <span data-ttu-id="4f37e-144">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="4f37e-144">Attach.</span></span>
<span data-ttu-id="4f37e-145">Geben Sie diese Option an, um einen virtuellen Computer von einem speziellen Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f37e-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="4f37e-146">Wenn Sie diese Option angeben, geben Sie nicht den *Parameter "SourceImageUri"* an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="4f37e-147">Verwenden Sie stattdessen das Set-AzVMSourceImage Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="4f37e-148">Sie müssen auch die *Windows-* oder Linux-Parameter verwenden, um der azure-Plattform den Typ des Betriebssystems auf der VHD zu mitteilen. </span><span class="sxs-lookup"><span data-stu-id="4f37e-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="4f37e-149">Der *Parameter "VhdUri"* reicht aus, um der Azure-Plattform den Speicherort des anfügende Datenträgers zu mitteilen.</span><span class="sxs-lookup"><span data-stu-id="4f37e-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="4f37e-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="4f37e-150">FromImage.</span></span>
<span data-ttu-id="4f37e-151">Geben Sie diese Option an, um einen virtuellen Computer aus einem Plattformbild oder einem generalisierten Benutzerbild zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f37e-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="4f37e-152">Im Fall eines generalisierten Benutzerabbilds müssen Sie auch den *Parameter "SourceImageUri"* und entweder die *Windows-* oder die Linux-Parameter angeben, um der Azure-Plattform den Speicherort und typ des Betriebssystemdatenträgers VHD anzugeben, anstatt das **Cmdlet "Set-AzVMSourceImage"** zu verwenden. </span><span class="sxs-lookup"><span data-stu-id="4f37e-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="4f37e-153">Im Fall eines Plattformbilds ist der *Parameter "VhdUri"* ausreichend.</span><span class="sxs-lookup"><span data-stu-id="4f37e-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="4f37e-154">Leer.</span><span class="sxs-lookup"><span data-stu-id="4f37e-154">Empty.</span></span>

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

### <span data-ttu-id="4f37e-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f37e-155">-DefaultProfile</span></span>
<span data-ttu-id="4f37e-156">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f37e-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f37e-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="4f37e-157">-DiffDiskSetting</span></span>
<span data-ttu-id="4f37e-158">Gibt die unterschiedlichen Datenträgereinstellungen für den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="4f37e-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="4f37e-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="4f37e-160">Gibt den Speicherort des Datenträgerverschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="4f37e-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4f37e-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="4f37e-162">Gibt die Ressourcen-ID des Schlüsseltresor an, der den Datenträgerverschlüsselungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="4f37e-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="4f37e-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="4f37e-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="4f37e-164">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="4f37e-165">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f37e-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="4f37e-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4f37e-166">-DiskSizeInGB</span></span>
<span data-ttu-id="4f37e-167">Gibt die Größe (in GB) des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="4f37e-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="4f37e-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="4f37e-169">Gibt den Speicherort des Schlüsselverschlüsselungsschlüssels an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="4f37e-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4f37e-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="4f37e-171">Gibt die Ressourcen-ID des Schlüsseltresor an, der den Schlüsselverschlüsselungsschlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="4f37e-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="4f37e-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="4f37e-172">-Linux</span></span>
<span data-ttu-id="4f37e-173">Gibt an, dass das Betriebssystem im Benutzerbild Linux ist.</span><span class="sxs-lookup"><span data-stu-id="4f37e-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="4f37e-174">Geben Sie diesen Parameter für die Benutzerabbild-basierte Bereitstellung virtueller Computer an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="4f37e-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4f37e-175">-ManagedDiskId</span></span>
<span data-ttu-id="4f37e-176">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="4f37e-177">-Name</span><span class="sxs-lookup"><span data-stu-id="4f37e-177">-Name</span></span>
<span data-ttu-id="4f37e-178">Gibt den Namen des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="4f37e-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="4f37e-179">-SourceImageUri</span></span>
<span data-ttu-id="4f37e-180">Gibt den URI der VHD für Benutzerbildszenarien an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="4f37e-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4f37e-181">-StorageAccountType</span></span>
<span data-ttu-id="4f37e-182">Gibt den Speicherkontotyp des verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="4f37e-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4f37e-183">-VhdUri</span></span>
<span data-ttu-id="4f37e-184">Gibt den URI (Uniform Resource Identifier) einer virtuellen Festplatte (VHD) an.</span><span class="sxs-lookup"><span data-stu-id="4f37e-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="4f37e-185">Bei einem bildbasierten virtuellen Computer gibt dieser Parameter die VHD-Datei an, die beim Angeben eines Plattform- oder Benutzerbilds erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f37e-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="4f37e-186">Dies ist der Speicherort, von dem das binary large-Objekt (BLOB) des Bilds kopiert wird, um den virtuellen Computer zu starten.</span><span class="sxs-lookup"><span data-stu-id="4f37e-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="4f37e-187">Bei einem Datenträger-basierten Startszenario für einen virtuellen Computer gibt dieser Parameter die VHD-Datei an, die der virtuelle Computer direkt zum Starten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="4f37e-188">-VM</span><span class="sxs-lookup"><span data-stu-id="4f37e-188">-VM</span></span>
<span data-ttu-id="4f37e-189">Gibt das Objekt des lokalen virtuellen Computers an, für das Die Datenträgereigenschaften des Betriebssystems festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4f37e-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="4f37e-190">Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f37e-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="4f37e-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="4f37e-191">-Windows</span></span>
<span data-ttu-id="4f37e-192">Gibt an, dass windows das Betriebssystem des Benutzerbilds ist.</span><span class="sxs-lookup"><span data-stu-id="4f37e-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="4f37e-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4f37e-193">-WriteAccelerator</span></span>
<span data-ttu-id="4f37e-194">Gibt an, ob WriteAccelerator auf dem Betriebssystemdatenträger aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f37e-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="4f37e-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f37e-195">CommonParameters</span></span>
<span data-ttu-id="4f37e-196">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f37e-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f37e-197">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f37e-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f37e-198">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f37e-198">INPUTS</span></span>

### <span data-ttu-id="4f37e-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4f37e-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4f37e-200">System.String</span><span class="sxs-lookup"><span data-stu-id="4f37e-200">System.String</span></span>

## <span data-ttu-id="4f37e-201">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f37e-201">OUTPUTS</span></span>

### <span data-ttu-id="4f37e-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4f37e-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4f37e-203">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f37e-203">NOTES</span></span>

## <span data-ttu-id="4f37e-204">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f37e-204">RELATED LINKS</span></span>

[<span data-ttu-id="4f37e-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4f37e-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4f37e-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4f37e-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="4f37e-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4f37e-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


