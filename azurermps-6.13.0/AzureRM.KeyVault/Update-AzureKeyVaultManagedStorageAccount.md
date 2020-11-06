---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1a21db1918d9baef48d3efd15dc72c2cb542a925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496025"
---
# <span data-ttu-id="08de6-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08de6-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="08de6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08de6-102">SYNOPSIS</span></span>
<span data-ttu-id="08de6-103">Aktualisieren Sie die bearbeitbaren Attribute eines von Vault verwalteten Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="08de6-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08de6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08de6-104">SYNTAX</span></span>

### <span data-ttu-id="08de6-105">ByDefinitionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08de6-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08de6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="08de6-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08de6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08de6-107">DESCRIPTION</span></span>
<span data-ttu-id="08de6-108">Aktualisieren Sie die bearbeitbaren Attribute eines Vault Managed Azure-speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="08de6-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="08de6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08de6-109">EXAMPLES</span></span>

### <span data-ttu-id="08de6-110">Beispiel 1: Aktualisieren Sie den aktiven Schlüssel auf "key2" in einem von Key Vault verwalteten Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="08de6-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="08de6-111">Aktualisiert den Schlüssel Vault Managed Azure Storage Account Active Key auf "key2".</span><span class="sxs-lookup"><span data-stu-id="08de6-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="08de6-112">"key2" wird verwendet, um nach diesem Update SAS-Token zu generieren.</span><span class="sxs-lookup"><span data-stu-id="08de6-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="08de6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="08de6-113">PARAMETERS</span></span>

### <span data-ttu-id="08de6-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="08de6-114">-AccountName</span></span>
<span data-ttu-id="08de6-115">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="08de6-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="08de6-116">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="08de6-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="08de6-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="08de6-117">-ActiveKeyName</span></span>
<span data-ttu-id="08de6-118">Name des aktiven Schlüssels</span><span class="sxs-lookup"><span data-stu-id="08de6-118">Active key name.</span></span>
<span data-ttu-id="08de6-119">Wenn nicht angegeben, bleibt der vorhandene Wert des aktiven Schlüssel namens des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="08de6-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08de6-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="08de6-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="08de6-121">Schlüssel zur automatischen Neugenerierung</span><span class="sxs-lookup"><span data-stu-id="08de6-121">Auto regenerate key.</span></span>
<span data-ttu-id="08de6-122">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Schlüssels für die automatische Regenerierung des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="08de6-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="08de6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08de6-123">-DefaultProfile</span></span>
<span data-ttu-id="08de6-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="08de6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08de6-125">-Enable</span><span class="sxs-lookup"><span data-stu-id="08de6-125">-Enable</span></span>
<span data-ttu-id="08de6-126">Sofern vorhanden, wird die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung aktiviert, wenn value wahr ist.</span><span class="sxs-lookup"><span data-stu-id="08de6-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="08de6-127">Deaktiviert die Verwendung eines verwalteten Speicherkonto Schlüssels für die SAS-Token-Generierung, wenn der Wert false ist.</span><span class="sxs-lookup"><span data-stu-id="08de6-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="08de6-128">Wenn diese Option nicht angegeben ist, bleibt der vorhandene Wert des Status aktiviert/deaktiviert des speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="08de6-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="08de6-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08de6-129">-InputObject</span></span>
<span data-ttu-id="08de6-130">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08de6-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="08de6-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08de6-131">-PassThru</span></span>
<span data-ttu-id="08de6-132">Das Cmdlet gibt das Objekt nicht standardmäßig zurück.</span><span class="sxs-lookup"><span data-stu-id="08de6-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="08de6-133">Wenn dieser Schalter angegeben ist, geben Sie das Objekt des verwalteten speicherkontos zurück.</span><span class="sxs-lookup"><span data-stu-id="08de6-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="08de6-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="08de6-134">-RegenerationPeriod</span></span>
<span data-ttu-id="08de6-135">Erneuerungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="08de6-135">Regeneration period.</span></span> <span data-ttu-id="08de6-136">Wenn der Schlüssel für die automatische Regenerierung aktiviert ist, gibt dieser Wert die Zeitspanne an, nach der der inaktive keydes verwalteten speicherkontos automatisch neu generiert wird und zum aktiven Schlüssel wird.</span><span class="sxs-lookup"><span data-stu-id="08de6-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="08de6-137">Wenn nicht angegeben, bleibt der vorhandene Wert der Regenerierungs Periode von Schlüsseln des verwalteten speicherkontos unverändert.</span><span class="sxs-lookup"><span data-stu-id="08de6-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08de6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="08de6-138">-Tag</span></span>
<span data-ttu-id="08de6-139">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="08de6-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08de6-140">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="08de6-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08de6-141">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="08de6-141">-VaultName</span></span>
<span data-ttu-id="08de6-142">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="08de6-142">Vault name.</span></span>
<span data-ttu-id="08de6-143">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="08de6-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="08de6-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08de6-144">-Confirm</span></span>
<span data-ttu-id="08de6-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08de6-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08de6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08de6-146">-WhatIf</span></span>
<span data-ttu-id="08de6-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08de6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08de6-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08de6-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08de6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08de6-149">CommonParameters</span></span>
<span data-ttu-id="08de6-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08de6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08de6-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08de6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08de6-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08de6-152">INPUTS</span></span>

### <span data-ttu-id="08de6-153">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="08de6-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="08de6-154">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="08de6-154">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="08de6-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08de6-155">OUTPUTS</span></span>

### <span data-ttu-id="08de6-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08de6-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="08de6-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="08de6-157">NOTES</span></span>

## <span data-ttu-id="08de6-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08de6-158">RELATED LINKS</span></span>

[<span data-ttu-id="08de6-159">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="08de6-159">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
