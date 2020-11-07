---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 273a4388665e12cf58d1fe2d7e067648862bf4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661525"
---
# <span data-ttu-id="e6490-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e6490-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="e6490-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6490-102">SYNOPSIS</span></span>
<span data-ttu-id="e6490-103">Erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="e6490-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="e6490-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6490-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6490-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6490-105">DESCRIPTION</span></span>
<span data-ttu-id="e6490-106">Mit dem Cmdlet **New-AzDiskConfig** wird ein konfigurierbares Datenträgerobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e6490-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="e6490-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6490-107">EXAMPLES</span></span>

### <span data-ttu-id="e6490-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6490-108">Example 1</span></span>
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

<span data-ttu-id="e6490-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="e6490-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="e6490-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e6490-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e6490-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="e6490-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="e6490-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e6490-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e6490-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e6490-113">Example 2</span></span>
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

<span data-ttu-id="e6490-114">Der erste Befehl erstellt ein lokales Datenträgerobjekt für den Upload.</span><span class="sxs-lookup"><span data-stu-id="e6490-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="e6490-115">Der zweite Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e6490-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="e6490-116">Der dritte Befehl ruft die SAS-URL für den Datenträger ab.</span><span class="sxs-lookup"><span data-stu-id="e6490-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="e6490-117">Der vierte Befehl ruft den Zustand des Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="e6490-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="e6490-118">Wenn der Datenträgerstatus "ReadyToUpload" lautet, kann ein Benutzer mithilfe von AzCopy einen Datenträger vom BLOB-Speicher auf die SAS-URL der Festplatte hochladen.</span><span class="sxs-lookup"><span data-stu-id="e6490-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="e6490-119">Während des Uploads wird der Datenträgerstatus in "ActiveUpload" geändert.</span><span class="sxs-lookup"><span data-stu-id="e6490-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="e6490-120">Mit dem letzten Befehl wird der Datenträgerzugriff für die SAS-URL aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="e6490-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="e6490-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6490-121">PARAMETERS</span></span>

### <span data-ttu-id="e6490-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="e6490-122">-CreateOption</span></span>
<span data-ttu-id="e6490-123">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="e6490-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e6490-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6490-124">-DefaultProfile</span></span>
<span data-ttu-id="e6490-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6490-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6490-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e6490-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="e6490-127">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="e6490-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="e6490-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6490-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e6490-129">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e6490-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e6490-130">Ein Vorgang kann zwischen 4K-und 256 KB-Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="e6490-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="e6490-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e6490-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e6490-132">Die für diesen Datenträger zulässige Bandbreite; nur Settable für UltraSSD-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e6490-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e6490-133">Mbit/s bedeutet, dass Millionen von Bytes pro Sekunde-MB hier die ISO-Notation von Potenzen von 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6490-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="e6490-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e6490-134">-DiskSizeGB</span></span>
<span data-ttu-id="e6490-135">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="e6490-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e6490-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e6490-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e6490-137">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e6490-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e6490-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="e6490-138">-HyperVGeneration</span></span>
<span data-ttu-id="e6490-139">Die Hypervisor-Generierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e6490-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="e6490-140">Nur auf Betriebssystemdatenträger anwendbar.</span><span class="sxs-lookup"><span data-stu-id="e6490-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="e6490-141">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="e6490-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="e6490-142">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="e6490-142">-ImageReference</span></span>
<span data-ttu-id="e6490-143">Gibt den Bildverweis auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="e6490-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="e6490-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e6490-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="e6490-145">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="e6490-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="e6490-146">-Standort</span><span class="sxs-lookup"><span data-stu-id="e6490-146">-Location</span></span>
<span data-ttu-id="e6490-147">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="e6490-147">Specifies a location.</span></span>

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

### <span data-ttu-id="e6490-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="e6490-148">-OsType</span></span>
<span data-ttu-id="e6490-149">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="e6490-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e6490-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e6490-150">-SkuName</span></span>
<span data-ttu-id="e6490-151">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="e6490-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="e6490-152">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="e6490-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="e6490-153">UltraSSD_LRS können nur mit einem leeren Wert für den createoption-Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6490-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="e6490-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e6490-154">-SourceResourceId</span></span>
<span data-ttu-id="e6490-155">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="e6490-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="e6490-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e6490-156">-SourceUri</span></span>
<span data-ttu-id="e6490-157">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="e6490-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e6490-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e6490-158">-StorageAccountId</span></span>
<span data-ttu-id="e6490-159">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="e6490-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e6490-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6490-160">-Tag</span></span>
<span data-ttu-id="e6490-161">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="e6490-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e6490-162">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="e6490-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e6490-163">-Zone</span><span class="sxs-lookup"><span data-stu-id="e6490-163">-Zone</span></span>
<span data-ttu-id="e6490-164">Gibt die Liste der logischen Zonen für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="e6490-164">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="e6490-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e6490-165">-Confirm</span></span>
<span data-ttu-id="e6490-166">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6490-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6490-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6490-167">-WhatIf</span></span>
<span data-ttu-id="e6490-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6490-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6490-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6490-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6490-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6490-170">CommonParameters</span></span>
<span data-ttu-id="e6490-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6490-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6490-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6490-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6490-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6490-173">INPUTS</span></span>

### <span data-ttu-id="e6490-174">System. String</span><span class="sxs-lookup"><span data-stu-id="e6490-174">System.String</span></span>

### <span data-ttu-id="e6490-175">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e6490-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e6490-176">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e6490-176">System.Int32</span></span>

### <span data-ttu-id="e6490-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="e6490-177">System.String[]</span></span>

### <span data-ttu-id="e6490-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6490-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6490-179">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="e6490-179">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="e6490-180">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6490-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e6490-181">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e6490-181">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e6490-182">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e6490-182">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e6490-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6490-183">OUTPUTS</span></span>

### <span data-ttu-id="e6490-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="e6490-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e6490-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6490-185">NOTES</span></span>

## <span data-ttu-id="e6490-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6490-186">RELATED LINKS</span></span>
