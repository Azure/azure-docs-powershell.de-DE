---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 84c6df195b0d24e5096748a4a5e3fd8360665831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479178"
---
# <span data-ttu-id="c6d9d-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6d9d-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c6d9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d9d-103">Aktualisieren Sie die bearbeitbaren Attribute eines von Vault verwalteten Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6d9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6d9d-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6d9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d9d-106">Aktualisieren Sie die bearbeitbaren Attribute eines Vault Managed Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="c6d9d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d9d-108">Beispiel 1: Aktualisieren Sie den aktiven Schlüssel auf "key2" in einem von Key Vault verwalteten Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="c6d9d-109">Aktualisiert den Schlüssel Vault Managed Azure Storage Account Active Key auf "key2".</span><span class="sxs-lookup"><span data-stu-id="c6d9d-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="c6d9d-110">"key2" wird verwendet, um nach diesem Update SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="c6d9d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6d9d-111">PARAMETERS</span></span>

### <span data-ttu-id="c6d9d-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c6d9d-112">-AccountName</span></span>
<span data-ttu-id="c6d9d-113">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="c6d9d-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="c6d9d-114">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="c6d9d-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="c6d9d-115">-ActiveKeyName</span></span>
<span data-ttu-id="c6d9d-116">Name des aktiven Schlüssels</span><span class="sxs-lookup"><span data-stu-id="c6d9d-116">Active key name.</span></span>
<span data-ttu-id="c6d9d-117">Wenn nicht angegeben, bleibt der vorhandene Wert des aktiven Schlüssel namens des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d9d-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c6d9d-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="c6d9d-119">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="c6d9d-119">Auto regenerate key.</span></span>
<span data-ttu-id="c6d9d-120">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Schlüssels für die automatische Regenerierung des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d9d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6d9d-121">-Confirm</span></span>
<span data-ttu-id="c6d9d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6d9d-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="c6d9d-123">-Enable</span></span>
<span data-ttu-id="c6d9d-124">Sofern vorhanden, wird die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung aktiviert, wenn value wahr ist.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="c6d9d-125">Deaktiviert die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung, wenn der Wert false ist.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="c6d9d-126">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Status aktiviert/deaktiviert des speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d9d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6d9d-127">-PassThru</span></span>
<span data-ttu-id="c6d9d-128">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="c6d9d-129">Wenn dieser Schalter angegeben ist, geben Sie das Objekt des verwalteten speicherkontos zurück.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="c6d9d-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="c6d9d-130">-RegenerationPeriod</span></span>
<span data-ttu-id="c6d9d-131">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-131">Regeneration period.</span></span> <span data-ttu-id="c6d9d-132">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="c6d9d-133">Wenn nicht angegeben, bleibt der vorhandene Wert der Regenerierungs Periode von Schlüsseln des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="c6d9d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6d9d-134">-Tag</span></span>
<span data-ttu-id="c6d9d-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="c6d9d-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c6d9d-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c6d9d-136">For example:</span></span>

<span data-ttu-id="c6d9d-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="c6d9d-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c6d9d-138">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c6d9d-138">-VaultName</span></span>
<span data-ttu-id="c6d9d-139">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-139">Vault name.</span></span>
<span data-ttu-id="c6d9d-140">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c6d9d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6d9d-141">-WhatIf</span></span>
<span data-ttu-id="c6d9d-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6d9d-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6d9d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d9d-144">-DefaultProfile</span></span>
<span data-ttu-id="c6d9d-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d9d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d9d-146">CommonParameters</span></span>
<span data-ttu-id="c6d9d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6d9d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d9d-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d9d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d9d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6d9d-149">INPUTS</span></span>

## <span data-ttu-id="c6d9d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6d9d-150">OUTPUTS</span></span>

### <span data-ttu-id="c6d9d-151">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c6d9d-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="c6d9d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6d9d-152">NOTES</span></span>

## <span data-ttu-id="c6d9d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6d9d-153">RELATED LINKS</span></span>

[<span data-ttu-id="c6d9d-154">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="c6d9d-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
