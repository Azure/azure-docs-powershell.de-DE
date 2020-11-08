---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmKey.md
ms.openlocfilehash: 15a9466dd0caac6ebe7497942de36e832b89ee55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175495"
---
# <span data-ttu-id="38ba6-101">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-101">Remove-AzManagedHsmKey</span></span>

## <span data-ttu-id="38ba6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="38ba6-103">Löscht einen Schlüssel in einem verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="38ba6-103">Deletes a key in a managed HSM.</span></span>

## <span data-ttu-id="38ba6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38ba6-104">SYNTAX</span></span>

### <span data-ttu-id="38ba6-105">RemoveByKeyNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="38ba6-105">RemoveByKeyNameParameterSet (Default)</span></span>
```
Remove-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38ba6-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38ba6-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ba6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="38ba6-108">Das Remove-AzManagedHsmKey-Cmdlet löscht einen Schlüssel in einem verwalteten HSM.</span><span class="sxs-lookup"><span data-stu-id="38ba6-108">The Remove-AzManagedHsmKey cmdlet deletes a key in a managed HSM.</span></span>
<span data-ttu-id="38ba6-109">Wenn der Schlüssel versehentlich gelöscht wurde, kann der Schlüssel mithilfe von Undo-AzManagedHsmKeyRemoval von einem Benutzer mit speziellen "Recover"-Berechtigungen wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="38ba6-109">If the key was accidentally deleted the key can be recovered using Undo-AzManagedHsmKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="38ba6-110">Dieses Cmdlet hat den Wert "höchst" für die **ConfirmImpact** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="38ba6-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="38ba6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38ba6-111">EXAMPLES</span></span>

### <span data-ttu-id="38ba6-112">Beispiel 1: Entfernen eines Schlüssels aus einem verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="38ba6-112">Example 1: Remove a key from a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -PassThru

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:35:06 AM
Scheduled Purge Date : 1/12/2021 9:35:06 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="38ba6-113">Dieser Befehl entfernt den Schlüssel mit dem Namen TestKey aus dem verwalteten HSM mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="38ba6-113">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="38ba6-114">Beispiel 2: Entfernen eines Schlüssels ohne Bestätigung durch den Benutzer</span><span class="sxs-lookup"><span data-stu-id="38ba6-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -Force
```

<span data-ttu-id="38ba6-115">Dieser Befehl entfernt den Schlüssel mit dem Namen TestKey aus dem verwalteten HSM mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="38ba6-115">This command removes the key named testkey from the managed HSM named testmhsm.</span></span>
<span data-ttu-id="38ba6-116">Der Befehl gibt den Parameter *Force* an, und das Cmdlet fordert Sie daher nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="38ba6-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="38ba6-117">Beispiel 3: Dauerhaftes Löschen eines gelöschten Schlüssels aus dem verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="38ba6-117">Example 3: Purge a deleted key from the managed HSM permanently</span></span>
```powershell
PS C:\> Remove-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState
```

<span data-ttu-id="38ba6-118">Dieser Befehl entfernt den Schlüssel mit dem Namen TestKey aus dem verwalteten HSM mit dem Namen testmhsm dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="38ba6-118">This command removes the key named testkey from the managed HSM named testmhsm permanently.</span></span>
<span data-ttu-id="38ba6-119">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für dieses verwaltete HSM gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="38ba6-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this managed HSM.</span></span>

### <span data-ttu-id="38ba6-120">Beispiel 4: Entfernen von Schlüsseln mithilfe des Pipelineoperators</span><span class="sxs-lookup"><span data-stu-id="38ba6-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzManagedHsmKey
```

<span data-ttu-id="38ba6-121">Dieser Befehl ruft alle Schlüssel im verwalteten HSM mit dem Namen testmhsm ab und übergibt Sie mithilfe des Pipelineoperators an das **Where-Object-** Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ba6-121">This command gets all the keys in the managed HSM named testmhsm and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="38ba6-122">Dieses Cmdlet übergibt die Schlüssel mit dem Wert $false für das **Enabled** -Attribut an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ba6-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="38ba6-123">Dieses Cmdlet entfernt diese Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="38ba6-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="38ba6-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="38ba6-124">PARAMETERS</span></span>

### <span data-ttu-id="38ba6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ba6-125">-DefaultProfile</span></span>
<span data-ttu-id="38ba6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38ba6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ba6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="38ba6-127">-Force</span></span>
<span data-ttu-id="38ba6-128">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="38ba6-128">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38ba6-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="38ba6-129">-HsmName</span></span>
<span data-ttu-id="38ba6-130">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="38ba6-130">HSM name.</span></span> <span data-ttu-id="38ba6-131">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="38ba6-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ba6-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38ba6-132">-InputObject</span></span>
<span data-ttu-id="38ba6-133">Key-Objekt</span><span class="sxs-lookup"><span data-stu-id="38ba6-133">Key Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ba6-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="38ba6-134">-InRemovedState</span></span>
<span data-ttu-id="38ba6-135">Entfernen Sie den zuvor gelöschten Schlüssel dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="38ba6-135">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="38ba6-136">-Name</span><span class="sxs-lookup"><span data-stu-id="38ba6-136">-Name</span></span>
<span data-ttu-id="38ba6-137">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="38ba6-137">Key name.</span></span>
<span data-ttu-id="38ba6-138">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="38ba6-138">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByKeyNameParameterSet
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ba6-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38ba6-139">-PassThru</span></span>
<span data-ttu-id="38ba6-140">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="38ba6-140">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="38ba6-141">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das Schlüsselobjekt zurück, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="38ba6-141">If this switch is specified, the cmdlet returns the key object that was deleted.</span></span>

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

### <span data-ttu-id="38ba6-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="38ba6-142">-Confirm</span></span>
<span data-ttu-id="38ba6-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38ba6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ba6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ba6-144">-WhatIf</span></span>
<span data-ttu-id="38ba6-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38ba6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ba6-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38ba6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ba6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ba6-147">CommonParameters</span></span>
<span data-ttu-id="38ba6-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ba6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ba6-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38ba6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ba6-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38ba6-150">INPUTS</span></span>

### <span data-ttu-id="38ba6-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="38ba6-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="38ba6-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38ba6-152">OUTPUTS</span></span>

### <span data-ttu-id="38ba6-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-153">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="38ba6-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="38ba6-154">NOTES</span></span>

## <span data-ttu-id="38ba6-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38ba6-155">RELATED LINKS</span></span>

[<span data-ttu-id="38ba6-156">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-156">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="38ba6-157">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-157">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="38ba6-158">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-158">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="38ba6-159">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="38ba6-159">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="38ba6-160">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-160">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="38ba6-161">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="38ba6-161">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)