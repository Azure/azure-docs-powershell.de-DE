---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996147"
---
# <span data-ttu-id="b36b2-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="b36b2-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="b36b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b36b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b36b2-103">Erstellt ein konfigurierbares Snapshot-Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="b36b2-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="b36b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b36b2-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b36b2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b36b2-105">DESCRIPTION</span></span>
<span data-ttu-id="b36b2-106">Mit dem Cmdlet **New-AzSnapshotUpdateConfig** wird ein konfigurierbares Snapshot-Aktualisierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="b36b2-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="b36b2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b36b2-107">EXAMPLES</span></span>

### <span data-ttu-id="b36b2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b36b2-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="b36b2-109">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="b36b2-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="b36b2-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b36b2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b36b2-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="b36b2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="b36b2-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b36b2-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b36b2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b36b2-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="b36b2-114">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b36b2-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b36b2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b36b2-115">PARAMETERS</span></span>

### <span data-ttu-id="b36b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36b2-116">-DefaultProfile</span></span>
<span data-ttu-id="b36b2-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b36b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36b2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b36b2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="b36b2-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="b36b2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="b36b2-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b36b2-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b36b2-121">Gibt die Ressourcen-ID des Datenträger Verschlüsselungs Satzes an, mit dem die Verschlüsselung im Ruhezustand aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b36b2-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="b36b2-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b36b2-122">-DiskSizeGB</span></span>
<span data-ttu-id="b36b2-123">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="b36b2-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b36b2-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b36b2-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b36b2-125">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="b36b2-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b36b2-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="b36b2-126">-EncryptionType</span></span>
<span data-ttu-id="b36b2-127">Der Typ des Schlüssels, der zum Verschlüsseln der Daten des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b36b2-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="b36b2-128">Die verfügbaren Werte lauten: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="b36b2-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="b36b2-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b36b2-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="b36b2-130">Gibt den Schlüssel Verschlüsselungsschlüssel für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="b36b2-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="b36b2-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="b36b2-131">-OsType</span></span>
<span data-ttu-id="b36b2-132">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="b36b2-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b36b2-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b36b2-133">-SkuName</span></span>
<span data-ttu-id="b36b2-134">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="b36b2-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="b36b2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b36b2-135">-Tag</span></span>
<span data-ttu-id="b36b2-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b36b2-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b36b2-137">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b36b2-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b36b2-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b36b2-138">-Confirm</span></span>
<span data-ttu-id="b36b2-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b36b2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b36b2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b36b2-140">-WhatIf</span></span>
<span data-ttu-id="b36b2-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b36b2-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b36b2-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b36b2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b36b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36b2-143">CommonParameters</span></span>
<span data-ttu-id="b36b2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36b2-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b36b2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36b2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b36b2-146">INPUTS</span></span>

### <span data-ttu-id="b36b2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b36b2-147">System.String</span></span>

### <span data-ttu-id="b36b2-148">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b36b2-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b36b2-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b36b2-149">System.Int32</span></span>

### <span data-ttu-id="b36b2-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b36b2-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b36b2-151">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b36b2-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b36b2-152">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="b36b2-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b36b2-153">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="b36b2-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b36b2-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b36b2-154">OUTPUTS</span></span>

### <span data-ttu-id="b36b2-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="b36b2-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="b36b2-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="b36b2-156">NOTES</span></span>

## <span data-ttu-id="b36b2-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b36b2-157">RELATED LINKS</span></span>
