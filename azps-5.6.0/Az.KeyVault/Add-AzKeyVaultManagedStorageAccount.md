---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 05c744050cc377eda01e309fb30122f83b9a8f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946547"
---
# <span data-ttu-id="c8ea8-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8ea8-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c8ea8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ea8-103">Fügt dem angegebenen Schlüsseltresor ein vorhandenes Azure Storage-Konto hinzu, dessen Schlüssel vom Schlüsseltresordienst verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="c8ea8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8ea8-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8ea8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ea8-106">Richtet ein vorhandenes Azure Storage-Konto mit Schlüsseltresor für Speicherkontoschlüssel ein, das vom Schlüsseltresor verwaltet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="c8ea8-107">Das Speicherkonto muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-107">The Storage Account must already exist.</span></span> <span data-ttu-id="c8ea8-108">Die Speicherschlüssel werden für Anrufer nie verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="c8ea8-109">Der Schlüsseltresor wird automatisch neu generiert und wechselt den aktiven Schlüssel basierend auf dem Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="c8ea8-110">Eine Übersicht über dieses Feature finden Sie unter [Verwaltetes Azure Key Vault-Speicherkonto – PowerShell.](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell)</span><span class="sxs-lookup"><span data-stu-id="c8ea8-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="c8ea8-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8ea8-111">EXAMPLES</span></span>

### <span data-ttu-id="c8ea8-112">Beispiel 1: Festlegen eines Azure Storage-Kontos mit Schlüsseltresor zum Verwalten seiner Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c8ea8-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="c8ea8-113">Legt ein Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="c8ea8-114">Der aktive Schlüsselsatz ist "key1".</span><span class="sxs-lookup"><span data-stu-id="c8ea8-114">The active key set is 'key1'.</span></span> <span data-ttu-id="c8ea8-115">Dieser Schlüssel wird zum Generieren von Sastokens verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="c8ea8-116">Der Schlüsseltresor generiert den Schlüssel "key2" nach dem Erneuerungszeitraum ab dem Zeitpunkt dieses Befehls und setzt ihn als aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="c8ea8-117">Dieser prozess der automatischen Erneuerung wird zwischen "key1" und "key2" mit einer Lücke von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="c8ea8-118">Beispiel 2: Festlegen eines klassischen Azure -Speicherkontos mit Schlüsseltresor zum Verwalten seiner Schlüssel</span><span class="sxs-lookup"><span data-stu-id="c8ea8-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="c8ea8-119">Legt ein klassisches Speicherkonto mit Schlüsseltresor für die Schlüssel fest, die vom Schlüsseltresor verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="c8ea8-120">Der aktive Schlüsselsatz ist "Primär".</span><span class="sxs-lookup"><span data-stu-id="c8ea8-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="c8ea8-121">Dieser Schlüssel wird zum Generieren von Sastokens verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="c8ea8-122">Der Schlüsseltresor generiert nach dem Erneuerungszeitraum ab dem Zeitpunkt dieses Befehls den "sekundären" Schlüssel und setzt ihn als aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="c8ea8-123">Dieser prozess der automatischen Erneuerung wird zwischen "Primär" und "Sekundär" mit einer Lücke von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="c8ea8-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c8ea8-124">PARAMETERS</span></span>

### <span data-ttu-id="c8ea8-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-125">-AccountName</span></span>
<span data-ttu-id="c8ea8-126">Name des verwalteten Speicherkontos für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="c8ea8-127">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontonamens aus dem Tresornamen, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="c8ea8-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c8ea8-128">-AccountResourceId</span></span>
<span data-ttu-id="c8ea8-129">Azure-Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="c8ea8-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-130">-ActiveKeyName</span></span>
<span data-ttu-id="c8ea8-131">Name des Speicherkontoschlüssels, der zum Generieren von SAS-Token verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="c8ea8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ea8-132">-DefaultProfile</span></span>
<span data-ttu-id="c8ea8-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c8ea8-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8ea8-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="c8ea8-134">-Disable</span></span>
<span data-ttu-id="c8ea8-135">Deaktiviert die Verwendung des Schlüssels des verwalteten Speicherkontos für die Generierung von Sas-Tokens.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="c8ea8-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c8ea8-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="c8ea8-137">Automatisches Regenerieren des Schlüssels</span><span class="sxs-lookup"><span data-stu-id="c8ea8-137">Auto regenerate key.</span></span> <span data-ttu-id="c8ea8-138">Ist "true", wird der inaktive Schlüssel des verwalteten Speicherkontos automatisch neu generiert und wird nach dem Erneuerungszeitraum zum neuen aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="c8ea8-139">Ist false, werden die Schlüssel des verwalteten Speicherkontos nicht automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="c8ea8-140">-RegenerierenPeriod</span><span class="sxs-lookup"><span data-stu-id="c8ea8-140">-RegenerationPeriod</span></span>
<span data-ttu-id="c8ea8-141">Regenerierungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-141">Regeneration period.</span></span> <span data-ttu-id="c8ea8-142">Wenn der Schlüssel für die automatische Neuerneuerung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive Schlüssel des verwalteten Speicherkontos automatisch neu generiert wird und der neue aktive Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="c8ea8-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8ea8-143">-Tag</span></span>
<span data-ttu-id="c8ea8-144">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8ea8-145">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c8ea8-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8ea8-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c8ea8-146">-VaultName</span></span>
<span data-ttu-id="c8ea8-147">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-147">Vault name.</span></span>
<span data-ttu-id="c8ea8-148">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c8ea8-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8ea8-149">-Confirm</span></span>
<span data-ttu-id="c8ea8-150">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8ea8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8ea8-151">-WhatIf</span></span>
<span data-ttu-id="c8ea8-152">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8ea8-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8ea8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ea8-154">CommonParameters</span></span>
<span data-ttu-id="c8ea8-155">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ea8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ea8-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8ea8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ea8-157">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8ea8-157">INPUTS</span></span>

### <span data-ttu-id="c8ea8-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c8ea8-158">System.String</span></span>

### <span data-ttu-id="c8ea8-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8ea8-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8ea8-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c8ea8-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c8ea8-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8ea8-161">OUTPUTS</span></span>

### <span data-ttu-id="c8ea8-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8ea8-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c8ea8-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c8ea8-163">NOTES</span></span>

## <span data-ttu-id="c8ea8-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c8ea8-164">RELATED LINKS</span></span>

[<span data-ttu-id="c8ea8-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c8ea8-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
