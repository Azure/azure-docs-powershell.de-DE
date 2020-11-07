---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://go.microsoft.com/fwlink/?LinkId=690303
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 737a99fa59530ca37d32e2ca1c2c7d7e609ed225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664758"
---
# <span data-ttu-id="a6ae2-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6ae2-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="a6ae2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ae2-103">Erstellt oder aktualisiert ein Kennwort in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6ae2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6ae2-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ae2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="a6ae2-106">Das Cmdlet " **AzureKeyVaultSecret** " erstellt oder aktualisiert einen geheimen Schlüssel in einem schlüsseltresor im Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="a6ae2-107">Wenn der Schlüssel nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="a6ae2-108">Wenn der Schlüssel bereits vorhanden ist, wird mit diesem Cmdlet eine neue Version dieses geheimen Schlüssels erstellt.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="a6ae2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="a6ae2-110">Beispiel 1: Ändern des Werts eines geheimen Schlüssels mit Standardattributen</span><span class="sxs-lookup"><span data-stu-id="a6ae2-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="a6ae2-111">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Secret Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="a6ae2-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="a6ae2-113">Mit dem zweiten Befehl wird der Wert des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso geändert.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="a6ae2-114">Der geheime Wert wird zum in $Secret gespeicherten Wert.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="a6ae2-115">Beispiel 2: Ändern des Werts eines geheimen Schlüssels mithilfe benutzerdefinierter Attribute</span><span class="sxs-lookup"><span data-stu-id="a6ae2-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="a6ae2-116">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Secret Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="a6ae2-117">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="a6ae2-118">Die nächsten Befehle definieren benutzerdefinierte Attribute für das Ablaufdatum, Tags und den Kontexttyp und speichern die Attribute in Variablen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="a6ae2-119">Mit dem letzten Befehl werden die Werte des geheimen namens ITSecret im schlüsseltresor mit dem Namen contoso geändert, wobei die zuvor als Variablen angegebenen Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="a6ae2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6ae2-120">PARAMETERS</span></span>

### <span data-ttu-id="a6ae2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6ae2-121">-Confirm</span></span>
<span data-ttu-id="a6ae2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ae2-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a6ae2-123">-ContentType</span></span>
<span data-ttu-id="a6ae2-124">Gibt den Inhaltstyp eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="a6ae2-125">Wenn Sie den vorhandenen Inhaltstyp löschen möchten, geben Sie eine leere Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-126">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="a6ae2-126">-Disable</span></span>
<span data-ttu-id="a6ae2-127">Gibt an, dass dieses Cmdlet einen geheimen Schlüssel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="a6ae2-128">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="a6ae2-128">-Expires</span></span>
<span data-ttu-id="a6ae2-129">Gibt die Ablaufzeit als **DateTime** -Objekt für den geheimen Schlüssel an, den dieses Cmdlet aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="a6ae2-130">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="a6ae2-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="a6ae2-131">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="a6ae2-132">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-133">-Name</span><span class="sxs-lookup"><span data-stu-id="a6ae2-133">-Name</span></span>
<span data-ttu-id="a6ae2-134">Gibt den Namen des zu ändernden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="a6ae2-135">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="a6ae2-136">-NotBefore</span></span>
<span data-ttu-id="a6ae2-137">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="a6ae2-138">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-138">This parameter uses UTC.</span></span> <span data-ttu-id="a6ae2-139">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-140">-Secretvalue</span><span class="sxs-lookup"><span data-stu-id="a6ae2-140">-SecretValue</span></span>
<span data-ttu-id="a6ae2-141">Gibt den Wert für den geheimen Wert als **SecureString** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="a6ae2-142">Verwenden Sie zum Abrufen eines **SecureString** -Objekts das Cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="a6ae2-143">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6ae2-144">-Tag</span></span>
<span data-ttu-id="a6ae2-145">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a6ae2-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6ae2-146">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a6ae2-146">For example:</span></span>

<span data-ttu-id="a6ae2-147">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a6ae2-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-148">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="a6ae2-148">-VaultName</span></span>
<span data-ttu-id="a6ae2-149">Gibt den Namen des Schlüsseldepots an, zu dem dieser Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="a6ae2-150">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6ae2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ae2-151">-WhatIf</span></span>
<span data-ttu-id="a6ae2-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ae2-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ae2-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ae2-154">-DefaultProfile</span></span>
<span data-ttu-id="a6ae2-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6ae2-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ae2-156">CommonParameters</span></span>
<span data-ttu-id="a6ae2-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ae2-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ae2-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ae2-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ae2-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6ae2-159">INPUTS</span></span>

## <span data-ttu-id="a6ae2-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6ae2-160">OUTPUTS</span></span>

### <span data-ttu-id="a6ae2-161">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="a6ae2-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="a6ae2-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6ae2-162">NOTES</span></span>

## <span data-ttu-id="a6ae2-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6ae2-163">RELATED LINKS</span></span>

[<span data-ttu-id="a6ae2-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6ae2-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="a6ae2-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a6ae2-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
