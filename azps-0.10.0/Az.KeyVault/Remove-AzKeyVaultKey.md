---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842103"
---
# <span data-ttu-id="51e8a-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51e8a-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="51e8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="51e8a-103">Löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="51e8a-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="51e8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51e8a-104">SYNTAX</span></span>

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="51e8a-106">Das Remove-AzKeyVaultKey-Cmdlet löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="51e8a-106">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="51e8a-107">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzKeyVaultKeyRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="51e8a-107">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="51e8a-108">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51e8a-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="51e8a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="51e8a-110">Beispiel 1: Entfernen eines Schlüssels aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="51e8a-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="51e8a-111">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="51e8a-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="51e8a-112">Beispiel 2: Entfernen eines Schlüssels ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="51e8a-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="51e8a-113">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="51e8a-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="51e8a-114">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="51e8a-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="51e8a-115">Beispiel 3: Dauerhaftes Löschen eines gelöschten Schlüssels aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="51e8a-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="51e8a-116">Mit diesem Befehl wird der Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen "Contoso" endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="51e8a-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="51e8a-117">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="51e8a-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="51e8a-118">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="51e8a-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="51e8a-119">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab und übergibt Sie mithilfe des Pipelineoperators an das **Where-Object-** Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e8a-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51e8a-120">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $false für das **Enabled** -Attribut an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51e8a-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="51e8a-121">Dieses Cmdlet entfernt diese Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="51e8a-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="51e8a-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="51e8a-122">PARAMETERS</span></span>

### <span data-ttu-id="51e8a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e8a-123">-DefaultProfile</span></span>
<span data-ttu-id="51e8a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="51e8a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51e8a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="51e8a-125">-Force</span></span>
<span data-ttu-id="51e8a-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="51e8a-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="51e8a-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="51e8a-127">-InRemovedState</span></span>
<span data-ttu-id="51e8a-128">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="51e8a-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="51e8a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="51e8a-129">-Name</span></span>
<span data-ttu-id="51e8a-130">Gibt den Namen des zu entfernenden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="51e8a-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="51e8a-131">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="51e8a-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e8a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51e8a-132">-PassThru</span></span>
<span data-ttu-id="51e8a-133">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. keybundle** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="51e8a-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="51e8a-134">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="51e8a-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="51e8a-135">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="51e8a-135">-VaultName</span></span>
<span data-ttu-id="51e8a-136">Gibt den Namen des Schlüsselspeichers an, aus dem der Schlüssel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51e8a-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="51e8a-137">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="51e8a-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="51e8a-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51e8a-138">-Confirm</span></span>
<span data-ttu-id="51e8a-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51e8a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e8a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e8a-140">-WhatIf</span></span>
<span data-ttu-id="51e8a-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51e8a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e8a-142">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51e8a-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e8a-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51e8a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e8a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e8a-144">CommonParameters</span></span>
<span data-ttu-id="51e8a-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e8a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e8a-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e8a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e8a-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51e8a-147">INPUTS</span></span>

### <span data-ttu-id="51e8a-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="51e8a-148">String</span></span>

## <span data-ttu-id="51e8a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51e8a-149">OUTPUTS</span></span>

### <span data-ttu-id="51e8a-150">Microsoft. Azure. Commands. keyvault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="51e8a-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="51e8a-151">Dieses Cmdlet gibt nur dann einen Wert zurück, wenn Sie den *passthru* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="51e8a-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="51e8a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="51e8a-152">NOTES</span></span>

## <span data-ttu-id="51e8a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51e8a-153">RELATED LINKS</span></span>

[<span data-ttu-id="51e8a-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51e8a-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="51e8a-155">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="51e8a-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="51e8a-156">Satz-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="51e8a-156">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="51e8a-157">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="51e8a-157">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

