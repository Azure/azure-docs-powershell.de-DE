---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 12ebf45a0428b170f40edce6129d76dd7fcbd601
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148873"
---
# <span data-ttu-id="1370f-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="1370f-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="1370f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1370f-102">SYNOPSIS</span></span>
<span data-ttu-id="1370f-103">Erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="1370f-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="1370f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1370f-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1370f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1370f-105">DESCRIPTION</span></span>
<span data-ttu-id="1370f-106">Das **Cmdlet "New-AzDiskConfig"** erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="1370f-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="1370f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1370f-107">EXAMPLES</span></span>

### <span data-ttu-id="1370f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1370f-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="1370f-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit einer Größe von 5 GB im Standard_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="1370f-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="1370f-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt, und es werden Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1370f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="1370f-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Datenträgerobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1370f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="1370f-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="1370f-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1370f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1370f-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="1370f-114">Mit dem ersten Befehl wird ein lokales Datenträgerobjekt für "Upload" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1370f-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="1370f-115">Der zweite Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="1370f-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="1370f-116">Der dritte Befehl ruft die SAS-URL für den Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="1370f-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="1370f-117">Der vierte Befehl ruft den Zustand des Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="1370f-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="1370f-118">Wenn der Datenträgerstatus "ReadyToUpload" ist, kann ein Benutzer mithilfe von AzCopy einen Datenträger aus dem BLOB-Speicher in die SAS-URL des Datenträgers hochladen.</span><span class="sxs-lookup"><span data-stu-id="1370f-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="1370f-119">Während des Uploads wird der Datenträgerzustand in "ActiveUpload" geändert.</span><span class="sxs-lookup"><span data-stu-id="1370f-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="1370f-120">Der letzte Befehl widerruft den Datenträgerzugriff für die SAS-URL.</span><span class="sxs-lookup"><span data-stu-id="1370f-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="1370f-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1370f-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="1370f-122">Erstellen Sie einen Datenträger aus einer freigegebenen Katalogbildversion.</span><span class="sxs-lookup"><span data-stu-id="1370f-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="1370f-123">"ID" ist die ID der Bildversion des freigegebenen Katalogs.</span><span class="sxs-lookup"><span data-stu-id="1370f-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="1370f-124">Lun wird nur benötigt, wenn es sich bei der Quelle um einen Datenträger handelt.</span><span class="sxs-lookup"><span data-stu-id="1370f-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="1370f-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1370f-125">PARAMETERS</span></span>

