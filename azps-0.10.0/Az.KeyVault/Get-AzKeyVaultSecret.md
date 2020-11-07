---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843888"
---
# <span data-ttu-id="3d71d-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3d71d-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="3d71d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d71d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d71d-103">Ruft die Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="3d71d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d71d-104">SYNTAX</span></span>

### <span data-ttu-id="3d71d-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d71d-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d71d-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="3d71d-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d71d-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="3d71d-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d71d-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="3d71d-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d71d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d71d-109">DESCRIPTION</span></span>
<span data-ttu-id="3d71d-110">Das Cmdlet " **Get-AzKeyVaultSecret** " erhält in einem schlüsseltresor Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="3d71d-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="3d71d-111">Dieses Cmdlet ruft einen bestimmten geheimen oder alle Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="3d71d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d71d-112">EXAMPLES</span></span>

### <span data-ttu-id="3d71d-113">Beispiel 1: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="3d71d-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="3d71d-114">Mit diesem Befehl werden die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen contoso abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3d71d-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d71d-115">Beispiel 2: Abrufen aller Versionen eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d71d-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="3d71d-116">Dieser Befehl ruft alle Versionen des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d71d-117">Beispiel 3: Abrufen der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d71d-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="3d71d-118">Dieser Befehl ruft die aktuelle Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d71d-119">Beispiel 4: Abrufen einer bestimmten Version eines bestimmten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="3d71d-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="3d71d-120">Dieser Befehl ruft eine bestimmte Version des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d71d-121">Beispiel 5: Abrufen des nur-Text-Werts der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3d71d-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="3d71d-122">Diese Befehle rufen die aktuelle Version eines geheimen namens ITSecret ab und zeigen dann den nur-Text-Wert dieses geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="3d71d-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="3d71d-123">Beispiel 6: Abrufen aller für diesen schlüsseltresor gelöschten, aber nicht bereinigten Geheimnisse</span><span class="sxs-lookup"><span data-stu-id="3d71d-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="3d71d-124">Dieser Befehl ruft alle Geheimnisse ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="3d71d-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="3d71d-125">Beispiel 7: Ruft den geheimen ITSecret ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d71d-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="3d71d-126">Dieser Befehl ruft den geheimen ITSecret ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="3d71d-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="3d71d-127">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum für diesen gelöschten Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="3d71d-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="3d71d-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d71d-128">PARAMETERS</span></span>

### <span data-ttu-id="3d71d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d71d-129">-DefaultProfile</span></span>
<span data-ttu-id="3d71d-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d71d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d71d-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="3d71d-131">-IncludeVersions</span></span>
<span data-ttu-id="3d71d-132">Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="3d71d-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="3d71d-133">Die aktuelle Version eines Geheimnisses ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="3d71d-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="3d71d-134">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="3d71d-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="3d71d-135">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des geheimen Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="3d71d-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="3d71d-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3d71d-136">-InRemovedState</span></span>
<span data-ttu-id="3d71d-137">Gibt an, ob die zuvor gelöschten Geheimnisse in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d71d-137">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="3d71d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="3d71d-138">-Name</span></span>
<span data-ttu-id="3d71d-139">Gibt den Namen des abzurufenden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="3d71d-139">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="3d71d-140">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="3d71d-140">-VaultName</span></span>
<span data-ttu-id="3d71d-141">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="3d71d-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="3d71d-142">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3d71d-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="3d71d-143">-Version</span><span class="sxs-lookup"><span data-stu-id="3d71d-143">-Version</span></span>
<span data-ttu-id="3d71d-144">Gibt die geheime Version an.</span><span class="sxs-lookup"><span data-stu-id="3d71d-144">Specifies the secret version.</span></span>
<span data-ttu-id="3d71d-145">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="3d71d-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="3d71d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d71d-146">CommonParameters</span></span>
<span data-ttu-id="3d71d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d71d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d71d-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d71d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d71d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d71d-149">INPUTS</span></span>

### <span data-ttu-id="3d71d-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3d71d-150">String</span></span>

## <span data-ttu-id="3d71d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d71d-151">OUTPUTS</span></span>

### <span data-ttu-id="3d71d-152">Liste<Microsoft. Azure. Commands. keyvault. Models. SecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. Secret, List<Microsoft. Azure. Commands. keyvault. Models. DeletedSecretIdentityItem>, Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="3d71d-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="3d71d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d71d-153">NOTES</span></span>

## <span data-ttu-id="3d71d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d71d-154">RELATED LINKS</span></span>

[<span data-ttu-id="3d71d-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3d71d-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="3d71d-156">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="3d71d-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="3d71d-157">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3d71d-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

