---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 7a8c4bc3b875cb9072386784fe1c06730be89405
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996176"
---
# <span data-ttu-id="9558c-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="9558c-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="9558c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9558c-102">SYNOPSIS</span></span>
<span data-ttu-id="9558c-103">Erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="9558c-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="9558c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9558c-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9558c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9558c-105">DESCRIPTION</span></span>
<span data-ttu-id="9558c-106">Mit dem Cmdlet **New-AzDiskConfig** wird ein konfigurierbares Datenträgerobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9558c-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="9558c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9558c-107">EXAMPLES</span></span>

### <span data-ttu-id="9558c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9558c-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="9558c-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="9558c-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="9558c-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9558c-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="9558c-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="9558c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="9558c-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9558c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9558c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9558c-113">Example 2</span></span>
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

<span data-ttu-id="9558c-114">Der erste Befehl erstellt ein lokales Datenträgerobjekt für den Upload.</span><span class="sxs-lookup"><span data-stu-id="9558c-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="9558c-115">Der zweite Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9558c-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="9558c-116">Der dritte Befehl ruft die SAS-URL für den Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="9558c-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="9558c-117">Der vierte Befehl ruft den Zustand des Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="9558c-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="9558c-118">Wenn der Datenträgerstatus "ReadyToUpload" lautet, kann ein Benutzer mithilfe von AzCopy einen Datenträger vom BLOB-Speicher auf die SAS-URL der Festplatte hochladen.</span><span class="sxs-lookup"><span data-stu-id="9558c-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="9558c-119">Während des Uploads wird der Datenträgerstatus in "ActiveUpload" geändert.</span><span class="sxs-lookup"><span data-stu-id="9558c-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="9558c-120">Mit dem letzten Befehl wird der Datenträgerzugriff für die SAS-URL aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="9558c-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="9558c-121">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="9558c-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="9558c-122">Erstellen Sie einen Datenträger aus einer freigegebenen Katalogbild Version.</span><span class="sxs-lookup"><span data-stu-id="9558c-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="9558c-123">ID ist die ID der freigegebenen Katalogbild Version.</span><span class="sxs-lookup"><span data-stu-id="9558c-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="9558c-124">LUN ist nur erforderlich, wenn es sich bei der Quelle um einen Daten Datenträger handelt.</span><span class="sxs-lookup"><span data-stu-id="9558c-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="9558c-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="9558c-125">PARAMETERS</span></span>

### <span data-ttu-id="9558c-126">-Createoption</span><span class="sxs-lookup"><span data-stu-id="9558c-126">-CreateOption</span></span>
<span data-ttu-id="9558c-127">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="9558c-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="9558c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9558c-128">-DefaultProfile</span></span>
<span data-ttu-id="9558c-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9558c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9558c-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9558c-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="9558c-131">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9558c-131">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="9558c-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9558c-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9558c-133">Gibt die Ressourcen-ID des Datenträger Verschlüsselungs Satzes an, mit dem die Verschlüsselung im Ruhezustand aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9558c-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="9558c-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="9558c-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="9558c-135">Die Gesamtzahl der IOPS, die für alle VMs zulässig sind, die den freigegebenen Datenträger als ReadOnly bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9558c-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="9558c-136">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="9558c-136">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="9558c-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="9558c-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="9558c-138">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9558c-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="9558c-139">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="9558c-139">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="9558c-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="9558c-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="9558c-141">"Beschreibung": "der Gesamtdurchsatz (Mbit/s), der für alle VMs zulässig ist, die den freigegebenen Datenträger als ReadOnly bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9558c-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="9558c-142">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="9558c-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="9558c-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="9558c-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="9558c-144">Die für diesen Datenträger zulässige Bandbreite; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9558c-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="9558c-145">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="9558c-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="9558c-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9558c-146">-DiskSizeGB</span></span>
<span data-ttu-id="9558c-147">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="9558c-147">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="9558c-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="9558c-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="9558c-149">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9558c-149">Enable encryption settings.</span></span>

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

