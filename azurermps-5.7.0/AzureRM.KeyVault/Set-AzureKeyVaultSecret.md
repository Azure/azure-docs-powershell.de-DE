---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: c7968d915ab28dca6bf595e5339d2681962ecdea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664912"
---
# <span data-ttu-id="0522d-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0522d-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="0522d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0522d-102">SYNOPSIS</span></span>
<span data-ttu-id="0522d-103">Erstellt oder aktualisiert ein Kennwort in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0522d-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0522d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0522d-104">SYNTAX</span></span>

### <span data-ttu-id="0522d-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="0522d-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0522d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0522d-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0522d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0522d-107">DESCRIPTION</span></span>
<span data-ttu-id="0522d-108">Das Cmdlet " **AzureKeyVaultSecret** " erstellt oder aktualisiert einen geheimen Schlüssel in einem schlüsseltresor im Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0522d-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="0522d-109">Wenn der Schlüssel nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="0522d-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="0522d-110">Wenn der Schlüssel bereits vorhanden ist, wird mit diesem Cmdlet eine neue Version dieses geheimen Schlüssels erstellt.</span><span class="sxs-lookup"><span data-stu-id="0522d-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="0522d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0522d-111">EXAMPLES</span></span>

### <span data-ttu-id="0522d-112">Beispiel 1: Ändern des Werts eines geheimen Schlüssels mit Standardattributen</span><span class="sxs-lookup"><span data-stu-id="0522d-112">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="0522d-113">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Secret Variablen.</span><span class="sxs-lookup"><span data-stu-id="0522d-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="0522d-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0522d-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="0522d-115">Mit dem zweiten Befehl wird der Wert des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso geändert.</span><span class="sxs-lookup"><span data-stu-id="0522d-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="0522d-116">Der geheime Wert wird zum in $Secret gespeicherten Wert.</span><span class="sxs-lookup"><span data-stu-id="0522d-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="0522d-117">Beispiel 2: Ändern des Werts eines geheimen Schlüssels mithilfe benutzerdefinierter Attribute</span><span class="sxs-lookup"><span data-stu-id="0522d-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="0522d-118">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Secret Variablen.</span><span class="sxs-lookup"><span data-stu-id="0522d-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="0522d-119">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0522d-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="0522d-120">Die nächsten Befehle definieren benutzerdefinierte Attribute für das Ablaufdatum, Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="0522d-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="0522d-121">Mit dem letzten Befehl werden die Werte des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso geändert, wobei die zuvor als Variablen angegebenen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0522d-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="0522d-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="0522d-122">PARAMETERS</span></span>

### <span data-ttu-id="0522d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="0522d-123">-ContentType</span></span>
<span data-ttu-id="0522d-124">Gibt den Inhaltstyp eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="0522d-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="0522d-125">Wenn Sie den vorhandenen Inhaltstyp löschen möchten, geben Sie eine leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="0522d-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="0522d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0522d-126">-DefaultProfile</span></span>
<span data-ttu-id="0522d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0522d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0522d-128">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="0522d-128">-Disable</span></span>
<span data-ttu-id="0522d-129">Gibt an, dass dieses Cmdlet einen geheimen Schlüssel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0522d-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="0522d-130">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="0522d-130">-Expires</span></span>
<span data-ttu-id="0522d-131">Gibt die Ablaufzeit als **DateTime** -Objekt für den geheimen Schlüssel an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0522d-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="0522d-132">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="0522d-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0522d-133">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0522d-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="0522d-134">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0522d-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="0522d-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0522d-135">-InputObject</span></span>
<span data-ttu-id="0522d-136">Geheimes Objekt</span><span class="sxs-lookup"><span data-stu-id="0522d-136">Secret object</span></span>

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

### <span data-ttu-id="0522d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="0522d-137">-Name</span></span>
<span data-ttu-id="0522d-138">Gibt den Namen des zu ändernden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="0522d-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="0522d-139">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0522d-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="0522d-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="0522d-140">-NotBefore</span></span>
<span data-ttu-id="0522d-141">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0522d-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="0522d-142">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="0522d-142">This parameter uses UTC.</span></span> <span data-ttu-id="0522d-143">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0522d-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="0522d-144">-Secretvalue</span><span class="sxs-lookup"><span data-stu-id="0522d-144">-SecretValue</span></span>
<span data-ttu-id="0522d-145">Gibt den Wert für den geheimen Wert als **SecureString** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0522d-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="0522d-146">Verwenden Sie zum Abrufen eines **SecureString** -Objekts das Cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="0522d-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="0522d-147">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="0522d-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0522d-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="0522d-148">-Tag</span></span>
<span data-ttu-id="0522d-149">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="0522d-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0522d-150">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0522d-150">For example:</span></span>

<span data-ttu-id="0522d-151">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="0522d-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0522d-152">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0522d-152">-VaultName</span></span>
<span data-ttu-id="0522d-153">Gibt den Namen des Schlüsseldepots an, zu dem dieser Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="0522d-153">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="0522d-154">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0522d-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0522d-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0522d-155">-Confirm</span></span>
<span data-ttu-id="0522d-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0522d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0522d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0522d-157">-WhatIf</span></span>
<span data-ttu-id="0522d-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0522d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0522d-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0522d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0522d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0522d-160">CommonParameters</span></span>
<span data-ttu-id="0522d-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0522d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0522d-162">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0522d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0522d-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0522d-163">INPUTS</span></span>

### <span data-ttu-id="0522d-164">Keine</span><span class="sxs-lookup"><span data-stu-id="0522d-164">None</span></span>
<span data-ttu-id="0522d-165">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0522d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0522d-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0522d-166">OUTPUTS</span></span>

### <span data-ttu-id="0522d-167">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0522d-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="0522d-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="0522d-168">NOTES</span></span>

## <span data-ttu-id="0522d-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0522d-169">RELATED LINKS</span></span>

[<span data-ttu-id="0522d-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0522d-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="0522d-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0522d-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
