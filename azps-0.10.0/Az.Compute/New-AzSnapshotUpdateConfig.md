---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844480"
---
# <span data-ttu-id="441b4-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="441b4-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="441b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="441b4-102">SYNOPSIS</span></span>
<span data-ttu-id="441b4-103">Erstellt ein konfigurierbares Snapshot-Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="441b4-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="441b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="441b4-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="441b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="441b4-105">DESCRIPTION</span></span>
<span data-ttu-id="441b4-106">Mit dem Cmdlet **New-AzSnapshotUpdateConfig** wird ein konfigurierbares Snapshot-Aktualisierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="441b4-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="441b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="441b4-107">EXAMPLES</span></span>

### <span data-ttu-id="441b4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="441b4-108">Example 1</span></span>
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

<span data-ttu-id="441b4-109">Mit dem ersten Befehl wird ein lokales leeres Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="441b4-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="441b4-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="441b4-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="441b4-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="441b4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="441b4-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="441b4-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="441b4-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="441b4-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="441b4-114">Mit diesem Befehl wird ein vorhandener Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="441b4-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="441b4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="441b4-115">PARAMETERS</span></span>

### <span data-ttu-id="441b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441b4-116">-DefaultProfile</span></span>
<span data-ttu-id="441b4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="441b4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="441b4-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="441b4-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="441b4-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="441b4-120">-DiskSizeGB</span></span>
<span data-ttu-id="441b4-121">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="441b4-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="441b4-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="441b4-123">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="441b4-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="441b4-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="441b4-125">Gibt den Schlüssel Verschlüsselungsschlüssel für einen Schnappschuss an.</span><span class="sxs-lookup"><span data-stu-id="441b4-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="441b4-126">-OsType</span></span>
<span data-ttu-id="441b4-127">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="441b4-127">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="441b4-128">-SkuName</span></span>
<span data-ttu-id="441b4-129">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="441b4-129">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="441b4-130">-Tag</span></span>
<span data-ttu-id="441b4-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="441b4-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="441b4-132">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="441b4-132">For example:</span></span>

<span data-ttu-id="441b4-133">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="441b4-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="441b4-134">-Confirm</span></span>
<span data-ttu-id="441b4-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="441b4-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441b4-136">-WhatIf</span></span>
<span data-ttu-id="441b4-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="441b4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="441b4-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="441b4-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="441b4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441b4-139">CommonParameters</span></span>
<span data-ttu-id="441b4-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441b4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441b4-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="441b4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441b4-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="441b4-142">INPUTS</span></span>

### <span data-ttu-id="441b4-143">Keine</span><span class="sxs-lookup"><span data-stu-id="441b4-143">None</span></span>
<span data-ttu-id="441b4-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="441b4-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="441b4-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="441b4-145">OUTPUTS</span></span>

### <span data-ttu-id="441b4-146">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="441b4-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="441b4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="441b4-147">NOTES</span></span>

## <span data-ttu-id="441b4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="441b4-148">RELATED LINKS</span></span>

