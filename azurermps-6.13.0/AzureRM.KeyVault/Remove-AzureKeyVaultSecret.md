---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496058"
---
# <span data-ttu-id="f53ea-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f53ea-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="f53ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f53ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f53ea-103">Löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f53ea-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f53ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f53ea-104">SYNTAX</span></span>

### <span data-ttu-id="f53ea-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f53ea-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f53ea-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f53ea-107">DESCRIPTION</span></span>
<span data-ttu-id="f53ea-108">Das Remove-AzureKeyVaultSecret-Cmdlet löscht einen geheimen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="f53ea-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="f53ea-109">Wenn das Geheimnis versehentlich gelöscht wurde, kann das Geheimnis mithilfe von Undo-AzureKeyVaultSecretRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f53ea-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="f53ea-110">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f53ea-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="f53ea-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f53ea-111">EXAMPLES</span></span>

### <span data-ttu-id="f53ea-112">Beispiel 1: Entfernen eines Geheimnisses aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="f53ea-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="f53ea-113">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso".</span><span class="sxs-lookup"><span data-stu-id="f53ea-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="f53ea-114">Beispiel 2: Entfernen eines Geheimnisses aus einem schlüsseltresor ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="f53ea-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="f53ea-115">Dieser Befehl entfernt den geheimen Namen FinanceSecret aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="f53ea-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="f53ea-116">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f53ea-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f53ea-117">Beispiel 3: Dauerhaftes Löschen eines gelöschten Geheimnisses aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="f53ea-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="f53ea-118">Mit diesem Befehl wird der geheime Name FinanceSecret aus dem schlüsseltresor mit dem Namen "Contoso" endgültig verschoben.</span><span class="sxs-lookup"><span data-stu-id="f53ea-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="f53ea-119">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f53ea-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="f53ea-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f53ea-120">PARAMETERS</span></span>

### <span data-ttu-id="f53ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53ea-121">-DefaultProfile</span></span>
<span data-ttu-id="f53ea-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f53ea-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f53ea-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f53ea-123">-Force</span></span>
<span data-ttu-id="f53ea-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f53ea-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f53ea-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f53ea-125">-InputObject</span></span>
<span data-ttu-id="f53ea-126">Schlüsseldepot-Secret-Objekt</span><span class="sxs-lookup"><span data-stu-id="f53ea-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="f53ea-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f53ea-127">-InRemovedState</span></span>
<span data-ttu-id="f53ea-128">Wenn vorhanden, wird das zuvor gelöschte Geheimnis endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="f53ea-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="f53ea-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f53ea-129">-Name</span></span>
<span data-ttu-id="f53ea-130">Gibt den Namen eines Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="f53ea-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="f53ea-131">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f53ea-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="f53ea-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f53ea-132">-PassThru</span></span>
<span data-ttu-id="f53ea-133">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. Secret** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f53ea-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="f53ea-134">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f53ea-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f53ea-135">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="f53ea-135">-VaultName</span></span>
<span data-ttu-id="f53ea-136">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="f53ea-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="f53ea-137">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="f53ea-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="f53ea-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f53ea-138">-Confirm</span></span>
<span data-ttu-id="f53ea-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f53ea-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53ea-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53ea-140">-WhatIf</span></span>
<span data-ttu-id="f53ea-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f53ea-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53ea-142">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f53ea-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53ea-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f53ea-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53ea-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53ea-144">CommonParameters</span></span>
<span data-ttu-id="f53ea-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53ea-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53ea-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53ea-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53ea-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f53ea-147">INPUTS</span></span>

### <span data-ttu-id="f53ea-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f53ea-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="f53ea-149">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f53ea-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f53ea-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f53ea-150">OUTPUTS</span></span>

### <span data-ttu-id="f53ea-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f53ea-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="f53ea-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="f53ea-152">NOTES</span></span>

## <span data-ttu-id="f53ea-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f53ea-153">RELATED LINKS</span></span>

[<span data-ttu-id="f53ea-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f53ea-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="f53ea-155">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f53ea-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="f53ea-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f53ea-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

