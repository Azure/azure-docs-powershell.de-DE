---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152716"
---
# <span data-ttu-id="12e9a-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="12e9a-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="12e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="12e9a-103">Legt eine SAS (Shared Access Signature)-Definition mit Schlüsseltresor für ein bestimmtes, vom Schlüsseltresor verwaltetes Azure -Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="12e9a-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="12e9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e9a-104">SYNTAX</span></span>

### <span data-ttu-id="12e9a-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="12e9a-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e9a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12e9a-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12e9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="12e9a-108">Legt eine SAS (Shared Access Signature)-Definition mit einem bestimmten schlüsseltresor verwalteten Azure -Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="12e9a-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="12e9a-109">Dadurch wird auch ein geheimer Schlüssel definiert, der verwendet werden kann, um das SAS-Token nach dieser SAS-Definition abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12e9a-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="12e9a-110">Das SAS-Token wird mit diesen Parametern und dem aktiven Schlüssel des verwalteten Azure -Speicherkontos generiert.</span><span class="sxs-lookup"><span data-stu-id="12e9a-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="12e9a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e9a-111">EXAMPLES</span></span>

### <span data-ttu-id="12e9a-112">Beispiel 1: Festlegen einer SAS-Definition vom Kontotyp und Abrufen eines aktuellen darauf basierenden SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="12e9a-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="12e9a-113">Legt die KONTO-SAS-Definition "accountsas" für ein von KeyVault verwaltetes Speicherkonto "mysa" im Tresor "mykv" fest.</span><span class="sxs-lookup"><span data-stu-id="12e9a-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="12e9a-114">Insbesondere führt die oben aufgeführte Sequenz Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="12e9a-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="12e9a-115">erhält ein (bereits vorhandenes) Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="12e9a-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="12e9a-116">erhält einen (bereits vorhandenen) Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="12e9a-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="12e9a-117">Fügt dem Tresor ein von KeyVault verwaltetes Speicherkonto hinzu, setzt "Key1" als aktiven Schlüssel und hat einen Zeitraum von 180 Tagen.</span><span class="sxs-lookup"><span data-stu-id="12e9a-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="12e9a-118">legt einen Speicherkontext für das angegebene Speicherkonto fest, mit Schlüssel1</span><span class="sxs-lookup"><span data-stu-id="12e9a-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="12e9a-119">erstellt ein Konto-SAS-Token für "Blob", "File", "Table" und "Queue" für die Ressourcentypen "Service", "Container" und "Object" mit allen Berechtigungen über https und mit den angegebenen Start- und Enddaten.</span><span class="sxs-lookup"><span data-stu-id="12e9a-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="12e9a-120">legt eine KEYVault-verwaltete Speicher-SAS-Definition im Tresor fest, mit dem Vorlagen-URI als oben erstelltem SAS-Token, vom SAS-Typ "account" und gültig für 30 Tage</span><span class="sxs-lookup"><span data-stu-id="12e9a-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="12e9a-121">ruft das tatsächliche Zugriffstoken aus dem geheimen Schlüssel "KeyVault" ab, der der</span><span class="sxs-lookup"><span data-stu-id="12e9a-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="12e9a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e9a-122">PARAMETERS</span></span>

### <span data-ttu-id="12e9a-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12e9a-123">-AccountName</span></span>
<span data-ttu-id="12e9a-124">Name des verwalteten Speicherkontos im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="12e9a-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="12e9a-125">Das Cmdlet erstellt den FQDN eines verwalteten Speicherkontos aus dem Namen des Tresors, der aktuell ausgewählten Umgebung und dem verwalteten Speicherkontonamen.</span><span class="sxs-lookup"><span data-stu-id="12e9a-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="12e9a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e9a-126">-DefaultProfile</span></span>
<span data-ttu-id="12e9a-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="12e9a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e9a-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="12e9a-128">-Disable</span></span>
<span data-ttu-id="12e9a-129">Deaktiviert die Verwendung der Sasdefinition für die Generation des Sas-Tokens.</span><span class="sxs-lookup"><span data-stu-id="12e9a-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="12e9a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e9a-130">-InputObject</span></span>
<span data-ttu-id="12e9a-131">ManagedStorageAccount-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12e9a-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="12e9a-132">-Name</span><span class="sxs-lookup"><span data-stu-id="12e9a-132">-Name</span></span>
<span data-ttu-id="12e9a-133">Name der Speicher-SAS-Definition.</span><span class="sxs-lookup"><span data-stu-id="12e9a-133">Storage sas definition name.</span></span> <span data-ttu-id="12e9a-134">Das Cmdlet erstellt den FQDN einer Speicher-SAS-Definition aus dem Namen des Tresors, der aktuell ausgewählten Umgebung, dem Namen des Speicherkontos und dem Namen der Sasdefinition.</span><span class="sxs-lookup"><span data-stu-id="12e9a-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="12e9a-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="12e9a-135">-SasType</span></span>
<span data-ttu-id="12e9a-136">Speicher-SAS-Typ.</span><span class="sxs-lookup"><span data-stu-id="12e9a-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="12e9a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="12e9a-137">-Tag</span></span>
<span data-ttu-id="12e9a-138">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="12e9a-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="12e9a-139">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="12e9a-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="12e9a-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="12e9a-140">-TemplateUri</span></span>
<span data-ttu-id="12e9a-141">Speicher-SAS-Definitionsvorlagen-URI.</span><span class="sxs-lookup"><span data-stu-id="12e9a-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="12e9a-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="12e9a-142">-ValidityPeriod</span></span>
<span data-ttu-id="12e9a-143">Gültigkeitszeitraum, der zum Festlegen der Ablaufzeit des Sas-Tokens ab dem Zeitpunkt der Generierte verwendet wird</span><span class="sxs-lookup"><span data-stu-id="12e9a-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="12e9a-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="12e9a-144">-VaultName</span></span>
<span data-ttu-id="12e9a-145">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="12e9a-145">Vault name.</span></span>
<span data-ttu-id="12e9a-146">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="12e9a-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="12e9a-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e9a-147">-Confirm</span></span>
<span data-ttu-id="12e9a-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e9a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e9a-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="12e9a-149">-WhatIf</span></span>
<span data-ttu-id="12e9a-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12e9a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e9a-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12e9a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e9a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e9a-152">CommonParameters</span></span>
<span data-ttu-id="12e9a-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e9a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e9a-154">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e9a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e9a-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e9a-155">INPUTS</span></span>

### <span data-ttu-id="12e9a-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="12e9a-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="12e9a-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e9a-157">OUTPUTS</span></span>

### <span data-ttu-id="12e9a-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="12e9a-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="12e9a-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12e9a-159">NOTES</span></span>

## <span data-ttu-id="12e9a-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12e9a-160">RELATED LINKS</span></span>

[<span data-ttu-id="12e9a-161">Azureâ€,RM.â€-Keyâ€.Vault</span><span class="sxs-lookup"><span data-stu-id="12e9a-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
