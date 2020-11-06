---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: a71aed4703158c68d3b156ff1e37d438e5413782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482413"
---
# <span data-ttu-id="29197-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="29197-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="29197-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29197-102">SYNOPSIS</span></span>
<span data-ttu-id="29197-103">Legt eine freigegebene zugriffssignatur Definition (SAS) mit Schlüsselspeicher für ein gegebenes, zentrales Vault Managed Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="29197-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29197-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29197-104">SYNTAX</span></span>

### <span data-ttu-id="29197-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="29197-105">Default (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29197-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29197-106">ByInputObject</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29197-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29197-107">DESCRIPTION</span></span>
<span data-ttu-id="29197-108">Legt eine SAS-Definition (Shared Access Signature) mit einem angegebenen, von Vault verwalteten Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="29197-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="29197-109">Dadurch wird auch ein geheim Wert festgelegt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="29197-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="29197-110">SAS-Token wird mit diesen Parametern und dem aktiven Schlüssel des verwalteten Azure-speicherkontos für Schlüssel Vault generiert.</span><span class="sxs-lookup"><span data-stu-id="29197-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="29197-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29197-111">EXAMPLES</span></span>

### <span data-ttu-id="29197-112">Beispiel 1: Festlegen einer Kontotyp-SAS-Definition und Abrufen eines aktuellen SAS-Tokens basierend auf diesem</span><span class="sxs-lookup"><span data-stu-id="29197-112">Example 1 : Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzureRmStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzureRmKeyVault -VaultName mykv
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod 180
PS C:\> $sctx = New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzureStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzureKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="29197-113">Legt eine Konto-SAS-Definition "Accounts" auf einem keyvault-verwalteten Speicherkonto "MYSA" in Vault "mykv" fest.</span><span class="sxs-lookup"><span data-stu-id="29197-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="29197-114">Insbesondere führt die obige Abfolge die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="29197-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="29197-115">Ruft ein (bereits vorhandenes) Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="29197-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="29197-116">Ruft einen (bereits vorhandenen) schlüsseltresor ab</span><span class="sxs-lookup"><span data-stu-id="29197-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="29197-117">Fügt dem Tresor ein von keyvault verwaltetes Speicherkonto hinzu, wobei key1 als aktiver Schlüssel und mit einem Erneuerungszeitraum von 180 Tagen festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="29197-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="29197-118">legt einen Speicherkontext für das angegebene Speicherkonto fest, wobei key1</span><span class="sxs-lookup"><span data-stu-id="29197-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="29197-119">erstellt ein Konto-SAS-Token für Dienste-BLOB,-Datei,-Tabelle und-Warteschlange, für den Ressourcentypen Dienst, Container und Objekt, mit allen Berechtigungen über HTTPS und mit dem angegebenen Anfangs-und Enddatum.</span><span class="sxs-lookup"><span data-stu-id="29197-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="29197-120">legt eine von keyvault verwaltete Speicher-SAS-Definition im Tresor fest, wobei der Vorlagen-URI als das oben erstellte SAS-Token des SAS-Typs "Konto" und 30 Tage gültig ist</span><span class="sxs-lookup"><span data-stu-id="29197-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="29197-121">Ruft das eigentliche Zugriffstoken aus dem Schlüsselspeicher Schlüssel ab, der der SAS-Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="29197-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="29197-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="29197-122">PARAMETERS</span></span>

### <span data-ttu-id="29197-123">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="29197-123">-AccountName</span></span>
<span data-ttu-id="29197-124">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="29197-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="29197-125">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="29197-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29197-126">-DefaultProfile</span></span>
<span data-ttu-id="29197-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="29197-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29197-128">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="29197-128">-Disable</span></span>
<span data-ttu-id="29197-129">Deaktiviert die Verwendung der SAS-Definition für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="29197-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="29197-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29197-130">-InputObject</span></span>
<span data-ttu-id="29197-131">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="29197-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="29197-132">-Name</span><span class="sxs-lookup"><span data-stu-id="29197-132">-Name</span></span>
<span data-ttu-id="29197-133">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="29197-133">Storage sas definition name.</span></span> <span data-ttu-id="29197-134">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="29197-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="29197-135">-SasType</span></span>
<span data-ttu-id="29197-136">Speicher-SAS-Typ.</span><span class="sxs-lookup"><span data-stu-id="29197-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="29197-137">-Tag</span></span>
<span data-ttu-id="29197-138">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="29197-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="29197-139">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="29197-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="29197-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="29197-140">-TemplateUri</span></span>
<span data-ttu-id="29197-141">Speicher-SAS-Definitions Vorlagen-URI</span><span class="sxs-lookup"><span data-stu-id="29197-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="29197-142">-ValidityPeriod</span></span>
<span data-ttu-id="29197-143">Gültigkeitszeitraum, der verwendet wird, um die Ablaufzeit des SAS-Tokens ab dem Zeitpunkt festzulegen, zu dem es generiert wird</span><span class="sxs-lookup"><span data-stu-id="29197-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-144">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="29197-144">-VaultName</span></span>
<span data-ttu-id="29197-145">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="29197-145">Vault name.</span></span>
<span data-ttu-id="29197-146">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="29197-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29197-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29197-147">-Confirm</span></span>
<span data-ttu-id="29197-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29197-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29197-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29197-149">-WhatIf</span></span>
<span data-ttu-id="29197-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29197-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29197-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29197-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29197-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29197-152">CommonParameters</span></span>
<span data-ttu-id="29197-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29197-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29197-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29197-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29197-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29197-155">INPUTS</span></span>

### <span data-ttu-id="29197-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="29197-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="29197-157">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29197-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="29197-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29197-158">OUTPUTS</span></span>

### <span data-ttu-id="29197-159">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="29197-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="29197-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="29197-160">NOTES</span></span>

## <span data-ttu-id="29197-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29197-161">RELATED LINKS</span></span>

[<span data-ttu-id="29197-162">Azureâ € ‹ RM. â € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="29197-162">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
