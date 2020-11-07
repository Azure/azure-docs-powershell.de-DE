---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664854"
---
# <span data-ttu-id="bc775-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bc775-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="bc775-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc775-102">SYNOPSIS</span></span>
<span data-ttu-id="bc775-103">Aktualisiert Attribute eines Geheimnisses in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="bc775-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc775-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc775-104">SYNTAX</span></span>

### <span data-ttu-id="bc775-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc775-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc775-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bc775-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc775-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc775-107">DESCRIPTION</span></span>
<span data-ttu-id="bc775-108">Das Cmdlet **Update-AzureKeyVaultSecret** aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="bc775-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="bc775-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc775-109">EXAMPLES</span></span>

### <span data-ttu-id="bc775-110">Beispiel 1: Ändern der Attribute eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bc775-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="bc775-111">Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, die Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="bc775-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="bc775-112">Der endgültige Befehl ändert die Attribute für den geheimen Namen HR im schlüsseltresor mit dem Namen ContosoVault unter Verwendung der gespeicherten Variablen.</span><span class="sxs-lookup"><span data-stu-id="bc775-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="bc775-113">Beispiel 2: Löschen der Kategorien und des Inhaltstyps für einen geheimen Schlüssel</span><span class="sxs-lookup"><span data-stu-id="bc775-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="bc775-114">Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen namens HR im schlüsseltresor mit dem Namen "Contoso" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bc775-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="bc775-115">Beispiel 3: Deaktivieren Sie die aktuelle Version von Secrets, deren Name mit ihr beginnt</span><span class="sxs-lookup"><span data-stu-id="bc775-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="bc775-116">Der erste Befehl speichert den Zeichenfolgenwert Contoso in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="bc775-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="bc775-117">Der zweite Befehl speichert den Zeichenfolgenwert in der $prefix Variablen.</span><span class="sxs-lookup"><span data-stu-id="bc775-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="bc775-118">Der dritte Befehl verwendet das Get-AzureKeyVaultSecret-Cmdlet, um die Geheimnisse im angegebenen schlüsseltresor abzurufen, und übergibt diese Geheimnisse dann an das Cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="bc775-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="bc775-119">Das Cmdlet **Where-Object** filtert die Geheimnisse für Namen, die mit den Zeichen beginnen.</span><span class="sxs-lookup"><span data-stu-id="bc775-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="bc775-120">Der Befehl Pipes die Geheimnisse, die dem Filter entsprechen, mit dem Update-AzureKeyVaultSecret-Cmdlet ab, wodurch Sie deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="bc775-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="bc775-121">Beispiel 4: Einrichten des ContentType für alle Versionen eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="bc775-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="bc775-122">Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *vaultname* , *Name* und *ContentType* verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc775-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="bc775-123">Der vierte Befehl verwendet das Get-AzureKeyVaultKey-Cmdlet, um die angegebenen Schlüssel abzurufen, und leitet die Schlüssel an das Update-AzureKeyVaultSecret-Cmdlet weiter, um den Inhaltstyp auf XML festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bc775-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="bc775-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc775-124">PARAMETERS</span></span>

### <span data-ttu-id="bc775-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="bc775-125">-ContentType</span></span>
<span data-ttu-id="bc775-126">Inhaltstyp "Secret".</span><span class="sxs-lookup"><span data-stu-id="bc775-126">Secret's content type.</span></span>
<span data-ttu-id="bc775-127">Wenn Sie nicht angegeben wird, bleibt der vorhandene Wert des geheimen Inhaltstyps unverändert.</span><span class="sxs-lookup"><span data-stu-id="bc775-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="bc775-128">Entfernen Sie den vorhandenen Inhaltstyp Wert, indem Sie eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="bc775-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc775-129">-DefaultProfile</span></span>
<span data-ttu-id="bc775-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc775-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="bc775-131">-Enable</span></span>
<span data-ttu-id="bc775-132">Falls vorhanden, aktivieren Sie einen geheimen Schlüssel, wenn der Wert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="bc775-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="bc775-133">Deaktivieren Sie einen geheimen Schlüssel, wenn der Wert false ist.</span><span class="sxs-lookup"><span data-stu-id="bc775-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="bc775-134">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert für den aktivierten/deaktivierten Status von Secret unverändert.</span><span class="sxs-lookup"><span data-stu-id="bc775-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-135">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="bc775-135">-Expires</span></span>
<span data-ttu-id="bc775-136">Die Ablaufzeit eines Geheimnisses in UTC-Zeit.</span><span class="sxs-lookup"><span data-stu-id="bc775-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="bc775-137">Wenn Sie nicht angegeben wird, bleibt der vorhandene Wert der Verfallszeit des Secrets unverändert.</span><span class="sxs-lookup"><span data-stu-id="bc775-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bc775-138">-InputObject</span></span>
<span data-ttu-id="bc775-139">Geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="bc775-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-140">-Name</span><span class="sxs-lookup"><span data-stu-id="bc775-140">-Name</span></span>
<span data-ttu-id="bc775-141">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="bc775-141">Secret name.</span></span>
<span data-ttu-id="bc775-142">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und geheimem Namen.</span><span class="sxs-lookup"><span data-stu-id="bc775-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="bc775-143">-NotBefore</span></span>
<span data-ttu-id="bc775-144">Die UTC-Zeit, vor der Secret nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bc775-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="bc775-145">Wenn nicht angegeben, bleibt der vorhandene Wert des NotBefore-Attributs des geheimen Attributs unverändert.</span><span class="sxs-lookup"><span data-stu-id="bc775-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc775-146">-PassThru</span></span>
<span data-ttu-id="bc775-147">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="bc775-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="bc775-148">Wenn dieser Schalter angegeben ist, geben Sie Secret-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="bc775-148">If this switch is specified, return Secret object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc775-149">-Tag</span></span>
<span data-ttu-id="bc775-150">Eine Hashtable, die geheime Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc775-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="bc775-151">Wenn nicht angegeben, bleiben die vorhandenen Tags des geheimen Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="bc775-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="bc775-152">Entfernen Sie ein Tag, indem Sie eine leere Hashtable angeben.</span><span class="sxs-lookup"><span data-stu-id="bc775-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-153">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="bc775-153">-VaultName</span></span>
<span data-ttu-id="bc775-154">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="bc775-154">Vault name.</span></span>
<span data-ttu-id="bc775-155">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bc775-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-156">-Version</span><span class="sxs-lookup"><span data-stu-id="bc775-156">-Version</span></span>
<span data-ttu-id="bc775-157">Secret-Version.</span><span class="sxs-lookup"><span data-stu-id="bc775-157">Secret version.</span></span>
<span data-ttu-id="bc775-158">Cmdlet erstellt den FQDN eines geheimen Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung, geheimem Namen und geheimer Version.</span><span class="sxs-lookup"><span data-stu-id="bc775-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc775-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc775-159">-Confirm</span></span>
<span data-ttu-id="bc775-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc775-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc775-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc775-161">-WhatIf</span></span>
<span data-ttu-id="bc775-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc775-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc775-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc775-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc775-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc775-164">CommonParameters</span></span>
<span data-ttu-id="bc775-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc775-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc775-166">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc775-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc775-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc775-167">INPUTS</span></span>

### <span data-ttu-id="bc775-168">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bc775-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="bc775-169">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc775-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bc775-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc775-170">OUTPUTS</span></span>

### <span data-ttu-id="bc775-171">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="bc775-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="bc775-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc775-172">NOTES</span></span>

## <span data-ttu-id="bc775-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc775-173">RELATED LINKS</span></span>