### <span data-ttu-id="9558c-150">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="9558c-150">-EncryptionType</span></span>
<span data-ttu-id="9558c-151">Der Typ des Schlüssels, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9558c-151">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="9558c-152">Die verfügbaren Werte lauten: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="9558c-152">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="9558c-153">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="9558c-153">-GalleryImageReference</span></span>
<span data-ttu-id="9558c-154">Das GalleryImageReference-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9558c-154">The GalleryImageReference object.</span></span>  <span data-ttu-id="9558c-155">Erforderlich, wenn Sie aus einem Katalogbild erstellen.</span><span class="sxs-lookup"><span data-stu-id="9558c-155">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="9558c-156">Die ID ist die Arm-ID der freigegebenen Galley-Bildversion, aus der Sie einen Datenträger erstellen können.</span><span class="sxs-lookup"><span data-stu-id="9558c-156">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="9558c-157">Eine LUN wird benötigt, wenn die Quelle der Kopie einer der Daten Datenträger im Katalogbild ist. ist der Wert NULL, wird der Betriebssystemdatenträger des Bilds kopiert.</span><span class="sxs-lookup"><span data-stu-id="9558c-157">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="9558c-158">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="9558c-158">-HyperVGeneration</span></span>
<span data-ttu-id="9558c-159">Die Hypervisor-Generierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9558c-159">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="9558c-160">Nur auf Betriebssystemdatenträger anwendbar.</span><span class="sxs-lookup"><span data-stu-id="9558c-160">Applicable to OS disks only.</span></span>  <span data-ttu-id="9558c-161">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="9558c-161">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="9558c-162">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="9558c-162">-ImageReference</span></span>
<span data-ttu-id="9558c-163">Gibt den Bildverweis auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9558c-163">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="9558c-164">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9558c-164">-KeyEncryptionKey</span></span>
<span data-ttu-id="9558c-165">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9558c-165">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="9558c-166">-Standort</span><span class="sxs-lookup"><span data-stu-id="9558c-166">-Location</span></span>
<span data-ttu-id="9558c-167">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="9558c-167">Specifies a location.</span></span>

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

### <span data-ttu-id="9558c-168">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="9558c-168">-MaxSharesCount</span></span>
<span data-ttu-id="9558c-169">Die maximale Anzahl von VMS, die gleichzeitig an den Datenträger angefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="9558c-169">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="9558c-170">Der Wert größer als 1 gibt einen Datenträger an, der gleichzeitig auf mehreren VMS bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9558c-170">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="9558c-171">-OsType</span><span class="sxs-lookup"><span data-stu-id="9558c-171">-OsType</span></span>
<span data-ttu-id="9558c-172">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="9558c-172">Specifies the OS type.</span></span>

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

### <span data-ttu-id="9558c-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9558c-173">-SkuName</span></span>
<span data-ttu-id="9558c-174">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="9558c-174">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="9558c-175">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="9558c-175">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="9558c-176">UltraSSD_LRS können nur mit einem leeren Wert für den createoption-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-176">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="9558c-177">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="9558c-177">-SourceResourceId</span></span>
<span data-ttu-id="9558c-178">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="9558c-178">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="9558c-179">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="9558c-179">-SourceUri</span></span>
<span data-ttu-id="9558c-180">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="9558c-180">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="9558c-181">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9558c-181">-StorageAccountId</span></span>
<span data-ttu-id="9558c-182">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="9558c-182">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="9558c-183">-Tag</span><span class="sxs-lookup"><span data-stu-id="9558c-183">-Tag</span></span>
<span data-ttu-id="9558c-184">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="9558c-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9558c-185">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9558c-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9558c-186">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="9558c-186">-UploadSizeInBytes</span></span>
<span data-ttu-id="9558c-187">Gibt die Größe des Inhalts des Uploads an, einschließlich der VHD-Fußzeile, wenn createoption hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="9558c-187">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="9558c-188">Dieser Wert sollte zwischen 20972032 (20 MIB + 512 Byte für die VHD-Fußzeile) und 35183298347520 bytes (32 tib + 512 Bytes für die VHD-Fußzeile) liegen.</span><span class="sxs-lookup"><span data-stu-id="9558c-188">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="9558c-189">-Zone</span><span class="sxs-lookup"><span data-stu-id="9558c-189">-Zone</span></span>
<span data-ttu-id="9558c-190">Gibt die Liste der logischen Zonen für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="9558c-190">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="9558c-191">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9558c-191">-Confirm</span></span>
<span data-ttu-id="9558c-192">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9558c-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9558c-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9558c-193">-WhatIf</span></span>
<span data-ttu-id="9558c-194">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9558c-194">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9558c-195">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9558c-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9558c-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9558c-196">CommonParameters</span></span>
<span data-ttu-id="9558c-197">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9558c-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9558c-198">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9558c-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9558c-199">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9558c-199">INPUTS</span></span>

### <span data-ttu-id="9558c-200">System. String</span><span class="sxs-lookup"><span data-stu-id="9558c-200">System.String</span></span>

### <span data-ttu-id="9558c-201">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9558c-201">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9558c-202">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9558c-202">System.Int32</span></span>

### <span data-ttu-id="9558c-203">System. String []</span><span class="sxs-lookup"><span data-stu-id="9558c-203">System.String[]</span></span>

### <span data-ttu-id="9558c-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9558c-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9558c-205">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="9558c-205">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="9558c-206">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9558c-206">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9558c-207">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="9558c-207">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="9558c-208">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="9558c-208">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="9558c-209">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9558c-209">OUTPUTS</span></span>

### <span data-ttu-id="9558c-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="9558c-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="9558c-211">Notizen</span><span class="sxs-lookup"><span data-stu-id="9558c-211">NOTES</span></span>

## <span data-ttu-id="9558c-212">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9558c-212">RELATED LINKS</span></span>
