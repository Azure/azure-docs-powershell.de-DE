---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918872"
---
# <span data-ttu-id="c2ce8-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2ce8-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c2ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ce8-103">Entfernt ein vom Schlüsseltresor verwaltetes Azure Storage-Konto und alle zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="c2ce8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2ce8-104">SYNTAX</span></span>

### <span data-ttu-id="c2ce8-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2ce8-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2ce8-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ce8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2ce8-107">DESCRIPTION</span></span>
<span data-ttu-id="c2ce8-108">Die Zuordnung eines Azure Storage-Kontos vom Schlüsseltresor wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="c2ce8-109">Dadurch wird kein Azure Storage-Konto entfernt, sondern die Kontoschlüssel werden nicht vom Azure Key Vault verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="c2ce8-110">Alle zugeordneten Key Vault managed Storage SAS-Definitionen werden ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="c2ce8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2ce8-111">EXAMPLES</span></span>

### <span data-ttu-id="c2ce8-112">Beispiel 1: Entfernen eines vom Schlüsseltresor verwalteten Azure Storage-Kontos und aller zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="c2ce8-113">Entfernt das "mystorageaccount" des Azure Storage-Kontos vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="c2ce8-114">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="c2ce8-115">Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="c2ce8-116">Beispiel 2: Entfernen eines verwalteten Azure Storage-Schlüsseltresorkontos und aller zugehörigen SAS-Definitionen ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="c2ce8-117">Entfernt das "mystorageaccount" des Azure Storage-Kontos vom Schlüsseltresor "myvault" und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="c2ce8-118">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="c2ce8-119">Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="c2ce8-120">Beispiel 3: Endgültiges Löschen (Löschen) eines vom Schlüsseltresor verwalteten Azure Storage-Kontos und aller zugehörigen SAS-Definitionen aus einem Mit soft-delete aktivierten Tresor.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="c2ce8-121">Im Beispiel wird davon ausgegangen, dass das soft-delete für diesen Tresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="c2ce8-122">Überprüfen Sie, ob dies der Fall ist, indem Sie die Tresoreigenschaften oder das RecoveryLevel-Attribut einer Entität im Tresor untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="c2ce8-123">Das erste Cmdlet entfernt das "mystorageaccount" des Azure Storage-Kontos von "myvault" des Schlüsseltresors und verhindert, dass der Schlüsseltresor seine Schlüssel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="c2ce8-124">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="c2ce8-125">Alle mit dem Schlüsseltresor verwalteten SAS-Definitionen, die diesem Konto zugeordnet sind, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="c2ce8-126">Das zweite Cmdlet überprüft, ob sich das Speicherkonto in einem gelöschten, aber wiederherstellbaren Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="c2ce8-127">Das Erreichen dieses Zustands kann einige Zeit erfordern, lassen Sie bitte ~30s zu, bevor Sie versuchen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="c2ce8-128">Das dritte Cmdlet entfernt das Speicherkonto dauerhaft – eine Wiederherstellung ist nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="c2ce8-129">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2ce8-129">PARAMETERS</span></span>

### <span data-ttu-id="c2ce8-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2ce8-130">-AccountName</span></span>
<span data-ttu-id="c2ce8-131">Name des verwalteten Speicherkontos für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="c2ce8-132">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="c2ce8-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ce8-133">-DefaultProfile</span></span>
<span data-ttu-id="c2ce8-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c2ce8-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2ce8-135">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="c2ce8-135">-Force</span></span>
<span data-ttu-id="c2ce8-136">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c2ce8-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2ce8-137">-InputObject</span></span>
<span data-ttu-id="c2ce8-138">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="c2ce8-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c2ce8-139">-InRemovedState</span></span>
<span data-ttu-id="c2ce8-140">Entfernen Sie das zuvor gelöschte verwaltete Speicherkonto endgültig.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="c2ce8-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2ce8-141">-PassThru</span></span>
<span data-ttu-id="c2ce8-142">Das Cmdlet gibt standardmäßig kein -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c2ce8-143">Wenn dieser Schalter angegeben ist, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="c2ce8-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c2ce8-144">-VaultName</span></span>
<span data-ttu-id="c2ce8-145">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-145">Vault name.</span></span>
<span data-ttu-id="c2ce8-146">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c2ce8-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2ce8-147">-Confirm</span></span>
<span data-ttu-id="c2ce8-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ce8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ce8-149">-WhatIf</span></span>
<span data-ttu-id="c2ce8-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ce8-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ce8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ce8-152">CommonParameters</span></span>
<span data-ttu-id="c2ce8-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ce8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ce8-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2ce8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ce8-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2ce8-155">INPUTS</span></span>

### <span data-ttu-id="c2ce8-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c2ce8-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="c2ce8-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2ce8-157">OUTPUTS</span></span>

### <span data-ttu-id="c2ce8-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c2ce8-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c2ce8-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2ce8-159">NOTES</span></span>

## <span data-ttu-id="c2ce8-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2ce8-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

