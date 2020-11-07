---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652087"
---
# <span data-ttu-id="62c8c-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="62c8c-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="62c8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="62c8c-103">Erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="62c8c-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="62c8c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62c8c-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c8c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62c8c-105">DESCRIPTION</span></span>
<span data-ttu-id="62c8c-106">Mit dem Cmdlet **New-AzDiskConfig** wird ein konfigurierbares Datenträgerobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="62c8c-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="62c8c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62c8c-107">EXAMPLES</span></span>

### <span data-ttu-id="62c8c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62c8c-108">Example 1</span></span>
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

<span data-ttu-id="62c8c-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="62c8c-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="62c8c-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="62c8c-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="62c8c-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="62c8c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="62c8c-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="62c8c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="62c8c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="62c8c-113">Example 2</span></span>
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

<span data-ttu-id="62c8c-114">Der erste Befehl erstellt ein lokales Datenträgerobjekt für den Upload.</span><span class="sxs-lookup"><span data-stu-id="62c8c-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="62c8c-115">Der zweite Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="62c8c-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="62c8c-116">Der dritte Befehl ruft die SAS-URL für den Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="62c8c-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="62c8c-117">Der vierte Befehl ruft den Zustand des Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="62c8c-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="62c8c-118">Wenn der Datenträgerstatus "ReadyToUpload" lautet, kann ein Benutzer mithilfe von AzCopy einen Datenträger vom BLOB-Speicher auf die SAS-URL der Festplatte hochladen.</span><span class="sxs-lookup"><span data-stu-id="62c8c-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="62c8c-119">Während des Uploads wird der Datenträgerstatus in "ActiveUpload" geändert.</span><span class="sxs-lookup"><span data-stu-id="62c8c-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="62c8c-120">Mit dem letzten Befehl wird der Datenträgerzugriff für die SAS-URL aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="62c8c-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="62c8c-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="62c8c-121">PARAMETERS</span></span>

### <span data-ttu-id="62c8c-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="62c8c-122">-CreateOption</span></span>
<span data-ttu-id="62c8c-123">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="62c8c-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="62c8c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c8c-124">-DefaultProfile</span></span>
<span data-ttu-id="62c8c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62c8c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c8c-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62c8c-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="62c8c-127">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="62c8c-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="62c8c-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="62c8c-129">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="62c8c-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="62c8c-130">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="62c8c-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="62c8c-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="62c8c-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="62c8c-132">Die für diesen Datenträger zulässige Bandbreite; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="62c8c-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="62c8c-133">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="62c8c-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="62c8c-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="62c8c-134">-DiskSizeGB</span></span>
<span data-ttu-id="62c8c-135">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="62c8c-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="62c8c-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="62c8c-137">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="62c8c-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="62c8c-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="62c8c-138">-HyperVGeneration</span></span>
<span data-ttu-id="62c8c-139">Die Hypervisor-Generierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="62c8c-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="62c8c-140">Nur auf Betriebssystemdatenträger anwendbar.</span><span class="sxs-lookup"><span data-stu-id="62c8c-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="62c8c-141">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="62c8c-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="62c8c-142">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="62c8c-142">-ImageReference</span></span>
<span data-ttu-id="62c8c-143">Gibt den Bildverweis auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="62c8c-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62c8c-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="62c8c-145">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="62c8c-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="62c8c-146">-Location</span></span>
<span data-ttu-id="62c8c-147">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-147">Specifies a location.</span></span>

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

### <span data-ttu-id="62c8c-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="62c8c-148">-OsType</span></span>
<span data-ttu-id="62c8c-149">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="62c8c-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="62c8c-150">-SkuName</span></span>
<span data-ttu-id="62c8c-151">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="62c8c-152">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="62c8c-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="62c8c-153">UltraSSD_LRS können nur mit einem leeren Wert für den createoption-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62c8c-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="62c8c-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="62c8c-154">-SourceResourceId</span></span>
<span data-ttu-id="62c8c-155">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="62c8c-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="62c8c-156">-SourceUri</span></span>
<span data-ttu-id="62c8c-157">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="62c8c-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="62c8c-158">-StorageAccountId</span></span>
<span data-ttu-id="62c8c-159">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="62c8c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="62c8c-160">-Tag</span></span>
<span data-ttu-id="62c8c-161">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="62c8c-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="62c8c-162">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="62c8c-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="62c8c-163">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="62c8c-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="62c8c-164">Gibt die Größe des Inhalts des Uploads an, einschließlich der VHD-Fußzeile, wenn createoption hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="62c8c-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="62c8c-165">Dieser Wert sollte zwischen 20972032 (20 MIB + 512 Byte für die VHD-Fußzeile) und 35183298347520 bytes (32 tib + 512 Bytes für die VHD-Fußzeile) liegen.</span><span class="sxs-lookup"><span data-stu-id="62c8c-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="62c8c-166">-Zone</span><span class="sxs-lookup"><span data-stu-id="62c8c-166">-Zone</span></span>
<span data-ttu-id="62c8c-167">Gibt die Liste der logischen Zonen für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="62c8c-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="62c8c-168">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62c8c-168">-Confirm</span></span>
<span data-ttu-id="62c8c-169">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62c8c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c8c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c8c-170">-WhatIf</span></span>
<span data-ttu-id="62c8c-171">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62c8c-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62c8c-172">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62c8c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c8c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c8c-173">CommonParameters</span></span>
<span data-ttu-id="62c8c-174">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c8c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c8c-175">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62c8c-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c8c-176">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62c8c-176">INPUTS</span></span>

### <span data-ttu-id="62c8c-177">System. String</span><span class="sxs-lookup"><span data-stu-id="62c8c-177">System.String</span></span>

### <span data-ttu-id="62c8c-178">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62c8c-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="62c8c-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62c8c-179">System.Int32</span></span>

### <span data-ttu-id="62c8c-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="62c8c-180">System.String[]</span></span>

### <span data-ttu-id="62c8c-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62c8c-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62c8c-182">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="62c8c-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="62c8c-183">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62c8c-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62c8c-184">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="62c8c-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="62c8c-185">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="62c8c-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="62c8c-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62c8c-186">OUTPUTS</span></span>

### <span data-ttu-id="62c8c-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="62c8c-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="62c8c-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="62c8c-188">NOTES</span></span>

## <span data-ttu-id="62c8c-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62c8c-189">RELATED LINKS</span></span>
