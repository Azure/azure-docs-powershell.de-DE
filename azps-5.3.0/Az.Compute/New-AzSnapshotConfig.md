---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473065"
---
# <span data-ttu-id="c21db-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="c21db-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="c21db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c21db-102">SYNOPSIS</span></span>
<span data-ttu-id="c21db-103">Erstellt ein konfigurierbares Momentaufnahmeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c21db-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="c21db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c21db-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c21db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c21db-105">DESCRIPTION</span></span>
<span data-ttu-id="c21db-106">Das **Cmdlet "New-AzSnapshotConfig"** erstellt ein konfigurierbares Momentaufnahmeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c21db-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="c21db-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c21db-107">EXAMPLES</span></span>

### <span data-ttu-id="c21db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c21db-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="c21db-109">Der erste Befehl erstellt ein lokales leeres Momentaufnahmeobjekt mit einer Größe von 5 GB Standard_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="c21db-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="c21db-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c21db-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c21db-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Momentaufnahmeobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c21db-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="c21db-112">Der letzte Befehl erstellt das Momentaufnahmeobjekt und erstellt eine Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="c21db-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c21db-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c21db-113">Example 2</span></span>

<span data-ttu-id="c21db-114">Erstellt ein konfigurierbares Momentaufnahmeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c21db-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="c21db-115">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c21db-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="c21db-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c21db-116">PARAMETERS</span></span>

### <span data-ttu-id="c21db-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c21db-117">-CreateOption</span></span>
<span data-ttu-id="c21db-118">Gibt an, ob mit diesem Cmdlet ein Datenträger auf dem virtuellen Computer über eine Plattform oder ein Benutzerabbild erstellt, ein leerer Datenträger erstellt oder ein vorhandener Datenträger anfügen wird.</span><span class="sxs-lookup"><span data-stu-id="c21db-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="c21db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21db-119">-DefaultProfile</span></span>
<span data-ttu-id="c21db-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c21db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c21db-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c21db-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="c21db-122">Gibt das Objekt des Datenträgerverschlüsselungsschlüssels für eine Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="c21db-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="c21db-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c21db-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c21db-124">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, mit dem ruhede Verschlüsselung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c21db-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="c21db-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c21db-125">-DiskSizeGB</span></span>
<span data-ttu-id="c21db-126">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="c21db-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c21db-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="c21db-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="c21db-128">"Verschlüsselungseinstellungen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="c21db-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="c21db-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="c21db-129">-EncryptionType</span></span>
<span data-ttu-id="c21db-130">Der Schlüsseltyp, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c21db-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="c21db-131">Verfügbare Werte sind: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="c21db-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="c21db-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="c21db-132">-DiskAccessId</span></span>
<span data-ttu-id="c21db-133">Ruft die ARM der Ressource "DiskAccess" für die Verwendung privater Endpunkte ab oder legt sie fest.</span><span class="sxs-lookup"><span data-stu-id="c21db-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="c21db-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c21db-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="c21db-135">Die Netzwerkzugriffsrichtlinie definiert die Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c21db-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="c21db-136">Mögliche Werte sind: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="c21db-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="c21db-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="c21db-137">-HyperVGeneration</span></span>
<span data-ttu-id="c21db-138">Die Hypervisorgenerierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="c21db-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="c21db-139">Gilt nur für Betriebssystemdatenträger.</span><span class="sxs-lookup"><span data-stu-id="c21db-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="c21db-140">Zulässige Werte sind V1 und V2.</span><span class="sxs-lookup"><span data-stu-id="c21db-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="c21db-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="c21db-141">-ImageReference</span></span>
<span data-ttu-id="c21db-142">Gibt den Bildverweis für eine Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="c21db-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="c21db-143">-Inkrementell</span><span class="sxs-lookup"><span data-stu-id="c21db-143">-Incremental</span></span>
<span data-ttu-id="c21db-144">Gibt eine inkrementelle Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="c21db-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="c21db-145">Inkrementelle Momentaufnahmen auf demselben Datenträger belegen weniger Speicherplatz als vollständige Momentaufnahmen und können beugt werden.</span><span class="sxs-lookup"><span data-stu-id="c21db-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21db-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c21db-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="c21db-147">Gibt den Schlüsselverschlüsselungsschlüssel für eine Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="c21db-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="c21db-148">-Location</span><span class="sxs-lookup"><span data-stu-id="c21db-148">-Location</span></span>
<span data-ttu-id="c21db-149">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="c21db-149">Specifies a location.</span></span>

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

### <span data-ttu-id="c21db-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="c21db-150">-OsType</span></span>
<span data-ttu-id="c21db-151">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="c21db-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="c21db-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c21db-152">-SkuName</span></span>
<span data-ttu-id="c21db-153">Gibt den Namen der SKU des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="c21db-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="c21db-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="c21db-154">-SourceResourceId</span></span>
<span data-ttu-id="c21db-155">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="c21db-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="c21db-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="c21db-156">-SourceUri</span></span>
<span data-ttu-id="c21db-157">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="c21db-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="c21db-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c21db-158">-StorageAccountId</span></span>
<span data-ttu-id="c21db-159">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="c21db-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="c21db-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="c21db-160">-Tag</span></span>
<span data-ttu-id="c21db-161">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c21db-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c21db-162">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c21db-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c21db-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c21db-163">-Confirm</span></span>
<span data-ttu-id="c21db-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c21db-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21db-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c21db-165">-WhatIf</span></span>
<span data-ttu-id="c21db-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c21db-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c21db-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c21db-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21db-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21db-168">CommonParameters</span></span>
<span data-ttu-id="c21db-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21db-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21db-170">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c21db-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21db-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c21db-171">INPUTS</span></span>

### <span data-ttu-id="c21db-172">System.String</span><span class="sxs-lookup"><span data-stu-id="c21db-172">System.String</span></span>

### <span data-ttu-id="c21db-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c21db-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c21db-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c21db-174">System.Int32</span></span>

### <span data-ttu-id="c21db-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c21db-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c21db-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="c21db-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="c21db-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c21db-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c21db-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="c21db-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="c21db-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="c21db-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="c21db-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c21db-180">OUTPUTS</span></span>

### <span data-ttu-id="c21db-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c21db-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c21db-182">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c21db-182">NOTES</span></span>

## <span data-ttu-id="c21db-183">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c21db-183">RELATED LINKS</span></span>
