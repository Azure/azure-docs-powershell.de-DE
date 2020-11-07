---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 2c52d6cbd5a3e027baf41959d28816f63062b046
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650863"
---
# <span data-ttu-id="8d6b9-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d6b9-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="8d6b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6b9-103">Löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="8d6b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d6b9-104">SYNTAX</span></span>

### <span data-ttu-id="8d6b9-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d6b9-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d6b9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d6b9-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d6b9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d6b9-107">DESCRIPTION</span></span>
<span data-ttu-id="8d6b9-108">Das Remove-AzKeyVaultSecret-Cmdlet löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="8d6b9-109">Wenn das Geheimnis versehentlich gelöscht wurde, kann das Geheimnis mithilfe von Undo-AzKeyVaultSecretRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8d6b9-110">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8d6b9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d6b9-111">EXAMPLES</span></span>

### <span data-ttu-id="8d6b9-112">Beispiel 1: Entfernen eines Geheimnisses aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="8d6b9-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="8d6b9-113">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso".</span><span class="sxs-lookup"><span data-stu-id="8d6b9-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="8d6b9-114">Beispiel 2: Entfernen eines Geheimnisses aus einem schlüsseltresor ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="8d6b9-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="8d6b9-115">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="8d6b9-116">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8d6b9-117">Beispiel 3: Dauerhaftes Löschen eines gelöschten Geheimnisses aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="8d6b9-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="8d6b9-118">Mit diesem Befehl wird der geheime Name FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso" endgültig verschoben.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8d6b9-119">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="8d6b9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d6b9-120">PARAMETERS</span></span>

### <span data-ttu-id="8d6b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6b9-121">-DefaultProfile</span></span>
<span data-ttu-id="8d6b9-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8d6b9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d6b9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8d6b9-123">-Force</span></span>
<span data-ttu-id="8d6b9-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d6b9-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d6b9-125">-InputObject</span></span>
<span data-ttu-id="8d6b9-126">Schlüsseldepot-Secret-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d6b9-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d6b9-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8d6b9-127">-InRemovedState</span></span>
<span data-ttu-id="8d6b9-128">Wenn vorhanden, wird das zuvor gelöschte Geheimnis endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="8d6b9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8d6b9-129">-Name</span></span>
<span data-ttu-id="8d6b9-130">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="8d6b9-131">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6b9-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d6b9-132">-PassThru</span></span>
<span data-ttu-id="8d6b9-133">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. Secret** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="8d6b9-134">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d6b9-135">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="8d6b9-135">-VaultName</span></span>
<span data-ttu-id="8d6b9-136">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="8d6b9-137">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d6b9-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d6b9-138">-Confirm</span></span>
<span data-ttu-id="8d6b9-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d6b9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d6b9-140">-WhatIf</span></span>
<span data-ttu-id="8d6b9-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d6b9-142">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d6b9-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d6b9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6b9-144">CommonParameters</span></span>
<span data-ttu-id="8d6b9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d6b9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6b9-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6b9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6b9-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d6b9-147">INPUTS</span></span>

### <span data-ttu-id="8d6b9-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8d6b9-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="8d6b9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d6b9-149">OUTPUTS</span></span>

### <span data-ttu-id="8d6b9-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d6b9-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="8d6b9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d6b9-151">NOTES</span></span>

## <span data-ttu-id="8d6b9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d6b9-152">RELATED LINKS</span></span>

[<span data-ttu-id="8d6b9-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d6b9-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="8d6b9-154">Satz-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8d6b9-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="8d6b9-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="8d6b9-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

