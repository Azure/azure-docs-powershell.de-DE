---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152596"
---
# <span data-ttu-id="f1240-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1240-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="f1240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1240-102">SYNOPSIS</span></span>
<span data-ttu-id="f1240-103">Aktualisiert die Attribute eines geheimen Schlüssels in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f1240-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f1240-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1240-104">SYNTAX</span></span>

### <span data-ttu-id="f1240-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1240-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1240-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f1240-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1240-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1240-107">DESCRIPTION</span></span>
<span data-ttu-id="f1240-108">Das **Cmdlet "Update-AzKeyVaultSecret"** aktualisiert bearbeitbare Attribute eines geheimen Schlüssels in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f1240-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f1240-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1240-109">EXAMPLES</span></span>

### <span data-ttu-id="f1240-110">Beispiel 1: Ändern der Attribute eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="f1240-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="f1240-111">Die ersten vier Befehle definieren Attribute für das Ablaufdatum, das NotBefore-Datum, Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1240-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="f1240-112">Der letzte Befehl ändert die Attribute für den geheimen Namen "HR" im Schlüsseltresor "ContosoVault" unter Verwendung der gespeicherten Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1240-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="f1240-113">Beispiel 2: Löschen der Tags und des Inhaltstyps eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="f1240-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="f1240-114">Mit diesem Befehl werden die Tags und der Inhaltstyp für die angegebene Version des geheimen Namens "HR" im Schlüsseltresor "Contoso" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f1240-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="f1240-115">Beispiel 3: Deaktivieren der aktuellen Version von geheimen Daten, deren Name mit der IT beginnt</span><span class="sxs-lookup"><span data-stu-id="f1240-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="f1240-116">Der erste Befehl speichert den Zeichenfolgenwert "Contoso" in der $Vault Variable.</span><span class="sxs-lookup"><span data-stu-id="f1240-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="f1240-117">Der zweite Befehl speichert den Zeichenfolgenwert IT in der $Prefix Variable.</span><span class="sxs-lookup"><span data-stu-id="f1240-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="f1240-118">Der dritte Befehl verwendet das Get-AzKeyVaultSecret-Cmdlet, um die geheimen Daten im angegebenen Schlüsseltresor zu erhalten, und übergibt diese anschließend an das **Where-Object-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="f1240-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="f1240-119">Das **Cmdlet "Where-Object"** filtert die geheimen Daten nach Namen, die mit den Zeichen IT beginnen.</span><span class="sxs-lookup"><span data-stu-id="f1240-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="f1240-120">Der Befehl gibt die geheimen Daten, die dem Filter entsprechen, Update-AzKeyVaultSecret an das Cmdlet weiter, wodurch sie deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="f1240-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="f1240-121">Beispiel 4: Festlegen des Inhaltstyps für alle Versionen eines geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="f1240-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="f1240-122">Die ersten drei Befehle definieren Zeichenfolgenvariablen, die für die Parameter *VaultName,* *Name* und *ContentType verwendet werden.*</span><span class="sxs-lookup"><span data-stu-id="f1240-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="f1240-123">Der vierte Befehl verwendet das Get-AzKeyVaultKey-Cmdlet, um die angegebenen Schlüssel zu erhalten, und gibt die Schlüssel an das cmdlet Update-AzKeyVaultSecret weiter, um den Inhaltstyp auf XML zu setzen.</span><span class="sxs-lookup"><span data-stu-id="f1240-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="f1240-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1240-124">PARAMETERS</span></span>

