---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850007"
---
# <span data-ttu-id="819d0-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="819d0-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="819d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="819d0-102">SYNOPSIS</span></span>
<span data-ttu-id="819d0-103">Ruft die Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="819d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="819d0-104">SYNTAX</span></span>

### <span data-ttu-id="819d0-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="819d0-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="819d0-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="819d0-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="819d0-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="819d0-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="819d0-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="819d0-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="819d0-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="819d0-109">DESCRIPTION</span></span>
<span data-ttu-id="819d0-110">Das Cmdlet " **Get-AzureKeyVaultSecret** " erhält in einem schlüsseltresor Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="819d0-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="819d0-111">Dieses Cmdlet ruft einen bestimmten geheimen oder alle Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="819d0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="819d0-112">EXAMPLES</span></span>

### <span data-ttu-id="819d0-113">Beispiel 1: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="819d0-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="819d0-114">Mit diesem Befehl werden die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen contoso abgerufen.</span><span class="sxs-lookup"><span data-stu-id="819d0-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="819d0-115">Beispiel 2: Abrufen aller Versionen eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="819d0-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="819d0-116">Dieser Befehl ruft alle Versionen des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="819d0-117">Beispiel 3: Abrufen der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="819d0-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="819d0-118">Dieser Befehl ruft die aktuelle Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="819d0-119">Beispiel 4: Abrufen einer bestimmten Version eines bestimmten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="819d0-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="819d0-120">Dieser Befehl ruft eine bestimmte Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="819d0-121">Beispiel 5: Abrufen des nur-Text-Werts der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="819d0-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="819d0-122">Diese Befehle rufen die aktuelle Version eines geheimen namens ITSecret ab und zeigen dann den nur-Text-Wert dieses geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="819d0-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="819d0-123">Beispiel 6: Abrufen aller für diesen schlüsseltresor gelöschten, aber nicht bereinigten Geheimnisse</span><span class="sxs-lookup"><span data-stu-id="819d0-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="819d0-124">Dieser Befehl ruft alle Geheimnisse ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="819d0-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="819d0-125">Beispiel 7: Ruft den geheimen ITSecret ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="819d0-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="819d0-126">Dieser Befehl ruft den geheimen ITSecret ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="819d0-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="819d0-127">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum für diesen gelöschten Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="819d0-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="819d0-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="819d0-128">PARAMETERS</span></span>

### <span data-ttu-id="819d0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819d0-129">-DefaultProfile</span></span>
<span data-ttu-id="819d0-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="819d0-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="819d0-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="819d0-131">-IncludeVersions</span></span>
<span data-ttu-id="819d0-132">Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="819d0-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="819d0-133">Die aktuelle Version eines Geheimnisses ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="819d0-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="819d0-134">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="819d0-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="819d0-135">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des geheimen Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="819d0-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819d0-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="819d0-136">-InRemovedState</span></span>
<span data-ttu-id="819d0-137">Gibt an, ob die zuvor gelöschten Geheimnisse in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="819d0-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819d0-138">-Name</span><span class="sxs-lookup"><span data-stu-id="819d0-138">-Name</span></span>
<span data-ttu-id="819d0-139">Gibt den Namen des abzurufenden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="819d0-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819d0-140">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="819d0-140">-VaultName</span></span>
<span data-ttu-id="819d0-141">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="819d0-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="819d0-142">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="819d0-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="819d0-143">-Version</span><span class="sxs-lookup"><span data-stu-id="819d0-143">-Version</span></span>
<span data-ttu-id="819d0-144">Gibt die geheime Version an.</span><span class="sxs-lookup"><span data-stu-id="819d0-144">Specifies the secret version.</span></span>
<span data-ttu-id="819d0-145">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="819d0-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819d0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819d0-146">CommonParameters</span></span>
<span data-ttu-id="819d0-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819d0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819d0-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819d0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819d0-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="819d0-149">INPUTS</span></span>

### <span data-ttu-id="819d0-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="819d0-150">String</span></span>

## <span data-ttu-id="819d0-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="819d0-151">OUTPUTS</span></span>

### <span data-ttu-id="819d0-152">Liste<Microsoft. Azure. Commands. keyvault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. Secret, List<Microsoft. Azure. Commands. keyvault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="819d0-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="819d0-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="819d0-153">NOTES</span></span>

## <span data-ttu-id="819d0-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="819d0-154">RELATED LINKS</span></span>

[<span data-ttu-id="819d0-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="819d0-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="819d0-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="819d0-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="819d0-157">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="819d0-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

