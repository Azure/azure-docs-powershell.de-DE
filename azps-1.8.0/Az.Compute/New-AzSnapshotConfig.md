---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 293e894704509fe1b869ca23bd726c49f400de48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661515"
---
# <span data-ttu-id="3c0a5-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3c0a5-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="3c0a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0a5-103">Erstellt ein konfigurierbares Snapshot-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="3c0a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c0a5-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c0a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c0a5-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0a5-106">Mit dem Cmdlet **New-AzSnapshotConfig** wird ein konfigurierbares Snapshot-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="3c0a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c0a5-107">EXAMPLES</span></span>

### <span data-ttu-id="3c0a5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c0a5-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="3c0a5-109">Der erste Befehl erstellt ein lokales leeres snapshotobjekt mit der Größe 5GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="3c0a5-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="3c0a5-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="3c0a5-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3c0a5-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3c0a5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c0a5-113">PARAMETERS</span></span>

### <span data-ttu-id="3c0a5-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="3c0a5-114">-CreateOption</span></span>
<span data-ttu-id="3c0a5-115">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="3c0a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0a5-116">-DefaultProfile</span></span>
<span data-ttu-id="3c0a5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c0a5-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3c0a5-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="3c0a5-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="3c0a5-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3c0a5-120">-DiskSizeGB</span></span>
<span data-ttu-id="3c0a5-121">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3c0a5-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="3c0a5-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="3c0a5-123">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="3c0a5-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="3c0a5-124">-HyperVGeneration</span></span>
<span data-ttu-id="3c0a5-125">Die Hypervisor-Generierung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="3c0a5-126">Nur auf Betriebssystemdatenträger anwendbar.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="3c0a5-127">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="3c0a5-128">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="3c0a5-128">-ImageReference</span></span>
<span data-ttu-id="3c0a5-129">Gibt den Bildverweis auf einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-129">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="3c0a5-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3c0a5-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="3c0a5-131">Gibt den Schlüssel Verschlüsselungsschlüssel für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-131">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="3c0a5-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="3c0a5-132">-Location</span></span>
<span data-ttu-id="3c0a5-133">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-133">Specifies a location.</span></span>

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

### <span data-ttu-id="3c0a5-134">-OsType</span><span class="sxs-lookup"><span data-stu-id="3c0a5-134">-OsType</span></span>
<span data-ttu-id="3c0a5-135">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-135">Specifies the OS type.</span></span>

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

### <span data-ttu-id="3c0a5-136">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3c0a5-136">-SkuName</span></span>
<span data-ttu-id="3c0a5-137">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-137">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="3c0a5-138">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="3c0a5-138">-SourceResourceId</span></span>
<span data-ttu-id="3c0a5-139">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-139">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="3c0a5-140">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3c0a5-140">-SourceUri</span></span>
<span data-ttu-id="3c0a5-141">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-141">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="3c0a5-142">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3c0a5-142">-StorageAccountId</span></span>
<span data-ttu-id="3c0a5-143">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-143">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="3c0a5-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c0a5-144">-Tag</span></span>
<span data-ttu-id="3c0a5-145">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="3c0a5-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c0a5-146">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="3c0a5-146">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3c0a5-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c0a5-147">-Confirm</span></span>
<span data-ttu-id="3c0a5-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0a5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0a5-149">-WhatIf</span></span>
<span data-ttu-id="3c0a5-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c0a5-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0a5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0a5-152">CommonParameters</span></span>
<span data-ttu-id="3c0a5-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0a5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0a5-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0a5-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0a5-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c0a5-155">INPUTS</span></span>

### <span data-ttu-id="3c0a5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3c0a5-156">System.String</span></span>

### <span data-ttu-id="3c0a5-157">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3c0a5-157">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3c0a5-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3c0a5-158">System.Int32</span></span>

### <span data-ttu-id="3c0a5-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c0a5-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3c0a5-160">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="3c0a5-160">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="3c0a5-161">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3c0a5-161">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3c0a5-162">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="3c0a5-162">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="3c0a5-163">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="3c0a5-163">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="3c0a5-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c0a5-164">OUTPUTS</span></span>

### <span data-ttu-id="3c0a5-165">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="3c0a5-165">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="3c0a5-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c0a5-166">NOTES</span></span>

## <span data-ttu-id="3c0a5-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c0a5-167">RELATED LINKS</span></span>
