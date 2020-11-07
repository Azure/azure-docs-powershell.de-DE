---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 48b5182efd368b0950313ac4d2c7b2e23f2948fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843848"
---
# <span data-ttu-id="2d7bf-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2d7bf-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2d7bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7bf-103">Legt eine freigegebene zugriffssignatur Definition (SAS) mit Schlüsselspeicher für ein gegebenes, zentrales Vault Managed Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2d7bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d7bf-104">SYNTAX</span></span>

### <span data-ttu-id="2d7bf-105">RawSas (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d7bf-105">RawSas (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-106">AdhocAccountSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-107">AdhocServiceBlobSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-108">AdhocServiceContainerSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-109">AdhocServiceFileSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-110">AdhocServiceShareSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-111">AdhocServiceQueueSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-112">AdhocServiceTableSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d7bf-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="2d7bf-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7bf-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d7bf-119">DESCRIPTION</span></span>
<span data-ttu-id="2d7bf-120">Legt eine SAS-Definition (Shared Access Signature) mit einem angegebenen, von Vault verwalteten Azure-Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="2d7bf-121">Dadurch wird auch ein geheim Wert festgelegt, der zum Abrufen des SAS-Tokens pro dieser SAS-Definition verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="2d7bf-122">SAS-Token wird mit diesen Parametern und dem aktiven Schlüssel des verwalteten Azure-speicherkontos für Schlüssel Vault generiert.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2d7bf-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d7bf-123">EXAMPLES</span></span>

### <span data-ttu-id="2d7bf-124">Beispiel 1: Festlegen einer BLOB-SAS-Definition für Ad-hoc-Dienste</span><span class="sxs-lookup"><span data-stu-id="2d7bf-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="2d7bf-125">Legt eine Ad-hoc-Dienst-BLOB-SAS-Definition "sas1" mit dem Schlüsseldepot-verwalteten Speicherkonto "computerkonto1" in Vault "vault1" fest.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="2d7bf-126">Beispiel 2: Festlegen einer SAS-Definition für Ad-hoc-Konten</span><span class="sxs-lookup"><span data-stu-id="2d7bf-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="2d7bf-127">Legt eine Ad-hoc-BLOB-SAS-Definition "sas1" mit dem Schlüsseldepot-verwalteten Speicherkonto "computerkonto1" in Vault "vault1" fest.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="2d7bf-128">Beispiel 3: Festlegen einer SAS-Definition mithilfe einer Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d7bf-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="2d7bf-129">Legt eine Ad-hoc-BLOB-SAS-Definition "sas1" mit dem Schlüsseldepot-verwalteten Speicherkonto "computerkonto1" in Vault "vault1" mit einer Hashtable fest.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="2d7bf-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d7bf-130">PARAMETERS</span></span>

