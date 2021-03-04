---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921408"
---
# <span data-ttu-id="a85a1-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="a85a1-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="a85a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a85a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a85a1-103">Erstellt ein konfigurierbares Datenträgerupdateobjekt.</span><span class="sxs-lookup"><span data-stu-id="a85a1-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="a85a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a85a1-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a85a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a85a1-106">Das **Cmdlet New-AzDiskUpdateConfig** erstellt ein konfigurierbares Datenträgerupdateobjekt.</span><span class="sxs-lookup"><span data-stu-id="a85a1-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="a85a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a85a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a85a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a85a1-108">Example 1</span></span>
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

<span data-ttu-id="a85a1-109">Mit dem ersten Befehl wird ein lokales leeres Datenträgeraktualisierungsobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="a85a1-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="a85a1-110">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a85a1-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a85a1-111">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Datenträgeraktualisierungsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a85a1-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="a85a1-112">Der letzte Befehl übernimmt das Datenträgeraktualisierungsobjekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a85a1-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a85a1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a85a1-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="a85a1-114">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a85a1-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="a85a1-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a85a1-115">PARAMETERS</span></span>

### <span data-ttu-id="a85a1-116">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="a85a1-116">-BurstingEnabled</span></span>
<span data-ttu-id="a85a1-117">Ermöglicht das Bursting über das bereitgestellte Leistungsziel des Datenträgers hinaus.</span><span class="sxs-lookup"><span data-stu-id="a85a1-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="a85a1-118">Bursting ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a85a1-118">Bursting is disabled by default.</span></span> <span data-ttu-id="a85a1-119">Gilt nicht für Ultra-Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a85a1-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="a85a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85a1-120">-DefaultProfile</span></span>
<span data-ttu-id="a85a1-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a85a1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a85a1-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="a85a1-122">-DiskAccessId</span></span>
<span data-ttu-id="a85a1-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="a85a1-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="a85a1-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a85a1-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="a85a1-125">Gibt das Objekt des Datenträgerverschlüsselungsschlüssels auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="a85a1-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a85a1-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a85a1-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a85a1-127">Gibt die Ressourcen-ID der Datenträgerverschlüsselung an, die zum Aktivieren der ruhenden Verschlüsselung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a85a1-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="a85a1-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="a85a1-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="a85a1-129">Die Gesamtanzahl der IOPS, die für alle VMs zulässig sind, die den freigegebenen Datenträger als ReadOnly häufen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="a85a1-130">Ein Vorgang kann zwischen 4k und 256k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="a85a1-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="a85a1-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="a85a1-132">Die Anzahl der ioPS, die für diesen Datenträger zulässig sind; nur für UltraSSD-Datenträger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a85a1-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a85a1-133">Ein Vorgang kann zwischen 4k und 256k Bytes übertragen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="a85a1-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="a85a1-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="a85a1-135">Der Gesamtdurchsatz (MBps), der für alle VMs zulässig ist, die den freigegebenen Datenträger als ReadOnly bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="a85a1-136">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Befugnissen 10.</span><span class="sxs-lookup"><span data-stu-id="a85a1-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="a85a1-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="a85a1-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="a85a1-138">Die für diesen Datenträger zulässige Bandbreite; nur für UltraSSD-Datenträger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a85a1-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a85a1-139">MBps bedeutet Millionen von Bytes pro Sekunde – MB verwendet hier die ISO-Notation mit den Befugnissen 10.</span><span class="sxs-lookup"><span data-stu-id="a85a1-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="a85a1-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a85a1-140">-DiskSizeGB</span></span>
<span data-ttu-id="a85a1-141">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="a85a1-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a85a1-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a85a1-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a85a1-143">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a85a1-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="a85a1-144">-EncryptionType</span></span>
<span data-ttu-id="a85a1-145">Der Schlüsseltyp, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a85a1-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="a85a1-146">Verfügbare Werte sind: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="a85a1-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="a85a1-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a85a1-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="a85a1-148">Gibt den Schlüsselverschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="a85a1-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a85a1-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="a85a1-149">-MaxSharesCount</span></span>
<span data-ttu-id="a85a1-150">Die maximale Anzahl von VMs, die gleichzeitig an den Datenträger anfügen können.</span><span class="sxs-lookup"><span data-stu-id="a85a1-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="a85a1-151">Der Wert größer als ein Wert gibt einen Datenträger an, der gleichzeitig auf mehreren VMs bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a85a1-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="a85a1-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a85a1-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="a85a1-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="a85a1-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="a85a1-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="a85a1-154">-OsType</span></span>
<span data-ttu-id="a85a1-155">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="a85a1-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a85a1-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a85a1-156">-SkuName</span></span>
<span data-ttu-id="a85a1-157">Gibt den Sku-Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="a85a1-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="a85a1-158">Verfügbare Werte sind Standard_LRS, Premium_LRS, StandardSSD_LRS und UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="a85a1-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="a85a1-159">UltraSSD_LRS kann nur mit dem Parameter Leerwert für CreateOption verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a85a1-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="a85a1-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="a85a1-160">-Tag</span></span>
<span data-ttu-id="a85a1-161">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a85a1-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a85a1-162">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a85a1-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a85a1-163">-Tier</span><span class="sxs-lookup"><span data-stu-id="a85a1-163">-Tier</span></span>
<span data-ttu-id="a85a1-164">Leistungsstufe des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="a85a1-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="a85a1-165">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a85a1-165">-Confirm</span></span>
<span data-ttu-id="a85a1-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a85a1-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85a1-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85a1-167">-WhatIf</span></span>
<span data-ttu-id="a85a1-168">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a85a1-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a85a1-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a85a1-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85a1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85a1-170">CommonParameters</span></span>
<span data-ttu-id="a85a1-171">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85a1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85a1-172">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a85a1-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85a1-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a85a1-173">INPUTS</span></span>

### <span data-ttu-id="a85a1-174">System.String</span><span class="sxs-lookup"><span data-stu-id="a85a1-174">System.String</span></span>

### <span data-ttu-id="a85a1-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a85a1-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a85a1-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a85a1-176">System.Int32</span></span>

### <span data-ttu-id="a85a1-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a85a1-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a85a1-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a85a1-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a85a1-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a85a1-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a85a1-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a85a1-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a85a1-181">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a85a1-181">OUTPUTS</span></span>

### <span data-ttu-id="a85a1-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="a85a1-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="a85a1-183">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a85a1-183">NOTES</span></span>

## <span data-ttu-id="a85a1-184">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a85a1-184">RELATED LINKS</span></span>
