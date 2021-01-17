---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467672"
---
# <span data-ttu-id="807df-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="807df-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="807df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="807df-102">SYNOPSIS</span></span>
<span data-ttu-id="807df-103">Erstellt oder aktualisiert einen geheimen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="807df-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="807df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="807df-104">SYNTAX</span></span>

### <span data-ttu-id="807df-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="807df-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="807df-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="807df-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="807df-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="807df-107">DESCRIPTION</span></span>
<span data-ttu-id="807df-108">Das **Cmdlet Set-AzKeyVaultSecret** erstellt oder aktualisiert einen geheimen Schlüssel in einem Schlüsseltresor im Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="807df-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="807df-109">Wenn das Geheimnis nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="807df-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="807df-110">Wenn das Geheimnis bereits vorhanden ist, erstellt dieses Cmdlet eine neue Version dieses Geheimen.</span><span class="sxs-lookup"><span data-stu-id="807df-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="807df-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="807df-111">EXAMPLES</span></span>

### <span data-ttu-id="807df-112">Beispiel 1: Ändern des Werts eines geheimen Schlüssels mithilfe von Standardattributen</span><span class="sxs-lookup"><span data-stu-id="807df-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="807df-113">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Secret Variable.</span><span class="sxs-lookup"><span data-stu-id="807df-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="807df-114">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="807df-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="807df-115">Der zweite Befehl ändert den Wert des geheimen Namens "ITSecret" im Schlüsseltresor "Contoso".</span><span class="sxs-lookup"><span data-stu-id="807df-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="807df-116">Der geheime Wert wird zu dem Wert, der in der Datei $Secret.</span><span class="sxs-lookup"><span data-stu-id="807df-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="807df-117">Beispiel 2: Ändern des Werts eines geheimen Schlüssels mithilfe von benutzerdefinierten Attributen</span><span class="sxs-lookup"><span data-stu-id="807df-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="807df-118">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Secret Variable.</span><span class="sxs-lookup"><span data-stu-id="807df-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="807df-119">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="807df-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="807df-120">Mit den nächsten Befehlen werden benutzerdefinierte Attribute für das Ablaufdatum, Tags und den Kontexttyp definiert und die Attribute in Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="807df-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="807df-121">Der letzte Befehl ändert die Werte des geheimen Namens "ITSecret" im Schlüsseltresor "Contoso", indem die zuvor als Variablen angegebenen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="807df-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="807df-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="807df-122">PARAMETERS</span></span>

### <span data-ttu-id="807df-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="807df-123">-ContentType</span></span>
<span data-ttu-id="807df-124">Gibt den Inhaltstyp eines geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="807df-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="807df-125">Um den vorhandenen Inhaltstyp zu löschen, geben Sie eine leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="807df-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="807df-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807df-126">-DefaultProfile</span></span>
<span data-ttu-id="807df-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="807df-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="807df-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="807df-128">-Disable</span></span>
<span data-ttu-id="807df-129">Gibt an, dass dieses Cmdlet einen geheimen Schlüssel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="807df-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="807df-130">-Expires</span><span class="sxs-lookup"><span data-stu-id="807df-130">-Expires</span></span>
<span data-ttu-id="807df-131">Gibt die Ablaufzeit als **"DateTime"-Objekt** für das Geheime an, das dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="807df-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="807df-132">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="807df-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="807df-133">Verwenden Sie das Get-Date-Cmdlet, um ein **"DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="807df-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="807df-134">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="807df-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="807df-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="807df-135">-InputObject</span></span>
<span data-ttu-id="807df-136">Geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="807df-136">Secret object</span></span>

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

### <span data-ttu-id="807df-137">-Name</span><span class="sxs-lookup"><span data-stu-id="807df-137">-Name</span></span>
<span data-ttu-id="807df-138">Gibt den Namen eines geheimen Schlüssels an, der geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="807df-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="807df-139">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="807df-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="807df-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="807df-140">-NotBefore</span></span>
<span data-ttu-id="807df-141">Gibt die Uhrzeit als **"DateTime"-Objekt** an, vor dem das Geheime nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="807df-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="807df-142">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="807df-142">This parameter uses UTC.</span></span> <span data-ttu-id="807df-143">Verwenden Sie das Get-Date-Cmdlet, um ein **"DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="807df-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="807df-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="807df-144">-SecretValue</span></span>
<span data-ttu-id="807df-145">Gibt den Wert für das Geheime als **SecureString-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="807df-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="807df-146">Verwenden Sie zum **Abrufen eines SecureString-Objekts** **das Cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="807df-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="807df-147">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="807df-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="807df-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="807df-148">-Tag</span></span>
<span data-ttu-id="807df-149">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="807df-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="807df-150">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="807df-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="807df-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="807df-151">-VaultName</span></span>
<span data-ttu-id="807df-152">Gibt den Namen des Schlüsseltresor an, zu dem dieser Geheimschlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="807df-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="807df-153">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="807df-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="807df-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="807df-154">-Confirm</span></span>
<span data-ttu-id="807df-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="807df-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807df-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="807df-156">-WhatIf</span></span>
<span data-ttu-id="807df-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="807df-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="807df-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="807df-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="807df-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807df-159">CommonParameters</span></span>
<span data-ttu-id="807df-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="807df-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807df-161">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="807df-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807df-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="807df-162">INPUTS</span></span>

### <span data-ttu-id="807df-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="807df-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="807df-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="807df-164">OUTPUTS</span></span>

### <span data-ttu-id="807df-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="807df-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="807df-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="807df-166">NOTES</span></span>

## <span data-ttu-id="807df-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="807df-167">RELATED LINKS</span></span>

[<span data-ttu-id="807df-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="807df-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="807df-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="807df-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
