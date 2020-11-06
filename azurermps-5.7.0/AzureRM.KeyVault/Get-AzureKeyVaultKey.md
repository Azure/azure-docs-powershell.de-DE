---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500582"
---
# <span data-ttu-id="d7e91-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7e91-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="d7e91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7e91-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e91-103">Ruft schlüsseltresor Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7e91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7e91-104">SYNTAX</span></span>

### <span data-ttu-id="d7e91-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7e91-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e91-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="d7e91-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e91-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d7e91-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e91-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="d7e91-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e91-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="d7e91-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7e91-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="d7e91-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7e91-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7e91-111">DESCRIPTION</span></span>
<span data-ttu-id="d7e91-112">Das Cmdlet " **Get-AzureKeyVaultKey** " ruft Azure Key Vault-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="d7e91-113">Dieses Cmdlet ruft ein bestimmtes **Microsoft. Azure. Commands. keyvault. Models. keybundle** oder eine Liste aller **keybundle** -Objekte in einem schlüsseltresor oder nach Version ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="d7e91-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7e91-114">EXAMPLES</span></span>

### <span data-ttu-id="d7e91-115">Beispiel 1: Abrufen aller Schlüssel in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d7e91-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="d7e91-116">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7e91-117">Beispiel 2: Abrufen der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7e91-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="d7e91-118">Dieser Befehl ruft die aktuelle Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7e91-119">Beispiel 3: Abrufen aller Versionen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7e91-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="d7e91-120">Dieser Befehl ruft alle Versionen mit dem Schlüssel "ITPfx" im Schlüssel vaultnamed Contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="d7e91-121">Beispiel 4: Abrufen einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7e91-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="d7e91-122">Dieser Befehl ruft eine bestimmte Version des Schlüssels mit dem Namen ITPfx im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="d7e91-123">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels überprüfen, indem Sie im $Key-Objekt navigieren.</span><span class="sxs-lookup"><span data-stu-id="d7e91-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="d7e91-124">Beispiel 5: Abrufen aller Schlüssel, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden.</span><span class="sxs-lookup"><span data-stu-id="d7e91-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d7e91-125">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="d7e91-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7e91-126">Beispiel 6: Ruft den Schlüssel ITPfx ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="d7e91-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="d7e91-127">Dieser Befehl ruft den Schlüssel ITPfx ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="d7e91-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d7e91-128">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="d7e91-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="d7e91-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7e91-129">PARAMETERS</span></span>

### <span data-ttu-id="d7e91-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e91-130">-DefaultProfile</span></span>
<span data-ttu-id="d7e91-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7e91-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7e91-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d7e91-132">-IncludeVersions</span></span>
<span data-ttu-id="d7e91-133">Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="d7e91-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="d7e91-134">Die aktuelle Version eines Schlüssels ist der erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="d7e91-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="d7e91-135">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="d7e91-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="d7e91-136">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="d7e91-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7e91-137">-InputObject</span></span>
<span data-ttu-id="d7e91-138">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7e91-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d7e91-139">-InRemovedState</span></span>
<span data-ttu-id="d7e91-140">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7e91-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-141">-Name</span><span class="sxs-lookup"><span data-stu-id="d7e91-141">-Name</span></span>
<span data-ttu-id="d7e91-142">Gibt den Namen des abzurufenden Schlüsselpakets an.</span><span class="sxs-lookup"><span data-stu-id="d7e91-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-143">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d7e91-143">-VaultName</span></span>
<span data-ttu-id="d7e91-144">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="d7e91-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="d7e91-145">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d7e91-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-146">-Version</span><span class="sxs-lookup"><span data-stu-id="d7e91-146">-Version</span></span>
<span data-ttu-id="d7e91-147">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="d7e91-147">Specifies the key version.</span></span>
<span data-ttu-id="d7e91-148">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="d7e91-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7e91-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e91-149">CommonParameters</span></span>
<span data-ttu-id="d7e91-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e91-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e91-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e91-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e91-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7e91-152">INPUTS</span></span>

### <span data-ttu-id="d7e91-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d7e91-153">String</span></span>

## <span data-ttu-id="d7e91-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7e91-154">OUTPUTS</span></span>

### <span data-ttu-id="d7e91-155">List<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7e91-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d7e91-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7e91-156">NOTES</span></span>

## <span data-ttu-id="d7e91-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7e91-157">RELATED LINKS</span></span>

[<span data-ttu-id="d7e91-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7e91-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="d7e91-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7e91-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="d7e91-160">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d7e91-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="d7e91-161">Satz-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d7e91-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

