---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c415a7b80609a9e8794df183b2ae1cea73a7f1cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180414"
---
# <span data-ttu-id="68cf9-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68cf9-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="68cf9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="68cf9-103">Entfernt ein zentrales Vault Managed Azure-Speicherkonto und alle zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="68cf9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68cf9-104">SYNTAX</span></span>

### <span data-ttu-id="68cf9-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="68cf9-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68cf9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="68cf9-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68cf9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="68cf9-108">Trennt ein Azure Storage-Konto von Key Vault.</span><span class="sxs-lookup"><span data-stu-id="68cf9-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="68cf9-109">Dadurch wird kein Azure-Speicherkonto entfernt, aber die Kontoschlüssel werden vom Azure Key Vault verwaltet.</span><span class="sxs-lookup"><span data-stu-id="68cf9-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="68cf9-110">Alle zugehörigen Schlüsselspeicher-SAS-Definitionen für den Speicher werden ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="68cf9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68cf9-111">EXAMPLES</span></span>

### <span data-ttu-id="68cf9-112">Beispiel 1: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
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

<span data-ttu-id="68cf9-113">Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="68cf9-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="68cf9-114">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="68cf9-115">Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="68cf9-116">Beispiel 2: Entfernen eines zentralen Vault Managed Azure-speicherkontos und aller zugehörigen SAS-Definitionen ohne Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="68cf9-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
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

<span data-ttu-id="68cf9-117">Trennt das Azure-Speicherkonto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="68cf9-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="68cf9-118">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="68cf9-119">Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="68cf9-120">Beispiel 3: Dauerhaftes Löschen (bereinigen) eines von Key Vault verwalteten Azure-speicherkontos und aller zugehörigen SAS-Definitionen aus einem Tresor mit Soft-Delete-Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="68cf9-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="68cf9-121">In diesem Beispiel wird davon ausgegangen, dass Soft-Delete für diesen Tresor aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="68cf9-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="68cf9-122">Überprüfen Sie, ob dies der Fall ist, indem Sie die Vault-Eigenschaften oder das RecoveryLevel-Attribut einer Entität im Tresor untersuchen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="68cf9-123">Das erste Cmdlet trennt das Azure Storage-Konto "mystorageaccount" vom schlüsseltresor "myvault" ab und verhindert, dass die Schlüssel von Key Vault verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="68cf9-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="68cf9-124">Das Konto "mystorageaccount" wird nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="68cf9-125">Alle mit diesem Konto verknüpften Schlüsselspeicher-SAS-Definitionen für verwalteten Speicher werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="68cf9-126">Das zweite Cmdlet überprüft, ob sich das Speicherkonto in einem gelöschten, aber behebbaren Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="68cf9-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="68cf9-127">Wenn Sie diesen Zustand erreichen, benötigen Sie möglicherweise einige Zeit, bevor Sie es versuchen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="68cf9-128">Das dritte Cmdlet entfernt endgültig das Speicherkonto – die Wiederherstellung ist nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="68cf9-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="68cf9-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="68cf9-129">PARAMETERS</span></span>

### <span data-ttu-id="68cf9-130">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="68cf9-130">-AccountName</span></span>
<span data-ttu-id="68cf9-131">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="68cf9-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="68cf9-132">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="68cf9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68cf9-133">-DefaultProfile</span></span>
<span data-ttu-id="68cf9-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68cf9-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68cf9-135">-Force</span><span class="sxs-lookup"><span data-stu-id="68cf9-135">-Force</span></span>
<span data-ttu-id="68cf9-136">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="68cf9-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="68cf9-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68cf9-137">-InputObject</span></span>
<span data-ttu-id="68cf9-138">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="68cf9-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="68cf9-139">-InRemovedState</span></span>
<span data-ttu-id="68cf9-140">Entfernen Sie das zuvor gelöschte verwaltete Speicherkonto endgültig.</span><span class="sxs-lookup"><span data-stu-id="68cf9-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="68cf9-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68cf9-141">-PassThru</span></span>
<span data-ttu-id="68cf9-142">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="68cf9-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="68cf9-143">Wenn dieser Schalter angegeben wird, gibt das Cmdlet das gelöschte verwaltete Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="68cf9-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="68cf9-144">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="68cf9-144">-VaultName</span></span>
<span data-ttu-id="68cf9-145">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="68cf9-145">Vault name.</span></span>
<span data-ttu-id="68cf9-146">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="68cf9-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="68cf9-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68cf9-147">-Confirm</span></span>
<span data-ttu-id="68cf9-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68cf9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68cf9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68cf9-149">-WhatIf</span></span>
<span data-ttu-id="68cf9-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68cf9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68cf9-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68cf9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68cf9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68cf9-152">CommonParameters</span></span>
<span data-ttu-id="68cf9-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68cf9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68cf9-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68cf9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68cf9-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68cf9-155">INPUTS</span></span>

### <span data-ttu-id="68cf9-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="68cf9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="68cf9-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68cf9-157">OUTPUTS</span></span>

### <span data-ttu-id="68cf9-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="68cf9-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="68cf9-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="68cf9-159">NOTES</span></span>

## <span data-ttu-id="68cf9-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68cf9-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

