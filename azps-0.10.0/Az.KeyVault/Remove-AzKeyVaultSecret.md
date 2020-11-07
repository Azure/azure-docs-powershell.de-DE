---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842092"
---
# <span data-ttu-id="50d1e-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="50d1e-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="50d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="50d1e-103">Löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="50d1e-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="50d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50d1e-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50d1e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="50d1e-106">Das Remove-AzKeyVaultSecret-Cmdlet löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="50d1e-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="50d1e-107">Wenn das Geheimnis versehentlich gelöscht wurde, kann das Geheimnis mithilfe von Undo-AzKeyVaultSecretRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="50d1e-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="50d1e-108">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="50d1e-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="50d1e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50d1e-109">EXAMPLES</span></span>

### <span data-ttu-id="50d1e-110">Beispiel 1: Entfernen eines Geheimnisses aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="50d1e-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="50d1e-111">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso".</span><span class="sxs-lookup"><span data-stu-id="50d1e-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="50d1e-112">Beispiel 2: Entfernen eines Geheimnisses aus einem schlüsseltresor ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="50d1e-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="50d1e-113">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="50d1e-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="50d1e-114">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="50d1e-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="50d1e-115">Beispiel 3: Dauerhaftes Löschen eines gelöschten Geheimnisses aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="50d1e-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="50d1e-116">Mit diesem Befehl wird der geheime Name FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso" endgültig verschoben.</span><span class="sxs-lookup"><span data-stu-id="50d1e-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="50d1e-117">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="50d1e-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="50d1e-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="50d1e-118">PARAMETERS</span></span>

### <span data-ttu-id="50d1e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d1e-119">-DefaultProfile</span></span>
<span data-ttu-id="50d1e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="50d1e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50d1e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="50d1e-121">-Force</span></span>
<span data-ttu-id="50d1e-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="50d1e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50d1e-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="50d1e-123">-InRemovedState</span></span>
<span data-ttu-id="50d1e-124">Wenn vorhanden, wird das zuvor gelöschte Geheimnis endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="50d1e-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="50d1e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="50d1e-125">-Name</span></span>
<span data-ttu-id="50d1e-126">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="50d1e-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="50d1e-127">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="50d1e-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="50d1e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50d1e-128">-PassThru</span></span>
<span data-ttu-id="50d1e-129">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. Secret** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="50d1e-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="50d1e-130">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="50d1e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="50d1e-131">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="50d1e-131">-VaultName</span></span>
<span data-ttu-id="50d1e-132">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="50d1e-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="50d1e-133">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="50d1e-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="50d1e-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50d1e-134">-Confirm</span></span>
<span data-ttu-id="50d1e-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50d1e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d1e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50d1e-136">-WhatIf</span></span>
<span data-ttu-id="50d1e-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50d1e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d1e-138">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50d1e-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50d1e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50d1e-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d1e-140">CommonParameters</span></span>
<span data-ttu-id="50d1e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d1e-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d1e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d1e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50d1e-143">INPUTS</span></span>

### <span data-ttu-id="50d1e-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="50d1e-144">String</span></span>

## <span data-ttu-id="50d1e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50d1e-145">OUTPUTS</span></span>

### <span data-ttu-id="50d1e-146">Microsoft. Azure. Commands. keyvault. Models. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="50d1e-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="50d1e-147">Dieses Cmdlet gibt nur dann einen Wert zurück, wenn Sie den *passthru* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="50d1e-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="50d1e-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="50d1e-148">NOTES</span></span>

## <span data-ttu-id="50d1e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50d1e-149">RELATED LINKS</span></span>

[<span data-ttu-id="50d1e-150">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="50d1e-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="50d1e-151">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="50d1e-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="50d1e-152">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="50d1e-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

