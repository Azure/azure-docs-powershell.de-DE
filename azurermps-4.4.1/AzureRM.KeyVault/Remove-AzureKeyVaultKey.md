---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://go.microsoft.com/fwlink/?LinkId=690299
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: b5f2917da71e8c4539660dbb91dd81f3fb5d7959
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502714"
---
# <span data-ttu-id="8b389-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b389-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="8b389-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b389-102">SYNOPSIS</span></span>
<span data-ttu-id="8b389-103">Löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="8b389-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b389-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b389-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b389-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b389-105">DESCRIPTION</span></span>
<span data-ttu-id="8b389-106">Das Remove-AzureKeyVaultKey-Cmdlet löscht einen Schlüssel in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="8b389-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="8b389-107">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzureKeyVaultKeyRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8b389-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8b389-108">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8b389-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8b389-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b389-109">EXAMPLES</span></span>

### <span data-ttu-id="8b389-110">Beispiel 1: Entfernen eines Schlüssels aus einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="8b389-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="8b389-111">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="8b389-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="8b389-112">Beispiel 2: Entfernen eines Schlüssels ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="8b389-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="8b389-113">Dieser Befehl entfernt den Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="8b389-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="8b389-114">Der Befehl gibt die Parameter *Force* und *Confirm* an, und daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8b389-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8b389-115">Beispiel 3: Dauerhaftes Löschen eines gelöschten Schlüssels aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="8b389-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="8b389-116">Mit diesem Befehl wird der Schlüssel mit dem Namen ITSoftware aus dem schlüsseltresor mit dem Namen "Contoso" endgültig entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b389-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8b389-117">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b389-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="8b389-118">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="8b389-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="8b389-119">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab und übergibt Sie mithilfe des Pipelineoperators an das **Where-Object-** Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b389-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b389-120">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $false für das **Enabled** -Attribut an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b389-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="8b389-121">Dieses Cmdlet entfernt diese Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8b389-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="8b389-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b389-122">PARAMETERS</span></span>

### <span data-ttu-id="8b389-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8b389-123">-Force</span></span>
<span data-ttu-id="8b389-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8b389-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b389-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8b389-125">-InRemovedState</span></span>
<span data-ttu-id="8b389-126">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="8b389-126">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="8b389-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8b389-127">-Name</span></span>
<span data-ttu-id="8b389-128">Gibt den Namen des zu entfernenden Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="8b389-128">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="8b389-129">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8b389-129">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b389-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b389-130">-PassThru</span></span>
<span data-ttu-id="8b389-131">Gibt an, dass dieses Cmdlet ein **Microsoft. Azure. Commands. keyvault. Models. keybundle** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8b389-131">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="8b389-132">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8b389-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b389-133">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="8b389-133">-VaultName</span></span>
<span data-ttu-id="8b389-134">Gibt den Namen des Schlüsselspeichers an, aus dem der Schlüssel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b389-134">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="8b389-135">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8b389-135">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="8b389-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b389-136">-Confirm</span></span>
<span data-ttu-id="8b389-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b389-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b389-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b389-138">-WhatIf</span></span>
<span data-ttu-id="8b389-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b389-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b389-140">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b389-140">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b389-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b389-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b389-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b389-142">-DefaultProfile</span></span>
<span data-ttu-id="8b389-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b389-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b389-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b389-144">CommonParameters</span></span>
<span data-ttu-id="8b389-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b389-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b389-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b389-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b389-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b389-147">INPUTS</span></span>

### <span data-ttu-id="8b389-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8b389-148">String</span></span>

## <span data-ttu-id="8b389-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b389-149">OUTPUTS</span></span>

### <span data-ttu-id="8b389-150">Microsoft. Azure. Commands. keyvault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="8b389-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="8b389-151">Dieses Cmdlet gibt nur dann einen Wert zurück, wenn Sie den *passthru* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="8b389-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="8b389-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b389-152">NOTES</span></span>

## <span data-ttu-id="8b389-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b389-153">RELATED LINKS</span></span>

[<span data-ttu-id="8b389-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b389-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="8b389-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8b389-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="8b389-156">Satz-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="8b389-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="8b389-157">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8b389-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

