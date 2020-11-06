---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482897"
---
# <span data-ttu-id="83d7a-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83d7a-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="83d7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="83d7a-103">Löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="83d7a-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83d7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d7a-104">SYNTAX</span></span>

### <span data-ttu-id="83d7a-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="83d7a-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d7a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83d7a-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d7a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="83d7a-108">Das Remove-AzureKeyVaultKey-Cmdlet löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="83d7a-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="83d7a-109">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzureKeyVaultKeyRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="83d7a-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="83d7a-110">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="83d7a-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="83d7a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83d7a-111">EXAMPLES</span></span>

### <span data-ttu-id="83d7a-112">Beispiel 1: Entfernen eines Schlüssels aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="83d7a-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="83d7a-113">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="83d7a-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="83d7a-114">Beispiel 2: Entfernen eines Schlüssels ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="83d7a-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="83d7a-115">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="83d7a-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="83d7a-116">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="83d7a-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="83d7a-117">Beispiel 3: Dauerhaftes Löschen eines gelöschten Schlüssels aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="83d7a-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="83d7a-118">Mit diesem Befehl wird der Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen "Contoso" endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="83d7a-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="83d7a-119">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="83d7a-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="83d7a-120">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="83d7a-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="83d7a-121">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab und übergibt Sie mithilfe des Pipelineoperators an das **Where-Object-** Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d7a-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83d7a-122">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $false für das **Enabled** -Attribut an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d7a-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="83d7a-123">Dieses Cmdlet entfernt diese Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="83d7a-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="83d7a-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="83d7a-124">PARAMETERS</span></span>

### <span data-ttu-id="83d7a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d7a-125">-DefaultProfile</span></span>
<span data-ttu-id="83d7a-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="83d7a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83d7a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="83d7a-127">-Force</span></span>
<span data-ttu-id="83d7a-128">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="83d7a-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83d7a-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83d7a-129">-InputObject</span></span>
<span data-ttu-id="83d7a-130">Keybundle-Objekt</span><span class="sxs-lookup"><span data-stu-id="83d7a-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d7a-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="83d7a-131">-InRemovedState</span></span>
<span data-ttu-id="83d7a-132">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="83d7a-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="83d7a-133">-Name</span><span class="sxs-lookup"><span data-stu-id="83d7a-133">-Name</span></span>
<span data-ttu-id="83d7a-134">Gibt den Namen des zu entfernenden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="83d7a-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="83d7a-135">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="83d7a-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d7a-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83d7a-136">-PassThru</span></span>
<span data-ttu-id="83d7a-137">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. keybundle** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="83d7a-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="83d7a-138">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="83d7a-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83d7a-139">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="83d7a-139">-VaultName</span></span>
<span data-ttu-id="83d7a-140">Gibt den Namen des Schlüsselspeichers an, aus dem der Schlüssel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="83d7a-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="83d7a-141">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="83d7a-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d7a-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83d7a-142">-Confirm</span></span>
<span data-ttu-id="83d7a-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83d7a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d7a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d7a-144">-WhatIf</span></span>
<span data-ttu-id="83d7a-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83d7a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d7a-146">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83d7a-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d7a-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83d7a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d7a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d7a-148">CommonParameters</span></span>
<span data-ttu-id="83d7a-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d7a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d7a-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d7a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d7a-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83d7a-151">INPUTS</span></span>

### <span data-ttu-id="83d7a-152">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="83d7a-152">String</span></span>

## <span data-ttu-id="83d7a-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83d7a-153">OUTPUTS</span></span>

### <span data-ttu-id="83d7a-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83d7a-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="83d7a-155">Dieses Cmdlet gibt nur dann einen Wert zurück, wenn Sie den *passthru* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="83d7a-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="83d7a-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="83d7a-156">NOTES</span></span>

## <span data-ttu-id="83d7a-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83d7a-157">RELATED LINKS</span></span>

[<span data-ttu-id="83d7a-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83d7a-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="83d7a-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="83d7a-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="83d7a-160">Satz-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="83d7a-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="83d7a-161">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="83d7a-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

