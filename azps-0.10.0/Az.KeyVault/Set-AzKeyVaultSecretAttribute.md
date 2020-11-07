---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842091"
---
# <span data-ttu-id="94d18-101">Set-AzKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="94d18-101">Set-AzKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="94d18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94d18-102">SYNOPSIS</span></span>
<span data-ttu-id="94d18-103">Aktualisiert Attribute eines Geheimnisses in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="94d18-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="94d18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94d18-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d18-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94d18-105">DESCRIPTION</span></span>
<span data-ttu-id="94d18-106">Das Cmdlet " **Satz-AzKeyVaultSecretAttribute** " aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="94d18-106">The **Set-AzKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="94d18-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94d18-107">EXAMPLES</span></span>

### <span data-ttu-id="94d18-108">Beispiel 1: Ändern der Attribute eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="94d18-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="94d18-109">Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, die Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="94d18-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="94d18-110">Der endgültige Befehl ändert die Attribute für den geheimen Namen HR im schlüsseltresor mit dem Namen ContosoVault unter Verwendung der gespeicherten Variablen.</span><span class="sxs-lookup"><span data-stu-id="94d18-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="94d18-111">Beispiel 2: Löschen der Kategorien und des Inhaltstyps für einen geheimen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="94d18-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="94d18-112">Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen namens HR im schlüsseltresor mit dem Namen "Contoso" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="94d18-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="94d18-113">Beispiel 3: Deaktivieren Sie die aktuelle Version von Secrets, deren Name mit ihr beginnt</span><span class="sxs-lookup"><span data-stu-id="94d18-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="94d18-114">Der erste Befehl speichert den Zeichenfolgenwert Contoso in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="94d18-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="94d18-115">Der zweite Befehl speichert den Zeichenfolgenwert in der $prefix Variablen.</span><span class="sxs-lookup"><span data-stu-id="94d18-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="94d18-116">Der dritte Befehl verwendet das Get-AzKeyVaultSecret-Cmdlet, um die Geheimnisse im angegebenen schlüsseltresor abzurufen, und übergibt diese Geheimnisse dann an das Cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="94d18-116">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="94d18-117">Das Cmdlet **Where-Object** filtert die Geheimnisse für Namen, die mit den Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="94d18-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="94d18-118">Der Befehl Pipes die Geheimnisse, die dem Filter entsprechen, mit dem Set-AzKeyVaultSecretAttribute-Cmdlet ab, wodurch Sie deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="94d18-118">The command pipes the secrets that match the filter to the Set-AzKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="94d18-119">Beispiel 4: Einrichten des ContentType für alle Versionen eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="94d18-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="94d18-120">Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *vaultname* , *Name* und *ContentType* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94d18-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="94d18-121">Der vierte Befehl verwendet das Get-AzKeyVaultKey-Cmdlet, um die angegebenen Schlüssel abzurufen, und leitet die Schlüssel an das Set-AzKeyVaultSecretAttribute-Cmdlet weiter, um den Inhaltstyp auf XML festzulegen.</span><span class="sxs-lookup"><span data-stu-id="94d18-121">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="94d18-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="94d18-122">PARAMETERS</span></span>

### <span data-ttu-id="94d18-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="94d18-123">-ContentType</span></span>
<span data-ttu-id="94d18-124">Gibt den Inhaltstyp eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="94d18-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="94d18-125">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am Inhaltstyp des aktuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="94d18-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="94d18-126">Wenn Sie den vorhandenen Inhaltstyp entfernen möchten, geben Sie eine leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="94d18-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="94d18-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d18-127">-DefaultProfile</span></span>
<span data-ttu-id="94d18-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94d18-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94d18-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="94d18-129">-Enable</span></span>
<span data-ttu-id="94d18-130">Gibt an, ob ein Schlüssel aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="94d18-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="94d18-131">Geben Sie $false an, um einen Schlüssel zu deaktivieren, oder $true, um einen geheimen Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="94d18-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="94d18-132">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am aktivierten oder deaktivierten Zustand des aktuellen Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="94d18-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="94d18-133">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="94d18-133">-Expires</span></span>
<span data-ttu-id="94d18-134">Gibt das Datum und die Uhrzeit an, zu dem ein geheimer abläuft.</span><span class="sxs-lookup"><span data-stu-id="94d18-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="94d18-135">-Name</span><span class="sxs-lookup"><span data-stu-id="94d18-135">-Name</span></span>
<span data-ttu-id="94d18-136">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="94d18-136">Specifies the name of a secret.</span></span> <span data-ttu-id="94d18-137">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="94d18-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d18-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="94d18-138">-NotBefore</span></span>
<span data-ttu-id="94d18-139">Gibt die koordinierte Weltzeit (Coordinated Universal Time, UTC) an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="94d18-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="94d18-140">Wenn Sie diesen Parameter nicht angeben, gibt es keine Änderung am NotBefore-Attribut des aktuellen Geheimnisses.</span><span class="sxs-lookup"><span data-stu-id="94d18-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="94d18-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94d18-141">-PassThru</span></span>
<span data-ttu-id="94d18-142">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="94d18-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94d18-143">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="94d18-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94d18-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="94d18-144">-Tag</span></span>
<span data-ttu-id="94d18-145">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="94d18-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94d18-146">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="94d18-146">For example:</span></span>

<span data-ttu-id="94d18-147">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="94d18-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="94d18-148">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="94d18-148">-VaultName</span></span>
<span data-ttu-id="94d18-149">Gibt den Namen des zu ändernden Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="94d18-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="94d18-150">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="94d18-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="94d18-151">-Version</span><span class="sxs-lookup"><span data-stu-id="94d18-151">-Version</span></span>
<span data-ttu-id="94d18-152">Gibt die Version eines geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="94d18-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="94d18-153">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="94d18-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="94d18-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94d18-154">-Confirm</span></span>
<span data-ttu-id="94d18-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94d18-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d18-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d18-156">-WhatIf</span></span>
<span data-ttu-id="94d18-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94d18-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d18-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94d18-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d18-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d18-159">CommonParameters</span></span>
<span data-ttu-id="94d18-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d18-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d18-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d18-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d18-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94d18-162">INPUTS</span></span>

### <span data-ttu-id="94d18-163">Keine</span><span class="sxs-lookup"><span data-stu-id="94d18-163">None</span></span>
<span data-ttu-id="94d18-164">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="94d18-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94d18-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94d18-165">OUTPUTS</span></span>

### <span data-ttu-id="94d18-166">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="94d18-166">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="94d18-167">Gibt das Microsoft. Azure. Commands. keyvault. Models. Secret-Objekt zurück, wenn passthru angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="94d18-167">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="94d18-168">Andernfalls wird Nothing zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94d18-168">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="94d18-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="94d18-169">NOTES</span></span>

## <span data-ttu-id="94d18-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94d18-170">RELATED LINKS</span></span>

[<span data-ttu-id="94d18-171">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94d18-171">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="94d18-172">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94d18-172">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="94d18-173">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="94d18-173">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