### <span data-ttu-id="2d7bf-131">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="2d7bf-131">-AccountName</span></span>
<span data-ttu-id="2d7bf-132">Name des verwalteten speicherkontos in Key Vault</span><span class="sxs-lookup"><span data-stu-id="2d7bf-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="2d7bf-133">Cmdlet erstellt den FQDN eines verwalteten Speicherkonto namens aus Vault Name, aktuell ausgewählter Umgebung und verwaltetem Speicherkonto Namen.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2d7bf-134">-ApiVersion</span></span>
<span data-ttu-id="2d7bf-135">Gibt die Speicherdienst Version an, die zum Ausführen der Anforderung verwendet wird, die mit dem Konto-SAS-URI erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-136">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2d7bf-136">-Blob</span></span>
<span data-ttu-id="2d7bf-137">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-138">-Container</span><span class="sxs-lookup"><span data-stu-id="2d7bf-138">-Container</span></span>
<span data-ttu-id="2d7bf-139">Container Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7bf-140">-DefaultProfile</span></span>
<span data-ttu-id="2d7bf-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2d7bf-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d7bf-142">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="2d7bf-142">-Disable</span></span>
<span data-ttu-id="2d7bf-143">Deaktiviert die Verwendung der SAS-Definition für die Generierung von SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="2d7bf-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2d7bf-144">-EndPartitionKey</span></span>
<span data-ttu-id="2d7bf-145">Ende der Partitions Taste</span><span class="sxs-lookup"><span data-stu-id="2d7bf-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="2d7bf-146">-EndRowKey</span></span>
<span data-ttu-id="2d7bf-147">Zeilenschlüssel beenden</span><span class="sxs-lookup"><span data-stu-id="2d7bf-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2d7bf-148">-IPAddressOrRange</span></span>
<span data-ttu-id="2d7bf-149">IP-oder IP-Bereichs-ACL (Zugriffssteuerungsliste) der Anforderung, die von Azure Storage akzeptiert würde.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-150">-Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-150">-Name</span></span>
<span data-ttu-id="2d7bf-151">Name der Speicher-SAS-Definition</span><span class="sxs-lookup"><span data-stu-id="2d7bf-151">Storage sas definition name.</span></span> <span data-ttu-id="2d7bf-152">Cmdlet erstellt den FQDN einer Speicher SAS-Definition aus Vault-Name, aktuell ausgewählter Umgebung, Speicherkonto Name und SAS-Definitionsname.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="2d7bf-153">-Parameter</span></span>
<span data-ttu-id="2d7bf-154">SAS-Definitions Parameter, die zum Erstellen des SAS-Tokens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-155">-Path</span><span class="sxs-lookup"><span data-stu-id="2d7bf-155">-Path</span></span>
<span data-ttu-id="2d7bf-156">Der Pfad zur clouddatei, für die ein SAS-Token erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-157">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="2d7bf-157">-Permission</span></span>
<span data-ttu-id="2d7bf-158">Berechtigungs.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-158">Permission.</span></span> <span data-ttu-id="2d7bf-159">Werte sind "Abfrage", "hinzufügen", "Aktualisieren", "Prozess".</span><span class="sxs-lookup"><span data-stu-id="2d7bf-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-160">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="2d7bf-160">-Policy</span></span>
<span data-ttu-id="2d7bf-161">Richtlinien Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2d7bf-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-162">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2d7bf-162">-Protocol</span></span>
<span data-ttu-id="2d7bf-163">Das Protokoll kann in der Anforderung mit dem SAS-Token verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-164">-Queue</span><span class="sxs-lookup"><span data-stu-id="2d7bf-164">-Queue</span></span>
<span data-ttu-id="2d7bf-165">Warteschlangen Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-166">-</span><span class="sxs-lookup"><span data-stu-id="2d7bf-166">-ResourceType</span></span>
<span data-ttu-id="2d7bf-167">Ressourcentypen, auf die sich dieses SAS-Token bezieht.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="2d7bf-168">Werte sind "Service", "Container", "Objekt"</span><span class="sxs-lookup"><span data-stu-id="2d7bf-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-169">-Service</span><span class="sxs-lookup"><span data-stu-id="2d7bf-169">-Service</span></span>
<span data-ttu-id="2d7bf-170">Diensttypen, auf die sich dieses SAS-Token bezieht.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="2d7bf-171">Werte sind "BLOB", "Datei", "Warteschlange", "Tabelle"</span><span class="sxs-lookup"><span data-stu-id="2d7bf-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-172">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="2d7bf-172">-Share</span></span>
<span data-ttu-id="2d7bf-173">Freigabe Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="2d7bf-174">-SharedAccessHeader</span></span>
<span data-ttu-id="2d7bf-175">Gibt die Abfrageparameter an, um die Antwortheader zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2d7bf-176">-StartPartitionKey</span></span>
<span data-ttu-id="2d7bf-177">Partitionsschlüssel starten</span><span class="sxs-lookup"><span data-stu-id="2d7bf-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="2d7bf-178">-StartRowKey</span></span>
<span data-ttu-id="2d7bf-179">Start Zeilen Taste</span><span class="sxs-lookup"><span data-stu-id="2d7bf-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-180">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="2d7bf-180">-Table</span></span>
<span data-ttu-id="2d7bf-181">Tabellen Name</span><span class="sxs-lookup"><span data-stu-id="2d7bf-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d7bf-182">-Tag</span></span>
<span data-ttu-id="2d7bf-183">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2d7bf-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d7bf-184">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2d7bf-184">For example:</span></span>

<span data-ttu-id="2d7bf-185">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2d7bf-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d7bf-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="2d7bf-186">-TargetStorageVersion</span></span>
<span data-ttu-id="2d7bf-187">Gibt die signierte Speicherdienst Version an, die zum Authentifizieren von Anforderungen verwendet wird, die mit dem SAS-Token erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="2d7bf-188">-ValidityPeriod</span></span>
<span data-ttu-id="2d7bf-189">Gültigkeitszeitraum, der verwendet wird, um die Ablaufzeit des SAS-Tokens ab dem Zeitpunkt festzulegen, zu dem es generiert wird</span><span class="sxs-lookup"><span data-stu-id="2d7bf-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d7bf-190">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2d7bf-190">-VaultName</span></span>
<span data-ttu-id="2d7bf-191">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-191">Vault name.</span></span>
<span data-ttu-id="2d7bf-192">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2d7bf-193">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d7bf-193">-Confirm</span></span>
<span data-ttu-id="2d7bf-194">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7bf-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7bf-195">-WhatIf</span></span>
<span data-ttu-id="2d7bf-196">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7bf-197">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7bf-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7bf-198">CommonParameters</span></span>
<span data-ttu-id="2d7bf-199">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7bf-200">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7bf-200">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7bf-201">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d7bf-201">INPUTS</span></span>

### <span data-ttu-id="2d7bf-202">Keine</span><span class="sxs-lookup"><span data-stu-id="2d7bf-202">None</span></span>
<span data-ttu-id="2d7bf-203">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2d7bf-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d7bf-204">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d7bf-204">OUTPUTS</span></span>

### <span data-ttu-id="2d7bf-205">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2d7bf-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2d7bf-206">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d7bf-206">NOTES</span></span>

## <span data-ttu-id="2d7bf-207">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d7bf-207">RELATED LINKS</span></span>

[<span data-ttu-id="2d7bf-208">Azureâ € ‹ RM. â € ‹ keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="2d7bf-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/Az.keyvault/)
