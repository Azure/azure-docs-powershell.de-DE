---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: e5ec1e2377b9a1c04fc10ce976bd800227baabed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502701"
---
# <span data-ttu-id="21f39-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21f39-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="21f39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21f39-102">SYNOPSIS</span></span>
<span data-ttu-id="21f39-103">Löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="21f39-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21f39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21f39-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f39-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21f39-105">DESCRIPTION</span></span>
<span data-ttu-id="21f39-106">Das Remove-AzureKeyVaultSecret-Cmdlet löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="21f39-106">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="21f39-107">Wenn das Geheimnis versehentlich gelöscht wurde, kann das Geheimnis mithilfe von Undo-AzureKeyVaultSecretRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="21f39-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="21f39-108">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="21f39-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="21f39-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21f39-109">EXAMPLES</span></span>

### <span data-ttu-id="21f39-110">Beispiel 1: Entfernen eines Geheimnisses aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="21f39-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="21f39-111">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso".</span><span class="sxs-lookup"><span data-stu-id="21f39-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="21f39-112">Beispiel 2: Entfernen eines Geheimnisses aus einem schlüsseltresor ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="21f39-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="21f39-113">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="21f39-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="21f39-114">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="21f39-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="21f39-115">Beispiel 3: Dauerhaftes Löschen eines gelöschten Geheimnisses aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="21f39-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="21f39-116">Mit diesem Befehl wird der geheime Name FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso" endgültig verschoben.</span><span class="sxs-lookup"><span data-stu-id="21f39-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="21f39-117">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="21f39-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="21f39-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="21f39-118">PARAMETERS</span></span>

### <span data-ttu-id="21f39-119">-Force</span><span class="sxs-lookup"><span data-stu-id="21f39-119">-Force</span></span>
<span data-ttu-id="21f39-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="21f39-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21f39-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="21f39-121">-InRemovedState</span></span>
<span data-ttu-id="21f39-122">Wenn vorhanden, wird das zuvor gelöschte Geheimnis endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="21f39-122">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="21f39-123">-Name</span><span class="sxs-lookup"><span data-stu-id="21f39-123">-Name</span></span>
<span data-ttu-id="21f39-124">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="21f39-124">Specifies the name of a secret.</span></span>
<span data-ttu-id="21f39-125">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="21f39-125">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="21f39-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21f39-126">-PassThru</span></span>
<span data-ttu-id="21f39-127">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. Secret** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="21f39-127">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="21f39-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="21f39-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21f39-129">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="21f39-129">-VaultName</span></span>
<span data-ttu-id="21f39-130">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="21f39-130">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="21f39-131">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="21f39-131">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="21f39-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21f39-132">-Confirm</span></span>
<span data-ttu-id="21f39-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21f39-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f39-134">-WhatIf</span></span>
<span data-ttu-id="21f39-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21f39-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f39-136">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21f39-136">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f39-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21f39-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f39-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f39-138">-DefaultProfile</span></span>
<span data-ttu-id="21f39-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21f39-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21f39-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f39-140">CommonParameters</span></span>
<span data-ttu-id="21f39-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f39-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f39-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f39-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f39-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21f39-143">INPUTS</span></span>

### <span data-ttu-id="21f39-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="21f39-144">String</span></span>

## <span data-ttu-id="21f39-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21f39-145">OUTPUTS</span></span>

### <span data-ttu-id="21f39-146">Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="21f39-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="21f39-147">Dieses Cmdlet gibt nur dann einen Wert zurück, wenn Sie den *passthru* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="21f39-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="21f39-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="21f39-148">NOTES</span></span>

## <span data-ttu-id="21f39-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21f39-149">RELATED LINKS</span></span>

[<span data-ttu-id="21f39-150">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21f39-150">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="21f39-151">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="21f39-151">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="21f39-152">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="21f39-152">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

