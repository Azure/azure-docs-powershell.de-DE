---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472374"
---
# <span data-ttu-id="c7311-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7311-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c7311-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7311-102">SYNOPSIS</span></span>
<span data-ttu-id="c7311-103">Fügt dem angegebenen Schlüsseltresor ein vorhandenes Azure -Speicherkonto hinzu, dessen Schlüssel vom Schlüsseltresordienst verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7311-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="c7311-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7311-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7311-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7311-105">DESCRIPTION</span></span>
<span data-ttu-id="c7311-106">Richtet ein vorhandenes Azure -Speicherkonto mit Schlüsseltresor für Speicherkontoschlüssel ein, die vom Schlüsseltresor verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7311-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="c7311-107">Das Speicherkonto muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c7311-107">The Storage Account must already exist.</span></span> <span data-ttu-id="c7311-108">Die Speicherschlüssel werden anrufer niemals verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="c7311-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="c7311-109">Der Schlüsseltresor generiert und wechselt den aktiven Schlüssel automatisch basierend auf dem Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="c7311-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="c7311-110">Eine Übersicht über dieses Feature finden Sie unter ["Verwaltetes Speicherkonto im Azure Key Vault – PowerShell".](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell)</span><span class="sxs-lookup"><span data-stu-id="c7311-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="c7311-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7311-111">EXAMPLES</span></span>

### <span data-ttu-id="c7311-112">Beispiel 1: Einrichten eines Azure -Speicherkontos mit Schlüsseltresor zum Verwalten seiner Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c7311-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="c7311-113">Legt ein Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7311-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="c7311-114">Der aktive Schlüsselsatz ist "key1".</span><span class="sxs-lookup"><span data-stu-id="c7311-114">The active key set is 'key1'.</span></span> <span data-ttu-id="c7311-115">Dieser Schlüssel wird zum Generieren von Sastokens verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7311-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="c7311-116">Der Schlüsseltresor generiert den Schlüssel "key2" nach dem Zeitraum des Diensts ab dem Zeitpunkt dieses Befehls erneut und setzt ihn als aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7311-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="c7311-117">Dieser automatische Vorgang wird zwischen "key1" und "key2" mit einer Lücke von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c7311-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="c7311-118">Beispiel 2: Festlegen eines klassischen Azure -Speicherkontos mit Schlüsseltresor zum Verwalten seiner Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c7311-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="c7311-119">Legt ein klassisches Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7311-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="c7311-120">Der Aktive Schlüsselsatz ist "Primär".</span><span class="sxs-lookup"><span data-stu-id="c7311-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="c7311-121">Dieser Schlüssel wird zum Generieren von Sastokens verwendet.</span><span class="sxs-lookup"><span data-stu-id="c7311-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="c7311-122">Der Schlüsseltresor generiert den sekundären Schlüssel nach dem Zeitraum des Diensts ab dem Zeitpunkt dieses Befehls erneut und setzt ihn als aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7311-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="c7311-123">Dieser automatische Vorgang wird zwischen "Primär" und "Sekundär" mit einer Lücke von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c7311-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="c7311-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7311-124">PARAMETERS</span></span>

### <span data-ttu-id="c7311-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7311-125">-AccountName</span></span>
<span data-ttu-id="c7311-126">Name des verwalteten Speicherkontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c7311-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="c7311-127">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="c7311-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c7311-128">-AccountResourceId</span></span>
<span data-ttu-id="c7311-129">Die Azure-Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c7311-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="c7311-130">-ActiveKeyName</span></span>
<span data-ttu-id="c7311-131">Name des Speicherkontoschlüssels, der zum Generieren von Sastokens verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c7311-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7311-132">-DefaultProfile</span></span>
<span data-ttu-id="c7311-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c7311-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7311-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="c7311-134">-Disable</span></span>
<span data-ttu-id="c7311-135">Deaktiviert die Verwendung des Schlüssels eines verwalteten Speicherkontos für die Generation von Sastokens.</span><span class="sxs-lookup"><span data-stu-id="c7311-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="c7311-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c7311-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="c7311-137">Schlüssel automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="c7311-137">Auto regenerate key.</span></span> <span data-ttu-id="c7311-138">Ist dies der Fall, wird der inaktive Schlüssel des verwalteten Speicherkontos automatisch neu generiert und nach dem Zeitraum zum neuen aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7311-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="c7311-139">Wenn "False", werden die Schlüssel des verwalteten Speicherkontos nicht automatisch erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="c7311-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="c7311-140">-Destimperiod</span><span class="sxs-lookup"><span data-stu-id="c7311-140">-RegenerationPeriod</span></span>
<span data-ttu-id="c7311-141">Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="c7311-141">Regeneration period.</span></span> <span data-ttu-id="c7311-142">Wenn die automatische neu generierte Taste aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der die inaktiven Keygets des verwalteten Speicherkontos automatisch neu generiert und zum neuen aktiven Schlüssel werden.</span><span class="sxs-lookup"><span data-stu-id="c7311-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7311-143">-Tag</span></span>
<span data-ttu-id="c7311-144">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c7311-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7311-145">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c7311-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c7311-146">-VaultName</span></span>
<span data-ttu-id="c7311-147">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="c7311-147">Vault name.</span></span>
<span data-ttu-id="c7311-148">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c7311-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7311-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7311-149">-Confirm</span></span>
<span data-ttu-id="c7311-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7311-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7311-151">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c7311-151">-WhatIf</span></span>
<span data-ttu-id="c7311-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7311-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7311-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7311-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7311-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7311-154">CommonParameters</span></span>
<span data-ttu-id="c7311-155">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7311-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7311-156">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7311-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7311-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7311-157">INPUTS</span></span>

### <span data-ttu-id="c7311-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c7311-158">System.String</span></span>

### <span data-ttu-id="c7311-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c7311-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c7311-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7311-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7311-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7311-161">OUTPUTS</span></span>

### <span data-ttu-id="c7311-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c7311-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c7311-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c7311-163">NOTES</span></span>

## <span data-ttu-id="c7311-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c7311-164">RELATED LINKS</span></span>

[<span data-ttu-id="c7311-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c7311-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