### <span data-ttu-id="f1240-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f1240-125">-ContentType</span></span>
<span data-ttu-id="f1240-126">Inhaltstyp des Geheimen</span><span class="sxs-lookup"><span data-stu-id="f1240-126">Secret's content type.</span></span>
<span data-ttu-id="f1240-127">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Inhaltstyps des Geheimen unverändert.</span><span class="sxs-lookup"><span data-stu-id="f1240-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="f1240-128">Entfernen Sie den vorhandenen Inhaltstypwert, indem Sie eine leere Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="f1240-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="f1240-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1240-129">-DefaultProfile</span></span>
<span data-ttu-id="f1240-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1240-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1240-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="f1240-131">-Enable</span></span>
<span data-ttu-id="f1240-132">Wenn vorhanden, aktivieren Sie einen geheimen Wert, wenn der Wert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="f1240-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="f1240-133">Deaktivieren Sie einen geheimen Wert, wenn der Wert falsch ist.</span><span class="sxs-lookup"><span data-stu-id="f1240-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="f1240-134">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Status "Aktiviert/Deaktiviert" des Geheimen unverändert.</span><span class="sxs-lookup"><span data-stu-id="f1240-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="f1240-135">-Expires</span><span class="sxs-lookup"><span data-stu-id="f1240-135">-Expires</span></span>
<span data-ttu-id="f1240-136">Die Ablaufzeit eines geheimen Datums in UTC.</span><span class="sxs-lookup"><span data-stu-id="f1240-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="f1240-137">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert der Ablaufzeit des Geheimen unverändert.</span><span class="sxs-lookup"><span data-stu-id="f1240-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="f1240-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1240-138">-InputObject</span></span>
<span data-ttu-id="f1240-139">Geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="f1240-139">Secret object</span></span>

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

### <span data-ttu-id="f1240-140">-Name</span><span class="sxs-lookup"><span data-stu-id="f1240-140">-Name</span></span>
<span data-ttu-id="f1240-141">Geheimer Name.</span><span class="sxs-lookup"><span data-stu-id="f1240-141">Secret name.</span></span>
<span data-ttu-id="f1240-142">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Namen des Tresors, die aktuell ausgewählte Umgebung und den geheimen Namen.</span><span class="sxs-lookup"><span data-stu-id="f1240-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="f1240-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f1240-143">-NotBefore</span></span>
<span data-ttu-id="f1240-144">Die UTC-Zeit, vor der der geheime Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1240-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="f1240-145">Wenn dieser Wert nicht angegeben wird, bleibt der vorhandene Wert des Attributs "NotBefore" des Geheimen unverändert.</span><span class="sxs-lookup"><span data-stu-id="f1240-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="f1240-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1240-146">-PassThru</span></span>
<span data-ttu-id="f1240-147">Das Cmdlet gibt das Objekt standardmäßig nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="f1240-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="f1240-148">Wenn dieser Schalter angegeben ist, geben Sie das geheime Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f1240-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="f1240-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1240-149">-Tag</span></span>
<span data-ttu-id="f1240-150">Eine Hashtable, die geheime Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1240-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="f1240-151">Wenn nichts angegeben wird, bleiben die vorhandenen Tags des geheimen Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="f1240-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="f1240-152">Entfernen Sie ein Tag, indem Sie eine leere Hashtable angeben.</span><span class="sxs-lookup"><span data-stu-id="f1240-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="f1240-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f1240-153">-VaultName</span></span>
<span data-ttu-id="f1240-154">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="f1240-154">Vault name.</span></span>
<span data-ttu-id="f1240-155">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f1240-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f1240-156">-Version</span><span class="sxs-lookup"><span data-stu-id="f1240-156">-Version</span></span>
<span data-ttu-id="f1240-157">Geheime Version.</span><span class="sxs-lookup"><span data-stu-id="f1240-157">Secret version.</span></span>
<span data-ttu-id="f1240-158">Das Cmdlet erstellt den FQDN eines Geheimen aus dem Tresornamen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="f1240-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="f1240-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1240-159">-Confirm</span></span>
<span data-ttu-id="f1240-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1240-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1240-161">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f1240-161">-WhatIf</span></span>
<span data-ttu-id="f1240-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1240-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1240-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1240-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1240-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1240-164">CommonParameters</span></span>
<span data-ttu-id="f1240-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1240-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1240-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1240-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1240-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1240-167">INPUTS</span></span>

### <span data-ttu-id="f1240-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f1240-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="f1240-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1240-169">OUTPUTS</span></span>

### <span data-ttu-id="f1240-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f1240-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="f1240-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f1240-171">NOTES</span></span>

## <span data-ttu-id="f1240-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f1240-172">RELATED LINKS</span></span>