### <span data-ttu-id="1370f-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="1370f-126">-BurstingEnabled</span></span>
<span data-ttu-id="1370f-127">Ermöglicht das Aufplatzen über das bereitgestellte Leistungsziel des Datenträgers hinaus.</span><span class="sxs-lookup"><span data-stu-id="1370f-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="1370f-128">Das Aufplatzen ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1370f-128">Bursting is disabled by default.</span></span> <span data-ttu-id="1370f-129">Gilt nicht für Ultra-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1370f-129">Does not apply to Ultra disks.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="1370f-130">-CreateOption</span></span>
<span data-ttu-id="1370f-131">Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="1370f-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="1370f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1370f-132">-DefaultProfile</span></span>
<span data-ttu-id="1370f-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1370f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1370f-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="1370f-134">-DiskAccessId</span></span>
<span data-ttu-id="1370f-135">Ruft die ARM der Ressource "DiskAccess" für die Verwendung privater Endpunkte ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="1370f-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="1370f-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1370f-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="1370f-137">Gibt das Objekt des Datenträgerverschlüsselungsschlüssels auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="1370f-137">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1370f-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1370f-139">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, mit dem ruhede Verschlüsselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1370f-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="1370f-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="1370f-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="1370f-141">Die Gesamtzahl der IOPS, die für alle VMs zulässig sind, um den freigegebenen Datenträger als ReadOnly zu speichern.</span><span class="sxs-lookup"><span data-stu-id="1370f-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1370f-142">Ein Vorgang kann zwischen 4 und 256 k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="1370f-142">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="1370f-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="1370f-144">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur für UltraSSD-Datenträger festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="1370f-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1370f-145">Ein Vorgang kann zwischen 4 und 256 k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="1370f-145">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="1370f-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="1370f-147">"description": "Der Gesamtdurchsatz (MBps), der für alle VMs zulässig ist, die den freigegebenen Datenträger wie "ReadOnly" speichern.</span><span class="sxs-lookup"><span data-stu-id="1370f-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="1370f-148">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Powers von 10.</span><span class="sxs-lookup"><span data-stu-id="1370f-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="1370f-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="1370f-150">Die für diesen Datenträger zulässige Bandbreite; nur für UltraSSD-Datenträger festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="1370f-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="1370f-151">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Powers von 10.</span><span class="sxs-lookup"><span data-stu-id="1370f-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1370f-152">-DiskSizeGB</span></span>
<span data-ttu-id="1370f-153">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="1370f-153">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1370f-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="1370f-155">Aktivieren Sie die Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="1370f-155">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="1370f-156">-EncryptionType</span></span>
<span data-ttu-id="1370f-157">Der Schlüsseltyp, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1370f-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="1370f-158">Verfügbare Werte sind: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="1370f-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="1370f-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="1370f-159">-GalleryImageReference</span></span>
<span data-ttu-id="1370f-160">Das GalleryImageReference-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1370f-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="1370f-161">Erforderlich beim Erstellen aus einem Katalogbild.</span><span class="sxs-lookup"><span data-stu-id="1370f-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="1370f-162">Die ID ist die ARM-ID der freigegebenen Galley-Bildversion, aus der ein Datenträger erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1370f-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="1370f-163">Ein Lun ist erforderlich, wenn die Quelle der Kopie eine der Datenträger im Katalogbild ist. wenn null ist, wird der Betriebssystemdatenträger des Bilds kopiert.</span><span class="sxs-lookup"><span data-stu-id="1370f-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="1370f-164">-HyperVGeneration</span></span>
<span data-ttu-id="1370f-165">Die Hypervisorgenerierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="1370f-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="1370f-166">Gilt nur für Betriebssystemdatenträger.</span><span class="sxs-lookup"><span data-stu-id="1370f-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="1370f-167">Zulässige Werte sind V1 und V2.</span><span class="sxs-lookup"><span data-stu-id="1370f-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="1370f-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="1370f-168">-ImageReference</span></span>
<span data-ttu-id="1370f-169">Gibt den Bildverweis auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="1370f-169">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1370f-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="1370f-171">Gibt den Schlüsselverschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="1370f-171">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-172">-Location</span><span class="sxs-lookup"><span data-stu-id="1370f-172">-Location</span></span>
<span data-ttu-id="1370f-173">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="1370f-173">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="1370f-174">-LogicalSectorSize</span></span>
<span data-ttu-id="1370f-175">Logische Größe des Hochformats in Bytes für Ultra-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1370f-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="1370f-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="1370f-176">-MaxSharesCount</span></span>
<span data-ttu-id="1370f-177">Die maximale Anzahl von VMs, die gleichzeitig an den Datenträger anfügen können.</span><span class="sxs-lookup"><span data-stu-id="1370f-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="1370f-178">"Größer als eins" gibt einen Datenträger an, der gleichzeitig auf mehreren VMs bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1370f-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="1370f-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1370f-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="1370f-180">Die Netzwerkzugriffsrichtlinie definiert die Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="1370f-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="1370f-181">Mögliche Werte sind: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="1370f-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="1370f-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="1370f-182">-OsType</span></span>
<span data-ttu-id="1370f-183">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="1370f-183">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1370f-184">-SkuName</span></span>
<span data-ttu-id="1370f-185">Gibt den Namen der SKU des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1370f-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="1370f-186">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="1370f-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="1370f-187">UltraSSD_LRS kann nur mit einem leeren Wert für den Parameter "CreateOption" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1370f-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="1370f-188">-SourceResourceId</span></span>
<span data-ttu-id="1370f-189">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="1370f-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="1370f-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="1370f-190">-SourceUri</span></span>
<span data-ttu-id="1370f-191">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="1370f-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="1370f-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1370f-192">-StorageAccountId</span></span>
<span data-ttu-id="1370f-193">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="1370f-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="1370f-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="1370f-194">-Tag</span></span>
<span data-ttu-id="1370f-195">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1370f-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1370f-196">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1370f-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="1370f-197">-Tier</span></span>
<span data-ttu-id="1370f-198">Leistungsstufe des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1370f-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="1370f-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="1370f-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="1370f-200">Gibt die Größe des Inhalts des Uploads einschließlich der VHD-Fußzeile an, wenn "CreateOption" "Upload" ist.</span><span class="sxs-lookup"><span data-stu-id="1370f-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="1370f-201">Dieser Wert sollte zwischen 20972032 (20 MiB + 512 Bytes für die VHD-Fußzeile) und 35183298347520 Bytes (32 TiB + 512 Bytes für die Fußzeile von VHD) liegen.</span><span class="sxs-lookup"><span data-stu-id="1370f-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="1370f-202">-Zone</span></span>
<span data-ttu-id="1370f-203">Gibt die Liste der logischen Zonen für "Datenträger" an.</span><span class="sxs-lookup"><span data-stu-id="1370f-203">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1370f-204">-Confirm</span></span>
<span data-ttu-id="1370f-205">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1370f-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-206">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1370f-206">-WhatIf</span></span>
<span data-ttu-id="1370f-207">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1370f-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1370f-208">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1370f-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1370f-209">CommonParameters</span></span>
<span data-ttu-id="1370f-210">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1370f-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1370f-211">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1370f-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1370f-212">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1370f-212">INPUTS</span></span>

### <span data-ttu-id="1370f-213">System.String</span><span class="sxs-lookup"><span data-stu-id="1370f-213">System.String</span></span>

### <span data-ttu-id="1370f-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1370f-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1370f-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1370f-215">System.Int32</span></span>

### <span data-ttu-id="1370f-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1370f-216">System.String[]</span></span>

### <span data-ttu-id="1370f-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1370f-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1370f-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="1370f-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="1370f-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1370f-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1370f-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="1370f-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="1370f-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="1370f-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="1370f-222">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1370f-222">OUTPUTS</span></span>

### <span data-ttu-id="1370f-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="1370f-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1370f-224">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1370f-224">NOTES</span></span>

## <span data-ttu-id="1370f-225">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1370f-225">RELATED LINKS</span></span>
