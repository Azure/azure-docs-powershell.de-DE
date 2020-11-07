---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842139"
---
# <span data-ttu-id="540e6-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="540e6-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="540e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="540e6-102">SYNOPSIS</span></span>
<span data-ttu-id="540e6-103">Ruft schlüsseltresor Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="540e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="540e6-104">SYNTAX</span></span>

### <span data-ttu-id="540e6-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="540e6-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="540e6-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="540e6-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="540e6-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="540e6-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="540e6-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="540e6-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="540e6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="540e6-109">DESCRIPTION</span></span>
<span data-ttu-id="540e6-110">Das Cmdlet " **Get-AzKeyVaultKey** " ruft Azure Key Vault-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="540e6-111">Dieses Cmdlet ruft ein bestimmtes **Microsoft. Azure. Commands. keyvault. Models. keybundle** oder eine Liste aller **keybundle** -Objekte in einem schlüsseltresor oder nach Version ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="540e6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="540e6-112">EXAMPLES</span></span>

### <span data-ttu-id="540e6-113">Beispiel 1: Abrufen aller Schlüssel in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="540e6-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="540e6-114">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="540e6-115">Beispiel 2: Abrufen der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="540e6-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="540e6-116">Dieser Befehl ruft die aktuelle Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="540e6-117">Beispiel 3: Abrufen aller Versionen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="540e6-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="540e6-118">Dieser Befehl ruft alle Versionen mit dem Schlüssel "ITPfx" im Schlüssel vaultnamed Contoso ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="540e6-119">Beispiel 4: Abrufen einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="540e6-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="540e6-120">Dieser Befehl ruft eine bestimmte Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="540e6-121">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels überprüfen, indem Sie im $Key-Objekt navigieren.</span><span class="sxs-lookup"><span data-stu-id="540e6-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="540e6-122">Beispiel 5: Abrufen aller Schlüssel, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="540e6-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="540e6-123">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="540e6-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="540e6-124">Beispiel 6: Ruft den Schlüssel ITPfx ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="540e6-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="540e6-125">Dieser Befehl ruft den Schlüssel ITPfx ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="540e6-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="540e6-126">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="540e6-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="540e6-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="540e6-127">PARAMETERS</span></span>

### <span data-ttu-id="540e6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540e6-128">-DefaultProfile</span></span>
<span data-ttu-id="540e6-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="540e6-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="540e6-130">-IncludeVersions</span></span>
<span data-ttu-id="540e6-131">Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="540e6-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="540e6-132">Die aktuelle Version eines Schlüssels ist der erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="540e6-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="540e6-133">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="540e6-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="540e6-134">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="540e6-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="540e6-135">-InRemovedState</span></span>
<span data-ttu-id="540e6-136">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="540e6-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-137">-Name</span><span class="sxs-lookup"><span data-stu-id="540e6-137">-Name</span></span>
<span data-ttu-id="540e6-138">Gibt den Namen des abzurufenden Schlüsselpakets an.</span><span class="sxs-lookup"><span data-stu-id="540e6-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-139">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="540e6-139">-VaultName</span></span>
<span data-ttu-id="540e6-140">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="540e6-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="540e6-141">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="540e6-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-142">-Version</span><span class="sxs-lookup"><span data-stu-id="540e6-142">-Version</span></span>
<span data-ttu-id="540e6-143">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="540e6-143">Specifies the key version.</span></span>
<span data-ttu-id="540e6-144">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="540e6-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540e6-145">CommonParameters</span></span>
<span data-ttu-id="540e6-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540e6-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540e6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540e6-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="540e6-148">INPUTS</span></span>

### <span data-ttu-id="540e6-149">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="540e6-149">String</span></span>

## <span data-ttu-id="540e6-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="540e6-150">OUTPUTS</span></span>

### <span data-ttu-id="540e6-151">Liste<Microsoft. Azure. Commands. keyvault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. keybundle, List<Microsoft. Azure. Commands. keyvault. Models. DeletedKeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="540e6-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="540e6-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="540e6-152">NOTES</span></span>

## <span data-ttu-id="540e6-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="540e6-153">RELATED LINKS</span></span>

[<span data-ttu-id="540e6-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="540e6-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="540e6-155">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="540e6-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="540e6-156">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="540e6-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="540e6-157">Satz-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="540e6-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

