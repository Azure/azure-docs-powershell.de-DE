---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850144"
---
# <span data-ttu-id="0ff2b-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0ff2b-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="0ff2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ff2b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ff2b-103">Erstellt ein konfigurierbares Datenträger Aktualisierungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ff2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ff2b-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ff2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ff2b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ff2b-106">Mit dem Cmdlet **New-AzureRmDiskUpdateConfig** wird ein konfigurierbares Datenträger Aktualisierungs Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="0ff2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ff2b-107">EXAMPLES</span></span>

### <span data-ttu-id="0ff2b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ff2b-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0ff2b-109">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="0ff2b-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0ff2b-111">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="0ff2b-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0ff2b-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0ff2b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ff2b-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="0ff2b-114">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="0ff2b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ff2b-115">PARAMETERS</span></span>

### <span data-ttu-id="0ff2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ff2b-116">-DefaultProfile</span></span>
<span data-ttu-id="0ff2b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ff2b-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ff2b-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="0ff2b-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="0ff2b-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0ff2b-120">-DiskSizeGB</span></span>
<span data-ttu-id="0ff2b-121">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0ff2b-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ff2b-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0ff2b-123">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0ff2b-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ff2b-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="0ff2b-125">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="0ff2b-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="0ff2b-126">-OsType</span></span>
<span data-ttu-id="0ff2b-127">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0ff2b-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0ff2b-128">-SkuName</span></span>
<span data-ttu-id="0ff2b-129">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="0ff2b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ff2b-130">-Tag</span></span>
<span data-ttu-id="0ff2b-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0ff2b-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0ff2b-132">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0ff2b-132">For example:</span></span>

<span data-ttu-id="0ff2b-133">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0ff2b-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0ff2b-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ff2b-134">-Confirm</span></span>
<span data-ttu-id="0ff2b-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ff2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ff2b-136">-WhatIf</span></span>
<span data-ttu-id="0ff2b-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ff2b-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ff2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ff2b-139">CommonParameters</span></span>
<span data-ttu-id="0ff2b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ff2b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ff2b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ff2b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ff2b-142">INPUTS</span></span>

### <span data-ttu-id="0ff2b-143">Keine</span><span class="sxs-lookup"><span data-stu-id="0ff2b-143">None</span></span>
<span data-ttu-id="0ff2b-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0ff2b-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ff2b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ff2b-145">OUTPUTS</span></span>

### <span data-ttu-id="0ff2b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0ff2b-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="0ff2b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ff2b-147">NOTES</span></span>

## <span data-ttu-id="0ff2b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ff2b-148">RELATED LINKS</span></span>

