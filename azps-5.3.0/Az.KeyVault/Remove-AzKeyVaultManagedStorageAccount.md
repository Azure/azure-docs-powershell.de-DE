---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472356"
---
# <span data-ttu-id="3af1b-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3af1b-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3af1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3af1b-103">Entfernt ein schlüsseltresor verwaltetes Azure Storage-Konto und alle zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="3af1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3af1b-104">SYNTAX</span></span>

### <span data-ttu-id="3af1b-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3af1b-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3af1b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3af1b-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3af1b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3af1b-107">DESCRIPTION</span></span>
<span data-ttu-id="3af1b-108">Entfernt ein Azure -Speicherkonto vom Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3af1b-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="3af1b-109">Dadurch wird kein Azure -Speicherkonto entfernt, sondern die Kontoschlüssel werden von Azure Key Vault verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="3af1b-110">Alle zugeordneten SAS-Definitionen für den schlüsseltresor verwalteten Speicher werden ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="3af1b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3af1b-111">EXAMPLES</span></span>

### <span data-ttu-id="3af1b-112">Beispiel 1: Entfernen eines schlüsseltresor verwalteten Azure -Speicherkontos und aller zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="3af1b-113">Entfernt die Zuordnung des Azure -Speicherkontos "mystorageaccount" vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="3af1b-114">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="3af1b-115">Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Schlüsselspeicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="3af1b-116">Beispiel 2: Entfernen eines schlüsseltresor verwalteten Azure -Speicherkontos und aller zugeordneten SAS-Definitionen ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="3af1b-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="3af1b-117">Entfernt die Zuordnung des Azure -Speicherkontos "mystorageaccount" vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="3af1b-118">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="3af1b-119">Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Schlüsselspeicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="3af1b-120">Beispiel 3: Endgültiges Löschen eines Schlüsseltresor, das vom Schlüsseltresor verwaltet wurde, und aller zugehörigen SAS-Definitionen aus einem für die weiche Löschung aktivierten Tresor.</span><span class="sxs-lookup"><span data-stu-id="3af1b-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="3af1b-121">Im Beispiel wird davon ausgegangen, dass das weiche Löschen für diesen Tresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3af1b-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="3af1b-122">Überprüfen Sie, ob dies der Fall ist, indem Sie die Tresoreigenschaften oder das "RecoveryLevel"-Attribut einer Entität im Tresor überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="3af1b-123">Das erste Cmdlet entfernt das Azure -Speicherkonto "mystorageaccount" aus dem Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="3af1b-124">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="3af1b-125">Alle diesem Konto zugeordneten SAS-Definitionen für verwalteten Speicher im Schlüsseltresor werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="3af1b-126">Mit dem zweiten Cmdlet wird überprüft, ob sich das Speicherkonto in einem gelöschten, aber beh wiederherstellbaren Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="3af1b-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="3af1b-127">Das Erreichen dieses Status kann einige Zeit erfordern. Lassen Sie bitte ca. 30 s zu, bevor Sie versuchen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="3af1b-128">Das dritte Cmdlet entfernt das Speicherkonto dauerhaft – eine Wiederherstellung ist nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="3af1b-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="3af1b-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3af1b-129">PARAMETERS</span></span>

### <span data-ttu-id="3af1b-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3af1b-130">-AccountName</span></span>
<span data-ttu-id="3af1b-131">Name des verwalteten Speicherkontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3af1b-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="3af1b-132">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af1b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af1b-133">-DefaultProfile</span></span>
<span data-ttu-id="3af1b-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3af1b-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af1b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="3af1b-135">-Force</span></span>
<span data-ttu-id="3af1b-136">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="3af1b-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3af1b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3af1b-137">-InputObject</span></span>
<span data-ttu-id="3af1b-138">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3af1b-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3af1b-139">-InRemovedState</span></span>
<span data-ttu-id="3af1b-140">Endgültiges Entfernen des zuvor gelöschten verwalteten Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="3af1b-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="3af1b-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3af1b-141">-PassThru</span></span>
<span data-ttu-id="3af1b-142">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3af1b-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3af1b-143">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das konto für verwalteten Speicher zurück, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="3af1b-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="3af1b-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3af1b-144">-VaultName</span></span>
<span data-ttu-id="3af1b-145">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="3af1b-145">Vault name.</span></span>
<span data-ttu-id="3af1b-146">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3af1b-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af1b-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3af1b-147">-Confirm</span></span>
<span data-ttu-id="3af1b-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3af1b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af1b-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3af1b-149">-WhatIf</span></span>
<span data-ttu-id="3af1b-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3af1b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af1b-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3af1b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af1b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af1b-152">CommonParameters</span></span>
<span data-ttu-id="3af1b-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af1b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af1b-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3af1b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af1b-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3af1b-155">INPUTS</span></span>

### <span data-ttu-id="3af1b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3af1b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="3af1b-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3af1b-157">OUTPUTS</span></span>

### <span data-ttu-id="3af1b-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3af1b-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3af1b-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3af1b-159">NOTES</span></span>

## <span data-ttu-id="3af1b-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3af1b-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

