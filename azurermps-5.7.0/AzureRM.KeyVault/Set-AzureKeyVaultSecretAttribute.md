---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664911"
---
# <span data-ttu-id="616e4-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="616e4-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="616e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="616e4-102">SYNOPSIS</span></span>
<span data-ttu-id="616e4-103">Aktualisiert Attribute eines Geheimnisses in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="616e4-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="616e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="616e4-104">SYNTAX</span></span>

### <span data-ttu-id="616e4-105">Standard</span><span class="sxs-lookup"><span data-stu-id="616e4-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="616e4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="616e4-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="616e4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="616e4-107">DESCRIPTION</span></span>
<span data-ttu-id="616e4-108">Das Cmdlet " **Satz-AzureKeyVaultSecretAttribute** " aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="616e4-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="616e4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="616e4-109">EXAMPLES</span></span>

### <span data-ttu-id="616e4-110">Beispiel 1: Ändern der Attribute eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="616e4-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="616e4-111">Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, die Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="616e4-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="616e4-112">Der endgültige Befehl ändert die Attribute für den geheimen Namen HR im schlüsseltresor mit dem Namen ContosoVault unter Verwendung der gespeicherten Variablen.</span><span class="sxs-lookup"><span data-stu-id="616e4-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="616e4-113">Beispiel 2: Löschen der Kategorien und des Inhaltstyps für einen geheimen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="616e4-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="616e4-114">Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen namens HR im schlüsseltresor mit dem Namen "Contoso" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="616e4-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="616e4-115">Beispiel 3: Deaktivieren Sie die aktuelle Version von Secrets, deren Name mit ihr beginnt</span><span class="sxs-lookup"><span data-stu-id="616e4-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="616e4-116">Der erste Befehl speichert den Zeichenfolgenwert Contoso in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="616e4-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="616e4-117">Der zweite Befehl speichert den Zeichenfolgenwert in der $prefix Variablen.</span><span class="sxs-lookup"><span data-stu-id="616e4-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="616e4-118">Der dritte Befehl verwendet das Get-AzureKeyVaultSecret-Cmdlet, um die Geheimnisse im angegebenen schlüsseltresor abzurufen, und übergibt diese Geheimnisse dann an das Cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="616e4-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="616e4-119">Das Cmdlet **Where-Object** filtert die Geheimnisse für Namen, die mit den Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="616e4-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="616e4-120">Der Befehl Pipes die Geheimnisse, die dem Filter entsprechen, mit dem Set-AzureKeyVaultSecretAttribute-Cmdlet ab, wodurch Sie deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="616e4-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="616e4-121">Beispiel 4: Einrichten des ContentType für alle Versionen eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="616e4-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="616e4-122">Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *vaultname* , *Name* und *ContentType* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="616e4-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="616e4-123">Der vierte Befehl verwendet das Get-AzureKeyVaultKey-Cmdlet, um die angegebenen Schlüssel abzurufen, und leitet die Schlüssel an das Set-AzureKeyVaultSecretAttribute-Cmdlet weiter, um den Inhaltstyp auf XML festzulegen.</span><span class="sxs-lookup"><span data-stu-id="616e4-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="616e4-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="616e4-124">PARAMETERS</span></span>

### <span data-ttu-id="616e4-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="616e4-125">-ContentType</span></span>
<span data-ttu-id="616e4-126">Gibt den Inhaltstyp eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="616e4-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="616e4-127">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am Inhaltstyp des aktuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="616e4-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="616e4-128">Wenn Sie den vorhandenen Inhaltstyp entfernen möchten, geben Sie eine leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="616e4-128">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="616e4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="616e4-129">-DefaultProfile</span></span>
<span data-ttu-id="616e4-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="616e4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="616e4-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="616e4-131">-Enable</span></span>
<span data-ttu-id="616e4-132">Gibt an, ob ein Schlüssel aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="616e4-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="616e4-133">Geben Sie $false an, um einen Schlüssel zu deaktivieren, oder $true, um einen geheimen Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="616e4-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="616e4-134">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am aktivierten oder deaktivierten Zustand des aktuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="616e4-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-135">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="616e4-135">-Expires</span></span>
<span data-ttu-id="616e4-136">Gibt das Datum und die Uhrzeit an, zu dem ein geheimer abläuft.</span><span class="sxs-lookup"><span data-stu-id="616e4-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="616e4-137">-InputObject</span></span>
<span data-ttu-id="616e4-138">Geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="616e4-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-139">-Name</span><span class="sxs-lookup"><span data-stu-id="616e4-139">-Name</span></span>
<span data-ttu-id="616e4-140">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="616e4-140">Specifies the name of a secret.</span></span> <span data-ttu-id="616e4-141">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="616e4-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="616e4-142">-NotBefore</span></span>
<span data-ttu-id="616e4-143">Gibt die koordinierte Weltzeit (Coordinated Universal Time, UTC) an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="616e4-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="616e4-144">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am NotBefore-Attribut des aktuellen Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="616e4-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="616e4-145">-PassThru</span></span>
<span data-ttu-id="616e4-146">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="616e4-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="616e4-147">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="616e4-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="616e4-148">-Tag</span></span>
<span data-ttu-id="616e4-149">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="616e4-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="616e4-150">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="616e4-150">For example:</span></span>

<span data-ttu-id="616e4-151">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="616e4-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-152">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="616e4-152">-VaultName</span></span>
<span data-ttu-id="616e4-153">Gibt den Namen des zu ändernden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="616e4-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="616e4-154">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="616e4-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-155">-Version</span><span class="sxs-lookup"><span data-stu-id="616e4-155">-Version</span></span>
<span data-ttu-id="616e4-156">Gibt die Version eines geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="616e4-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="616e4-157">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="616e4-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="616e4-158">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="616e4-158">-Confirm</span></span>
<span data-ttu-id="616e4-159">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="616e4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="616e4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="616e4-160">-WhatIf</span></span>
<span data-ttu-id="616e4-161">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="616e4-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="616e4-162">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="616e4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="616e4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="616e4-163">CommonParameters</span></span>
<span data-ttu-id="616e4-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="616e4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="616e4-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="616e4-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="616e4-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="616e4-166">INPUTS</span></span>

### <span data-ttu-id="616e4-167">Keine</span><span class="sxs-lookup"><span data-stu-id="616e4-167">None</span></span>
<span data-ttu-id="616e4-168">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="616e4-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="616e4-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="616e4-169">OUTPUTS</span></span>

### <span data-ttu-id="616e4-170">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="616e4-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="616e4-171">Gibt das Microsoft. Azure. Commands. keyvault. Models. Secret-Objekt zurück, wenn passthru angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="616e4-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="616e4-172">Andernfalls wird Nothing zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="616e4-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="616e4-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="616e4-173">NOTES</span></span>

## <span data-ttu-id="616e4-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="616e4-174">RELATED LINKS</span></span>

[<span data-ttu-id="616e4-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="616e4-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="616e4-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="616e4-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="616e4-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="616e4-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
