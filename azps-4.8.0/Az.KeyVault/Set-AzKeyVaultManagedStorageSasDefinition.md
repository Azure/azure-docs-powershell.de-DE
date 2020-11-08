---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166588"
---
# <span data-ttu-id="a6cdc-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cdc-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a6cdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cdc-103">Legt eine freigegebene zugriffssignatur Definition (SAS) mit Schlüsselspeicher für ein gegebenes, zentrales Vault Managed Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a6cdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6cdc-104">SYNTAX</span></span>

### <span data-ttu-id="a6cdc-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6cdc-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6cdc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6cdc-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6cdc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="a6cdc-108">Legt eine SAS-Definition (Shared Access Signature) mit einem angegebenen, von Vault verwalteten Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="a6cdc-109">Dadurch wird auch ein geheim Wert festgelegt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="a6cdc-110">SAS-Token wird mit diesen Parametern und dem aktiven Schlüssel des verwalteten Azure-speicherkontos für Schlüssel Vault generiert.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a6cdc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6cdc-111">EXAMPLES</span></span>

### <span data-ttu-id="a6cdc-112">Beispiel 1: Festlegen einer Kontotyp-SAS-Definition und Abrufen eines aktuellen SAS-Tokens basierend auf diesem</span><span class="sxs-lookup"><span data-stu-id="a6cdc-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="a6cdc-113">Legt eine Konto-SAS-Definition "Accounts" auf einem keyvault-verwalteten Speicherkonto "MYSA" in Vault "mykv" fest.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="a6cdc-114">Insbesondere führt die obige Abfolge die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a6cdc-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="a6cdc-115">Ruft ein (bereits vorhandenes) Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="a6cdc-116">Ruft einen (bereits vorhandenen) schlüsseltresor ab</span><span class="sxs-lookup"><span data-stu-id="a6cdc-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="a6cdc-117">Fügt dem Tresor ein von keyvault verwaltetes Speicherkonto hinzu, wobei key1 als aktiver Schlüssel und mit einem Erneuerungszeitraum von 180 Tagen festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="a6cdc-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="a6cdc-118">legt einen Speicherkontext für das angegebene Speicherkonto fest, wobei key1</span><span class="sxs-lookup"><span data-stu-id="a6cdc-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="a6cdc-119">erstellt ein Konto-SAS-Token für Dienste-BLOB,-Datei,-Tabelle und-Warteschlange, für den Ressourcentypen Dienst, Container und Objekt, mit allen Berechtigungen über HTTPS und mit dem angegebenen Anfangs-und Enddatum.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="a6cdc-120">legt eine von keyvault verwaltete Speicher-SAS-Definition im Tresor fest, wobei der Vorlagen-URI als das oben erstellte SAS-Token des SAS-Typs "Konto" und 30 Tage gültig ist</span><span class="sxs-lookup"><span data-stu-id="a6cdc-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="a6cdc-121">Ruft das eigentliche Zugriffstoken aus dem Schlüsselspeicher Schlüssel ab, der der SAS-Definition entspricht.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="a6cdc-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6cdc-122">PARAMETERS</span></span>

### <span data-ttu-id="a6cdc-123">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a6cdc-123">-AccountName</span></span>
<span data-ttu-id="a6cdc-124">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="a6cdc-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="a6cdc-125">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="a6cdc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6cdc-126">-DefaultProfile</span></span>
<span data-ttu-id="a6cdc-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a6cdc-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6cdc-128">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="a6cdc-128">-Disable</span></span>
<span data-ttu-id="a6cdc-129">Deaktiviert die Verwendung der SAS-Definition für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="a6cdc-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6cdc-130">-InputObject</span></span>
<span data-ttu-id="a6cdc-131">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="a6cdc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a6cdc-132">-Name</span></span>
<span data-ttu-id="a6cdc-133">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="a6cdc-133">Storage sas definition name.</span></span> <span data-ttu-id="a6cdc-134">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="a6cdc-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="a6cdc-135">-SasType</span></span>
<span data-ttu-id="a6cdc-136">Speicher-SAS-Typ.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="a6cdc-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6cdc-137">-Tag</span></span>
<span data-ttu-id="a6cdc-138">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a6cdc-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6cdc-139">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a6cdc-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a6cdc-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a6cdc-140">-TemplateUri</span></span>
<span data-ttu-id="a6cdc-141">Speicher-SAS-Definitions Vorlagen-URI</span><span class="sxs-lookup"><span data-stu-id="a6cdc-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="a6cdc-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="a6cdc-142">-ValidityPeriod</span></span>
<span data-ttu-id="a6cdc-143">Gültigkeitszeitraum, der verwendet wird, um die Ablaufzeit des SAS-Tokens ab dem Zeitpunkt festzulegen, zu dem es generiert wird</span><span class="sxs-lookup"><span data-stu-id="a6cdc-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="a6cdc-144">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="a6cdc-144">-VaultName</span></span>
<span data-ttu-id="a6cdc-145">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-145">Vault name.</span></span>
<span data-ttu-id="a6cdc-146">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a6cdc-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6cdc-147">-Confirm</span></span>
<span data-ttu-id="a6cdc-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6cdc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6cdc-149">-WhatIf</span></span>
<span data-ttu-id="a6cdc-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6cdc-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6cdc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cdc-152">CommonParameters</span></span>
<span data-ttu-id="a6cdc-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6cdc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cdc-154">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6cdc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cdc-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6cdc-155">INPUTS</span></span>

### <span data-ttu-id="a6cdc-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a6cdc-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="a6cdc-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6cdc-157">OUTPUTS</span></span>

### <span data-ttu-id="a6cdc-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="a6cdc-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="a6cdc-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6cdc-159">NOTES</span></span>

## <span data-ttu-id="a6cdc-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6cdc-160">RELATED LINKS</span></span>

[<span data-ttu-id="a6cdc-161">Azureâ € ‹ RM. â € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="a6cdc-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
