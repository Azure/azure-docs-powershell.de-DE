---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 85a0bc0f552688d036dc76ebbc6d15c608ade433
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843900"
---
# <span data-ttu-id="adbde-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="adbde-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="adbde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="adbde-102">SYNOPSIS</span></span>
<span data-ttu-id="adbde-103">Fügt dem angegebenen schlüsseltresor ein vorhandenes Azure Storage-Konto hinzu, dessen Schlüssel vom Schlüssel-Vault-Dienst verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="adbde-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="adbde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="adbde-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adbde-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adbde-105">DESCRIPTION</span></span>
<span data-ttu-id="adbde-106">Richtet ein vorhandenes Azure Storage-Konto mit dem schlüsseltresor für speicherkontoschlüssel ein, die von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adbde-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="adbde-107">Das Speicherkonto muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="adbde-107">The Storage Account must already exist.</span></span> <span data-ttu-id="adbde-108">Die Speichertasten werden dem Anrufer nie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adbde-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="adbde-109">Key Vault wird automatisch neu generiert und wechselt basierend auf dem Erneuerungszeitraum den aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="adbde-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="adbde-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adbde-110">EXAMPLES</span></span>

### <span data-ttu-id="adbde-111">Beispiel 1: Einrichten eines Azure Storage-Kontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="adbde-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="adbde-112">Legt ein Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adbde-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="adbde-113">Der aktive Schlüsselsatz ist "key1".</span><span class="sxs-lookup"><span data-stu-id="adbde-113">The active key set is 'key1'.</span></span> <span data-ttu-id="adbde-114">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="adbde-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="adbde-115">Key Vault generiert den Schlüssel "key2" nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls erneut und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="adbde-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="adbde-116">Dieser automatische Regenerierungs Prozess wird zwischen "key1" und "key2" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="adbde-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="adbde-117">Beispiel 2: Einrichten eines klassischen Azure-speicherkontos mit Key Vault zum Verwalten der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="adbde-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="adbde-118">Legt ein klassisches Speicherkonto mit Key Vault fest, dessen Schlüssel von Key Vault verwaltet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="adbde-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="adbde-119">Der aktive Schlüsselsatz ist "Primär".</span><span class="sxs-lookup"><span data-stu-id="adbde-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="adbde-120">Dieser Schlüssel wird verwendet, um SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="adbde-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="adbde-121">Key Vault generiert nach dem Regenerations Zeitraum ab dem Zeitpunkt des Befehls den "sekundären" Schlüssel und legt ihn als aktiven Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="adbde-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="adbde-122">Dieser automatische Regenerierungs Prozess wird zwischen "Primär" und "Sekundär" mit einem Abstand von 90 Tagen fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="adbde-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="adbde-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="adbde-123">PARAMETERS</span></span>

### <span data-ttu-id="adbde-124">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="adbde-124">-AccountName</span></span>
<span data-ttu-id="adbde-125">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="adbde-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="adbde-126">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="adbde-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="adbde-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="adbde-127">-AccountResourceId</span></span>
<span data-ttu-id="adbde-128">Azure-Ressourcen-ID des speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="adbde-128">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="adbde-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="adbde-129">-ActiveKeyName</span></span>
<span data-ttu-id="adbde-130">Der Name des Speicherkonto Schlüssels, der zum Generieren von SAS-Token verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="adbde-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="adbde-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adbde-131">-DefaultProfile</span></span>
<span data-ttu-id="adbde-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="adbde-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adbde-133">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="adbde-133">-Disable</span></span>
<span data-ttu-id="adbde-134">Deaktiviert die Verwendung des Schlüssels des verwalteten speicherkontos für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="adbde-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="adbde-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="adbde-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="adbde-136">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="adbde-136">Auto regenerate key.</span></span> <span data-ttu-id="adbde-137">Ist der Wert "true", wird der inaktive Schlüssel des verwalteten speicherkontos automatisch neu generiert und nach dem Erneuerungszeitraum zum neuen aktiven Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="adbde-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="adbde-138">Ist der Wert false, werden die Schlüssel des verwalteten speicherkontos nicht automatisch neu generiert.</span><span class="sxs-lookup"><span data-stu-id="adbde-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="adbde-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="adbde-139">-RegenerationPeriod</span></span>
<span data-ttu-id="adbde-140">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="adbde-140">Regeneration period.</span></span> <span data-ttu-id="adbde-141">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum neuen aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="adbde-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="adbde-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="adbde-142">-Tag</span></span>
<span data-ttu-id="adbde-143">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="adbde-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="adbde-144">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="adbde-144">For example:</span></span>

<span data-ttu-id="adbde-145">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="adbde-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="adbde-146">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="adbde-146">-VaultName</span></span>
<span data-ttu-id="adbde-147">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="adbde-147">Vault name.</span></span>
<span data-ttu-id="adbde-148">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="adbde-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="adbde-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="adbde-149">-Confirm</span></span>
<span data-ttu-id="adbde-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="adbde-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adbde-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adbde-151">-WhatIf</span></span>
<span data-ttu-id="adbde-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="adbde-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adbde-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adbde-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adbde-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adbde-154">CommonParameters</span></span>
<span data-ttu-id="adbde-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adbde-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adbde-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adbde-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adbde-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="adbde-157">INPUTS</span></span>

### <span data-ttu-id="adbde-158">Keine</span><span class="sxs-lookup"><span data-stu-id="adbde-158">None</span></span>
<span data-ttu-id="adbde-159">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="adbde-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adbde-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="adbde-160">OUTPUTS</span></span>

### <span data-ttu-id="adbde-161">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="adbde-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="adbde-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="adbde-162">NOTES</span></span>

## <span data-ttu-id="adbde-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="adbde-163">RELATED LINKS</span></span>

[<span data-ttu-id="adbde-164">AZ. keyvault</span><span class="sxs-lookup"><span data-stu-id="adbde-164">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
