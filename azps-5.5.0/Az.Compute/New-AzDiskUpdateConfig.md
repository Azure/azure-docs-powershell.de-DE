---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: caa424dc6c80cf2196091930c52d1fd80889bd75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148865"
---
# <span data-ttu-id="55fb2-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="55fb2-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="55fb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="55fb2-103">Erstellt ein konfigurierbares Datenträgeraktualisierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="55fb2-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="55fb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55fb2-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55fb2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="55fb2-106">Das **Cmdlet "New-AzDiskUpdateConfig"** erstellt ein konfigurierbares Datenträgeraktualisierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="55fb2-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="55fb2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="55fb2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55fb2-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="55fb2-109">Der erste Befehl erstellt ein lokales leeres Datenträgeraktualisierungsobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="55fb2-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="55fb2-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt, und es werden Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="55fb2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="55fb2-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Datenträgeraktualisierungsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="55fb2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="55fb2-112">Der letzte Befehl übernimmt das Datenträgeraktualisierungsobjekt und aktualisiert einen vorhandenen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="55fb2-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="55fb2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="55fb2-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="55fb2-114">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="55fb2-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="55fb2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55fb2-115">PARAMETERS</span></span>

### <span data-ttu-id="55fb2-116">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="55fb2-116">-BurstingEnabled</span></span>
<span data-ttu-id="55fb2-117">Ermöglicht das Aufplatzen über das bereitgestellte Leistungsziel des Datenträgers hinaus.</span><span class="sxs-lookup"><span data-stu-id="55fb2-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="55fb2-118">Das Aufplatzen ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="55fb2-118">Bursting is disabled by default.</span></span> <span data-ttu-id="55fb2-119">Gilt nicht für Ultra-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="55fb2-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="55fb2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fb2-120">-DefaultProfile</span></span>
<span data-ttu-id="55fb2-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55fb2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55fb2-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="55fb2-122">-DiskAccessId</span></span>
<span data-ttu-id="55fb2-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="55fb2-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="55fb2-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="55fb2-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="55fb2-125">Gibt das Objekt des Datenträgerverschlüsselungsschlüssels auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="55fb2-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="55fb2-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="55fb2-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="55fb2-127">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, mit dem ruhede Verschlüsselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="55fb2-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="55fb2-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="55fb2-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="55fb2-129">Die Gesamtzahl der IOPS, die für alle VMs zulässig sind, um den freigegebenen Datenträger als ReadOnly zu speichern.</span><span class="sxs-lookup"><span data-stu-id="55fb2-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="55fb2-130">Ein Vorgang kann zwischen 4 und 256 k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="55fb2-130">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fb2-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="55fb2-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="55fb2-132">Die Anzahl der für diesen Datenträger zulässigen IOPS; nur für UltraSSD-Datenträger festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="55fb2-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="55fb2-133">Ein Vorgang kann zwischen 4 und 256 k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="55fb2-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="55fb2-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="55fb2-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="55fb2-135">Der Gesamtdurchsatz (MBps), der für alle VMs zulässig ist, die den freigegebenen Datenträger mit "ReadOnly" (LesenOnly) abspeichern.</span><span class="sxs-lookup"><span data-stu-id="55fb2-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="55fb2-136">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Powers von 10.</span><span class="sxs-lookup"><span data-stu-id="55fb2-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fb2-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="55fb2-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="55fb2-138">Die für diesen Datenträger zulässige Bandbreite; nur für UltraSSD-Datenträger festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="55fb2-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="55fb2-139">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Powers von 10.</span><span class="sxs-lookup"><span data-stu-id="55fb2-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="55fb2-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="55fb2-140">-DiskSizeGB</span></span>
<span data-ttu-id="55fb2-141">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="55fb2-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="55fb2-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="55fb2-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="55fb2-143">Aktivieren Sie die Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="55fb2-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="55fb2-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="55fb2-144">-EncryptionType</span></span>
<span data-ttu-id="55fb2-145">Der Schlüsseltyp, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="55fb2-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="55fb2-146">Verfügbare Werte sind: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="55fb2-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="55fb2-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="55fb2-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="55fb2-148">Gibt den Schlüsselverschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="55fb2-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="55fb2-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="55fb2-149">-MaxSharesCount</span></span>
<span data-ttu-id="55fb2-150">Die maximale Anzahl von VMs, die gleichzeitig an den Datenträger anfügen können.</span><span class="sxs-lookup"><span data-stu-id="55fb2-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="55fb2-151">"Größer als eins" gibt einen Datenträger an, der gleichzeitig auf mehreren VMs bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="55fb2-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fb2-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="55fb2-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="55fb2-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="55fb2-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="55fb2-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="55fb2-154">-OsType</span></span>
<span data-ttu-id="55fb2-155">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="55fb2-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="55fb2-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="55fb2-156">-SkuName</span></span>
<span data-ttu-id="55fb2-157">Gibt den Namen der SKU des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="55fb2-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="55fb2-158">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="55fb2-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="55fb2-159">UltraSSD_LRS kann nur mit einem leeren Wert für den Parameter "CreateOption" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55fb2-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="55fb2-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="55fb2-160">-Tag</span></span>
<span data-ttu-id="55fb2-161">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="55fb2-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55fb2-162">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="55fb2-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55fb2-163">-Tier</span><span class="sxs-lookup"><span data-stu-id="55fb2-163">-Tier</span></span>
<span data-ttu-id="55fb2-164">Leistungsstufe des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="55fb2-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="55fb2-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55fb2-165">-Confirm</span></span>
<span data-ttu-id="55fb2-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55fb2-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55fb2-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55fb2-167">-WhatIf</span></span>
<span data-ttu-id="55fb2-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55fb2-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55fb2-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55fb2-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55fb2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fb2-170">CommonParameters</span></span>
<span data-ttu-id="55fb2-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fb2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fb2-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55fb2-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fb2-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55fb2-173">INPUTS</span></span>

### <span data-ttu-id="55fb2-174">System.String</span><span class="sxs-lookup"><span data-stu-id="55fb2-174">System.String</span></span>

### <span data-ttu-id="55fb2-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="55fb2-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="55fb2-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="55fb2-176">System.Int32</span></span>

### <span data-ttu-id="55fb2-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="55fb2-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="55fb2-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="55fb2-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="55fb2-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="55fb2-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="55fb2-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="55fb2-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="55fb2-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55fb2-181">OUTPUTS</span></span>

### <span data-ttu-id="55fb2-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="55fb2-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="55fb2-183">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55fb2-183">NOTES</span></span>

## <span data-ttu-id="55fb2-184">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55fb2-184">RELATED LINKS</span></span>
