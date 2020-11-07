---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849371"
---
# <span data-ttu-id="de576-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="de576-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="de576-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de576-102">SYNOPSIS</span></span>
<span data-ttu-id="de576-103">Erstellt ein konfigurierbares Datenträgerobjekt.</span><span class="sxs-lookup"><span data-stu-id="de576-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de576-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de576-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de576-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de576-105">DESCRIPTION</span></span>
<span data-ttu-id="de576-106">Mit dem Cmdlet **New-AzureRmDiskConfig** wird ein konfigurierbares Datenträgerobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="de576-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="de576-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de576-107">EXAMPLES</span></span>

### <span data-ttu-id="de576-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de576-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="de576-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="de576-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="de576-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="de576-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="de576-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="de576-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="de576-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="de576-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="de576-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="de576-113">PARAMETERS</span></span>

### <span data-ttu-id="de576-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="de576-114">-CreateOption</span></span>
<span data-ttu-id="de576-115">Gibt an, ob dieses Cmdlet einen Datenträger auf dem virtuellen Computer von einer Plattform oder einem Benutzerbild erstellt, einen leeren Datenträger erstellt oder einen vorhandenen Datenträger anfügt.</span><span class="sxs-lookup"><span data-stu-id="de576-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de576-116">-DefaultProfile</span></span>
<span data-ttu-id="de576-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de576-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de576-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de576-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="de576-119">Gibt das Datenträgerverschlüsselungsschlüssel Objekt auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="de576-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="de576-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="de576-120">-DiskSizeGB</span></span>
<span data-ttu-id="de576-121">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="de576-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="de576-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="de576-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="de576-123">Aktivieren Sie Verschlüsselungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="de576-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="de576-124">-Imagereference</span><span class="sxs-lookup"><span data-stu-id="de576-124">-ImageReference</span></span>
<span data-ttu-id="de576-125">Gibt den Bildverweis auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="de576-125">Specifies the image reference on a disk.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de576-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="de576-127">Gibt den Schlüssel Verschlüsselungsschlüssel auf einem Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="de576-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="de576-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="de576-128">-Location</span></span>
<span data-ttu-id="de576-129">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="de576-129">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="de576-130">-OsType</span></span>
<span data-ttu-id="de576-131">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="de576-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="de576-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="de576-132">-SkuName</span></span>
<span data-ttu-id="de576-133">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="de576-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="de576-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="de576-134">-SourceResourceId</span></span>
<span data-ttu-id="de576-135">Gibt die Quellressourcen-ID an.</span><span class="sxs-lookup"><span data-stu-id="de576-135">Specifies the  source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="de576-136">-SourceUri</span></span>
<span data-ttu-id="de576-137">Gibt den Quell-URI an.</span><span class="sxs-lookup"><span data-stu-id="de576-137">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="de576-138">-StorageAccountId</span></span>
<span data-ttu-id="de576-139">Gibt die Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="de576-139">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="de576-140">-Tag</span></span>
<span data-ttu-id="de576-141">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="de576-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="de576-142">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="de576-142">For example:</span></span>

<span data-ttu-id="de576-143">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="de576-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="de576-144">-Zone</span></span>
<span data-ttu-id="de576-145">Gibt die Liste der logischen Zonen für den Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="de576-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de576-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de576-146">-Confirm</span></span>
<span data-ttu-id="de576-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de576-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de576-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de576-148">-WhatIf</span></span>
<span data-ttu-id="de576-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de576-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de576-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de576-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de576-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de576-151">CommonParameters</span></span>
<span data-ttu-id="de576-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de576-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de576-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de576-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de576-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de576-154">INPUTS</span></span>

### <span data-ttu-id="de576-155">Keine</span><span class="sxs-lookup"><span data-stu-id="de576-155">None</span></span>
<span data-ttu-id="de576-156">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="de576-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de576-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de576-157">OUTPUTS</span></span>

### <span data-ttu-id="de576-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="de576-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="de576-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="de576-159">NOTES</span></span>

## <span data-ttu-id="de576-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de576-160">RELATED LINKS</span></span>

