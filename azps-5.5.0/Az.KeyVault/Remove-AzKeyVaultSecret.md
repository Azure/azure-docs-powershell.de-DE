---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 71a0dcebdc889eb8116089eb3c5a5b8379c72b20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175217"
---
# <span data-ttu-id="0cfcd-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0cfcd-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="0cfcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfcd-103">Löscht einen Geheimschlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="0cfcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cfcd-104">SYNTAX</span></span>

### <span data-ttu-id="0cfcd-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cfcd-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cfcd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0cfcd-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cfcd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0cfcd-107">DESCRIPTION</span></span>
<span data-ttu-id="0cfcd-108">Das Remove-AzKeyVaultSecret cmdlet löscht einen geheimen Schlüssel in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="0cfcd-109">Wenn das Geheimnis versehentlich gelöscht wurde, kann es mithilfe von Undo-AzKeyVaultSecretRemoval einem Benutzer mit speziellen "Wiederherstellen"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="0cfcd-110">Dieses Cmdlet hat den Wert "High" für die **"ConfirmImpact"-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="0cfcd-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="0cfcd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0cfcd-111">EXAMPLES</span></span>

### <span data-ttu-id="0cfcd-112">Beispiel 1: Entfernen eines Geheimschlüssels aus einem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="0cfcd-112">Example 1: Remove a secret from a key vault</span></span>
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

<span data-ttu-id="0cfcd-113">Mit diesem Befehl wird der geheime Name "FinanceSecret" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="0cfcd-114">Beispiel 2: Entfernen eines Geheimschlüssels aus einem Schlüsseltresor ohne Benutzerbestätigung</span><span class="sxs-lookup"><span data-stu-id="0cfcd-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
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

<span data-ttu-id="0cfcd-115">Mit diesem Befehl wird der geheime Name "FinanceSecret" aus dem Schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="0cfcd-116">Der Befehl gibt die Parameter *"Erzwingen"* und *"Bestätigen"* an, daher fordert Sie das Cmdlet nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="0cfcd-117">Beispiel 3: Endgültiges Löschen des geheimen Schlüssels aus dem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="0cfcd-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="0cfcd-118">Dieser Befehl erstellt den geheimen Namen "FinanceSecret" aus dem Schlüsseltresor "Contoso" dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="0cfcd-119">Zum Ausführen dieses Cmdlets ist die Berechtigung zum Löschen erforderlich, die zuvor und explizit dem Benutzer für diesen Schlüsseltresor erteilt worden sein muss.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="0cfcd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cfcd-120">PARAMETERS</span></span>

### <span data-ttu-id="0cfcd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfcd-121">-DefaultProfile</span></span>
<span data-ttu-id="0cfcd-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0cfcd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cfcd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0cfcd-123">-Force</span></span>
<span data-ttu-id="0cfcd-124">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0cfcd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cfcd-125">-InputObject</span></span>
<span data-ttu-id="0cfcd-126">Geheimes Schlüsseltresorobjekt</span><span class="sxs-lookup"><span data-stu-id="0cfcd-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="0cfcd-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0cfcd-127">-InRemovedState</span></span>
<span data-ttu-id="0cfcd-128">Wenn dies der Fall ist, wird der zuvor gelöschte geheime Schlüssel dauerhaft entfernt.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="0cfcd-129">-Name</span><span class="sxs-lookup"><span data-stu-id="0cfcd-129">-Name</span></span>
<span data-ttu-id="0cfcd-130">Gibt den Namen eines geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="0cfcd-131">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines geheimen Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="0cfcd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cfcd-132">-PassThru</span></span>
<span data-ttu-id="0cfcd-133">Gibt an, dass dieses Cmdlet ein **Microsoft.Azure.Commands.KeyVault.Models.Secret-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="0cfcd-134">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0cfcd-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0cfcd-135">-VaultName</span></span>
<span data-ttu-id="0cfcd-136">Gibt den Namen des Schlüsseltresor an, zu dem das Geheimnis gehört.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="0cfcd-137">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="0cfcd-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cfcd-138">-Confirm</span></span>
<span data-ttu-id="0cfcd-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cfcd-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0cfcd-140">-WhatIf</span></span>
<span data-ttu-id="0cfcd-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cfcd-142">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cfcd-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cfcd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfcd-144">CommonParameters</span></span>
<span data-ttu-id="0cfcd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cfcd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfcd-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cfcd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfcd-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0cfcd-147">INPUTS</span></span>

### <span data-ttu-id="0cfcd-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0cfcd-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="0cfcd-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0cfcd-149">OUTPUTS</span></span>

### <span data-ttu-id="0cfcd-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0cfcd-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="0cfcd-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0cfcd-151">NOTES</span></span>

## <span data-ttu-id="0cfcd-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0cfcd-152">RELATED LINKS</span></span>

[<span data-ttu-id="0cfcd-153">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0cfcd-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="0cfcd-154">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0cfcd-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="0cfcd-155">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="0cfcd-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

