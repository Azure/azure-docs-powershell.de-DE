---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010194"
---
# <span data-ttu-id="6c5c8-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c5c8-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6c5c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5c8-103">Fügt dem angegebenen schlüsseltresor ein vorhandenes Azure Storage-Konto hinzu, dessen Schlüssel vom Schlüssel-Vault-Dienst verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="6c5c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c5c8-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c5c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="6c5c8-106">Richtet ein vorhandenes Azure Storage-Konto mit dem schlüsseltresor für speicherkontoschlüssel ein, die von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="6c5c8-107">Das Speicherkonto muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-107">The Storage Account must already exist.</span></span> <span data-ttu-id="6c5c8-108">Die Speichertasten werden dem Anrufer nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="6c5c8-109">Key Vault wird automatisch neu generiert und wechselt basierend auf dem Erneuerungszeitraum den aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="6c5c8-110">Eine Übersicht über dieses Feature finden Sie unter [Azure Key Vault, verwaltetes Speicherkonto – PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) .</span><span class="sxs-lookup"><span data-stu-id="6c5c8-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="6c5c8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c5c8-111">EXAMPLES</span></span>

### <span data-ttu-id="6c5c8-112">Beispiel 1: Einrichten eines Azure Storage-Kontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6c5c8-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="6c5c8-113">Legt ein Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="6c5c8-114">Der aktive Schlüsselsatz ist "key1".</span><span class="sxs-lookup"><span data-stu-id="6c5c8-114">The active key set is 'key1'.</span></span> <span data-ttu-id="6c5c8-115">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="6c5c8-116">Key Vault generiert den Schlüssel "key2" nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls erneut und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="6c5c8-117">Dieser automatische Regenerierungs Prozess wird zwischen "key1" und "key2" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="6c5c8-118">Beispiel 2: Einrichten eines klassischen Azure-speicherkontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6c5c8-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="6c5c8-119">Legt ein klassisches Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="6c5c8-120">Der aktive Schlüsselsatz ist "Primär".</span><span class="sxs-lookup"><span data-stu-id="6c5c8-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="6c5c8-121">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="6c5c8-122">Key Vault generiert nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls den "sekundären" Schlüssel und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="6c5c8-123">Dieser automatische Regenerierungs Prozess wird zwischen "Primär" und "Sekundär" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="6c5c8-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c5c8-124">PARAMETERS</span></span>

### <span data-ttu-id="6c5c8-125">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="6c5c8-125">-AccountName</span></span>
<span data-ttu-id="6c5c8-126">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="6c5c8-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="6c5c8-127">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="6c5c8-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6c5c8-128">-AccountResourceId</span></span>
<span data-ttu-id="6c5c8-129">Azure-Ressourcen-ID des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="6c5c8-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="6c5c8-130">-ActiveKeyName</span></span>
<span data-ttu-id="6c5c8-131">Der Name des Speicherkonto Schlüssels, der zum Generieren von SAS-Token verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="6c5c8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5c8-132">-DefaultProfile</span></span>
<span data-ttu-id="6c5c8-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c5c8-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c5c8-134">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="6c5c8-134">-Disable</span></span>
<span data-ttu-id="6c5c8-135">Deaktiviert die Verwendung des Schlüssels des verwalteten speicherkontos für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="6c5c8-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6c5c8-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="6c5c8-137">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="6c5c8-137">Auto regenerate key.</span></span> <span data-ttu-id="6c5c8-138">Ist der Wert "true", wird der inaktive Schlüssel des verwalteten speicherkontos automatisch neu generiert und nach dem Erneuerungszeitraum zum neuen aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="6c5c8-139">Ist der Wert false, werden die Schlüssel des verwalteten speicherkontos nicht automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="6c5c8-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="6c5c8-140">-RegenerationPeriod</span></span>
<span data-ttu-id="6c5c8-141">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-141">Regeneration period.</span></span> <span data-ttu-id="6c5c8-142">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum neuen aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="6c5c8-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c5c8-143">-Tag</span></span>
<span data-ttu-id="6c5c8-144">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="6c5c8-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c5c8-145">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6c5c8-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c5c8-146">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6c5c8-146">-VaultName</span></span>
<span data-ttu-id="6c5c8-147">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-147">Vault name.</span></span>
<span data-ttu-id="6c5c8-148">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6c5c8-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c5c8-149">-Confirm</span></span>
<span data-ttu-id="6c5c8-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c5c8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c5c8-151">-WhatIf</span></span>
<span data-ttu-id="6c5c8-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c5c8-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c5c8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5c8-154">CommonParameters</span></span>
<span data-ttu-id="6c5c8-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c5c8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5c8-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c5c8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5c8-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c5c8-157">INPUTS</span></span>

### <span data-ttu-id="6c5c8-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6c5c8-158">System.String</span></span>

### <span data-ttu-id="6c5c8-159">System. Nullable ' 1 [[System. TimeSpan, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6c5c8-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6c5c8-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c5c8-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c5c8-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c5c8-161">OUTPUTS</span></span>

### <span data-ttu-id="6c5c8-162">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6c5c8-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6c5c8-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c5c8-163">NOTES</span></span>

## <span data-ttu-id="6c5c8-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c5c8-164">RELATED LINKS</span></span>

[<span data-ttu-id="6c5c8-165">AZ. keyvault</span><span class="sxs-lookup"><span data-stu-id="6c5c8-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
