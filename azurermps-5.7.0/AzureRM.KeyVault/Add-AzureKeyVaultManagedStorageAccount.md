---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481197"
---
# <span data-ttu-id="2fd5b-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fd5b-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2fd5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd5b-103">Fügt dem angegebenen schlüsseltresor ein vorhandenes Azure Storage-Konto hinzu, dessen Schlüssel vom Schlüssel-Vault-Dienst verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fd5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fd5b-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd5b-106">Richtet ein vorhandenes Azure Storage-Konto mit dem schlüsseltresor für speicherkontoschlüssel ein, die von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="2fd5b-107">Das Speicherkonto muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-107">The Storage Account must already exist.</span></span> <span data-ttu-id="2fd5b-108">Die Speichertasten werden dem Anrufer nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="2fd5b-109">Key Vault wird automatisch neu generiert und wechselt basierend auf dem Erneuerungszeitraum den aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="2fd5b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fd5b-110">EXAMPLES</span></span>

### <span data-ttu-id="2fd5b-111">Beispiel 1: Einrichten eines Azure Storage-Kontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2fd5b-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="2fd5b-112">Legt ein Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="2fd5b-113">Der aktive Schlüsselsatz ist "key1".</span><span class="sxs-lookup"><span data-stu-id="2fd5b-113">The active key set is 'key1'.</span></span> <span data-ttu-id="2fd5b-114">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="2fd5b-115">Key Vault generiert den Schlüssel "key2" nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls erneut und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="2fd5b-116">Dieser automatische Regenerierungs Prozess wird zwischen "key1" und "key2" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="2fd5b-117">Beispiel 2: Einrichten eines klassischen Azure-speicherkontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2fd5b-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="2fd5b-118">Legt ein klassisches Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="2fd5b-119">Der aktive Schlüsselsatz ist "Primär".</span><span class="sxs-lookup"><span data-stu-id="2fd5b-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="2fd5b-120">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="2fd5b-121">Key Vault generiert nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls den "sekundären" Schlüssel und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="2fd5b-122">Dieser automatische Regenerierungs Prozess wird zwischen "Primär" und "Sekundär" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="2fd5b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fd5b-123">PARAMETERS</span></span>

### <span data-ttu-id="2fd5b-124">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="2fd5b-124">-AccountName</span></span>
<span data-ttu-id="2fd5b-125">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="2fd5b-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="2fd5b-126">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2fd5b-127">-AccountResourceId</span></span>
<span data-ttu-id="2fd5b-128">Azure-Ressourcen-ID des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="2fd5b-129">-ActiveKeyName</span></span>
<span data-ttu-id="2fd5b-130">Der Name des Speicherkonto Schlüssels, der zum Generieren von SAS-Token verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd5b-131">-DefaultProfile</span></span>
<span data-ttu-id="2fd5b-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2fd5b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fd5b-133">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="2fd5b-133">-Disable</span></span>
<span data-ttu-id="2fd5b-134">Deaktiviert die Verwendung des Schlüssels des verwalteten speicherkontos für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="2fd5b-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2fd5b-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="2fd5b-136">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="2fd5b-136">Auto regenerate key.</span></span> <span data-ttu-id="2fd5b-137">Ist der Wert "true", wird der inaktive Schlüssel des verwalteten speicherkontos automatisch neu generiert und nach dem Erneuerungszeitraum zum neuen aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="2fd5b-138">Ist der Wert false, werden die Schlüssel des verwalteten speicherkontos nicht automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="2fd5b-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="2fd5b-139">-RegenerationPeriod</span></span>
<span data-ttu-id="2fd5b-140">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-140">Regeneration period.</span></span> <span data-ttu-id="2fd5b-141">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum neuen aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="2fd5b-142">-Tag</span></span>
<span data-ttu-id="2fd5b-143">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2fd5b-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2fd5b-144">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2fd5b-144">For example:</span></span>

<span data-ttu-id="2fd5b-145">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2fd5b-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-146">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2fd5b-146">-VaultName</span></span>
<span data-ttu-id="2fd5b-147">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-147">Vault name.</span></span>
<span data-ttu-id="2fd5b-148">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2fd5b-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2fd5b-149">-Confirm</span></span>
<span data-ttu-id="2fd5b-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd5b-151">-WhatIf</span></span>
<span data-ttu-id="2fd5b-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd5b-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fd5b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd5b-154">CommonParameters</span></span>
<span data-ttu-id="2fd5b-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd5b-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd5b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd5b-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fd5b-157">INPUTS</span></span>

### <span data-ttu-id="2fd5b-158">Keine</span><span class="sxs-lookup"><span data-stu-id="2fd5b-158">None</span></span>
<span data-ttu-id="2fd5b-159">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2fd5b-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fd5b-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fd5b-160">OUTPUTS</span></span>

### <span data-ttu-id="2fd5b-161">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fd5b-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="2fd5b-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fd5b-162">NOTES</span></span>

## <span data-ttu-id="2fd5b-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fd5b-163">RELATED LINKS</span></span>

[<span data-ttu-id="2fd5b-164">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="2fd5b-164">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
