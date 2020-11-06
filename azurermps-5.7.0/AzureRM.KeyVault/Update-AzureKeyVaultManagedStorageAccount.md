---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: b16ceeb2409c2709286b970f857fcb9079bf067a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481158"
---
# <span data-ttu-id="5b547-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b547-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="5b547-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b547-102">SYNOPSIS</span></span>
<span data-ttu-id="5b547-103">Aktualisieren Sie die bearbeitbaren Attribute eines von Vault verwalteten Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="5b547-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b547-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b547-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b547-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b547-105">DESCRIPTION</span></span>
<span data-ttu-id="5b547-106">Aktualisieren Sie die bearbeitbaren Attribute eines Vault Managed Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="5b547-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="5b547-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b547-107">EXAMPLES</span></span>

### <span data-ttu-id="5b547-108">Beispiel 1: Aktualisieren Sie den aktiven Schlüssel auf "key2" in einem von Key Vault verwalteten Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="5b547-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="5b547-109">Aktualisiert den Schlüssel Vault Managed Azure Storage Account Active Key auf "key2".</span><span class="sxs-lookup"><span data-stu-id="5b547-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="5b547-110">"key2" wird verwendet, um nach diesem Update SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5b547-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="5b547-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b547-111">PARAMETERS</span></span>

### <span data-ttu-id="5b547-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5b547-112">-AccountName</span></span>
<span data-ttu-id="5b547-113">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="5b547-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="5b547-114">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="5b547-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="5b547-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="5b547-115">-ActiveKeyName</span></span>
<span data-ttu-id="5b547-116">Name des aktiven Schlüssels</span><span class="sxs-lookup"><span data-stu-id="5b547-116">Active key name.</span></span>
<span data-ttu-id="5b547-117">Wenn nicht angegeben, bleibt der vorhandene Wert des aktiven Schlüssel namens des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="5b547-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b547-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5b547-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="5b547-119">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="5b547-119">Auto regenerate key.</span></span>
<span data-ttu-id="5b547-120">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Schlüssels für die automatische Regenerierung des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="5b547-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b547-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b547-121">-DefaultProfile</span></span>
<span data-ttu-id="5b547-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b547-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b547-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="5b547-123">-Enable</span></span>
<span data-ttu-id="5b547-124">Sofern vorhanden, wird die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung aktiviert, wenn value wahr ist.</span><span class="sxs-lookup"><span data-stu-id="5b547-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="5b547-125">Deaktiviert die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung, wenn der Wert false ist.</span><span class="sxs-lookup"><span data-stu-id="5b547-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="5b547-126">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Status aktiviert/deaktiviert des speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="5b547-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b547-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b547-127">-PassThru</span></span>
<span data-ttu-id="5b547-128">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="5b547-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="5b547-129">Wenn dieser Schalter angegeben ist, geben Sie das Objekt des verwalteten speicherkontos zurück.</span><span class="sxs-lookup"><span data-stu-id="5b547-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="5b547-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="5b547-130">-RegenerationPeriod</span></span>
<span data-ttu-id="5b547-131">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="5b547-131">Regeneration period.</span></span> <span data-ttu-id="5b547-132">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="5b547-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="5b547-133">Wenn nicht angegeben, bleibt der vorhandene Wert der Regenerierungs Periode von Schlüsseln des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="5b547-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="5b547-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b547-134">-Tag</span></span>
<span data-ttu-id="5b547-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="5b547-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b547-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5b547-136">For example:</span></span>

<span data-ttu-id="5b547-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="5b547-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b547-138">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="5b547-138">-VaultName</span></span>
<span data-ttu-id="5b547-139">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="5b547-139">Vault name.</span></span>
<span data-ttu-id="5b547-140">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5b547-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="5b547-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b547-141">-Confirm</span></span>
<span data-ttu-id="5b547-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b547-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b547-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b547-143">-WhatIf</span></span>
<span data-ttu-id="5b547-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b547-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b547-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b547-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b547-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b547-146">CommonParameters</span></span>
<span data-ttu-id="5b547-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b547-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b547-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b547-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b547-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b547-149">INPUTS</span></span>

### <span data-ttu-id="5b547-150">Keine</span><span class="sxs-lookup"><span data-stu-id="5b547-150">None</span></span>
<span data-ttu-id="5b547-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5b547-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b547-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b547-152">OUTPUTS</span></span>

### <span data-ttu-id="5b547-153">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b547-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="5b547-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b547-154">NOTES</span></span>

## <span data-ttu-id="5b547-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b547-155">RELATED LINKS</span></span>

[<span data-ttu-id="5b547-156">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="5b547-156">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
