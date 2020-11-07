---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/update-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ea3d16ec55186017852df30f6ff745f79703f224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843836"
---
# <span data-ttu-id="20284-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20284-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="20284-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20284-102">SYNOPSIS</span></span>
<span data-ttu-id="20284-103">Aktualisieren Sie die bearbeitbaren Attribute eines von Vault verwalteten Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="20284-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="20284-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20284-104">SYNTAX</span></span>

```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20284-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20284-105">DESCRIPTION</span></span>
<span data-ttu-id="20284-106">Aktualisieren Sie die bearbeitbaren Attribute eines Vault Managed Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="20284-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="20284-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20284-107">EXAMPLES</span></span>

### <span data-ttu-id="20284-108">Beispiel 1: Aktualisieren Sie den aktiven Schlüssel auf "key2" in einem von Key Vault verwalteten Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="20284-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="20284-109">Aktualisiert den Schlüssel Vault Managed Azure Storage Account Active Key auf "key2".</span><span class="sxs-lookup"><span data-stu-id="20284-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="20284-110">"key2" wird verwendet, um nach diesem Update SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="20284-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="20284-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="20284-111">PARAMETERS</span></span>

### <span data-ttu-id="20284-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="20284-112">-AccountName</span></span>
<span data-ttu-id="20284-113">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="20284-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="20284-114">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="20284-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="20284-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="20284-115">-ActiveKeyName</span></span>
<span data-ttu-id="20284-116">Name des aktiven Schlüssels</span><span class="sxs-lookup"><span data-stu-id="20284-116">Active key name.</span></span>
<span data-ttu-id="20284-117">Wenn nicht angegeben, bleibt der vorhandene Wert des aktiven Schlüssel namens des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="20284-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="20284-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="20284-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="20284-119">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="20284-119">Auto regenerate key.</span></span>
<span data-ttu-id="20284-120">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Schlüssels für die automatische Regenerierung des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="20284-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="20284-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20284-121">-DefaultProfile</span></span>
<span data-ttu-id="20284-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="20284-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20284-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="20284-123">-Enable</span></span>
<span data-ttu-id="20284-124">Sofern vorhanden, wird die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung aktiviert, wenn value wahr ist.</span><span class="sxs-lookup"><span data-stu-id="20284-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="20284-125">Deaktiviert die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung, wenn der Wert false ist.</span><span class="sxs-lookup"><span data-stu-id="20284-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="20284-126">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Status aktiviert/deaktiviert des speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="20284-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="20284-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20284-127">-PassThru</span></span>
<span data-ttu-id="20284-128">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="20284-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="20284-129">Wenn dieser Schalter angegeben ist, geben Sie das Objekt des verwalteten speicherkontos zurück.</span><span class="sxs-lookup"><span data-stu-id="20284-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="20284-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="20284-130">-RegenerationPeriod</span></span>
<span data-ttu-id="20284-131">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="20284-131">Regeneration period.</span></span> <span data-ttu-id="20284-132">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="20284-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="20284-133">Wenn nicht angegeben, bleibt der vorhandene Wert der Regenerierungs Periode von Schlüsseln des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="20284-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="20284-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="20284-134">-Tag</span></span>
<span data-ttu-id="20284-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="20284-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20284-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="20284-136">For example:</span></span>

<span data-ttu-id="20284-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="20284-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20284-138">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="20284-138">-VaultName</span></span>
<span data-ttu-id="20284-139">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="20284-139">Vault name.</span></span>
<span data-ttu-id="20284-140">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="20284-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="20284-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20284-141">-Confirm</span></span>
<span data-ttu-id="20284-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20284-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20284-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20284-143">-WhatIf</span></span>
<span data-ttu-id="20284-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20284-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20284-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20284-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20284-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20284-146">CommonParameters</span></span>
<span data-ttu-id="20284-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20284-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20284-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20284-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20284-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20284-149">INPUTS</span></span>

### <span data-ttu-id="20284-150">Keine</span><span class="sxs-lookup"><span data-stu-id="20284-150">None</span></span>
<span data-ttu-id="20284-151">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="20284-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20284-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20284-152">OUTPUTS</span></span>

### <span data-ttu-id="20284-153">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20284-153">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="20284-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="20284-154">NOTES</span></span>

## <span data-ttu-id="20284-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20284-155">RELATED LINKS</span></span>

[<span data-ttu-id="20284-156">AZ. keyvault</span><span class="sxs-lookup"><span data-stu-id="20284-156">Az.KeyVault</span></span>](/powershell/module/Az.keyvault)
