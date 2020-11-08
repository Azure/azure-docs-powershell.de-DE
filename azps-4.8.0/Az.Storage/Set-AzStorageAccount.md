---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165956"
---
# <span data-ttu-id="7ae58-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ae58-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="7ae58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ae58-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae58-103">Ändert ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7ae58-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="7ae58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ae58-104">SYNTAX</span></span>

### <span data-ttu-id="7ae58-105">StorageEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ae58-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae58-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7ae58-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae58-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7ae58-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ae58-108">DESCRIPTION</span></span>
<span data-ttu-id="7ae58-109">Das Cmdlet " **Satz-AzStorageAccount** " ändert ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="7ae58-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="7ae58-110">Sie können dieses Cmdlet verwenden, um den Kontotyp zu ändern, eine Kundendomäne zu aktualisieren oder Tags für ein Speicherkonto einzurichten.</span><span class="sxs-lookup"><span data-stu-id="7ae58-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="7ae58-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ae58-111">EXAMPLES</span></span>

### <span data-ttu-id="7ae58-112">Beispiel 1: Einrichten des Speicher Kontotyps</span><span class="sxs-lookup"><span data-stu-id="7ae58-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="7ae58-113">Dieser Befehl legt den Typ des speicherkontos auf Standard_RAGRS fest.</span><span class="sxs-lookup"><span data-stu-id="7ae58-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="7ae58-114">Beispiel 2: Einrichten einer benutzerdefinierten Domäne für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7ae58-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="7ae58-115">Mit diesem Befehl wird eine benutzerdefinierte Domäne für ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ae58-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="7ae58-116">Beispiel 3: Einrichten des Zugriffsstufen Werts</span><span class="sxs-lookup"><span data-stu-id="7ae58-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="7ae58-117">Mit dem Befehl wird der Wert der Access-Ebene auf "cool" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7ae58-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="7ae58-118">Beispiel 4: Einrichten der benutzerdefinierten Domäne und der Tags</span><span class="sxs-lookup"><span data-stu-id="7ae58-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="7ae58-119">Der Befehl legt die benutzerdefinierte Domäne und die Tags für ein Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="7ae58-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="7ae58-120">Beispiel 5: Konfigurieren der Schlüsselquelle für Verschlüsselung auf keyvault</span><span class="sxs-lookup"><span data-stu-id="7ae58-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="7ae58-121">Mit diesem Befehl wird die Verschlüsselungs-keySource mit einem neu erstellten keyvault gesetzt.</span><span class="sxs-lookup"><span data-stu-id="7ae58-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="7ae58-122">Beispiel 6: Verschlüsselungs-keySource auf "Microsoft. Storage" setzen</span><span class="sxs-lookup"><span data-stu-id="7ae58-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="7ae58-123">Mit diesem Befehl wird die Verschlüsselungs-keySource auf "Microsoft. Storage" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="7ae58-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="7ae58-124">Beispiel 7: Festlegen der NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON</span><span class="sxs-lookup"><span data-stu-id="7ae58-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="7ae58-125">Dieser Befehl legt die NetworkRuleSet-Eigenschaft eines speicherkontos mit JSON fest.</span><span class="sxs-lookup"><span data-stu-id="7ae58-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="7ae58-126">Beispiel 8: Abrufen der NetworkRuleSet-Eigenschaft von einem Speicherkonto und festlegen auf ein anderes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7ae58-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="7ae58-127">Dieser erste Befehl ruft die NetworkRuleSet-Eigenschaft von einem Speicherkonto ab, und der zweite Befehl legt Sie auf ein anderes Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="7ae58-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="7ae58-128">Beispiel 9: Upgraden eines speicherkontos mit der Art "Speicher" oder "BlobStorage" auf "StorageV2" Art Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="7ae58-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="7ae58-129">Mit dem Befehl wird ein Speicherkonto mit der Art "Speicher" oder "BlobStorage" auf "StorageV2"-Speicherkonto aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ae58-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="7ae58-130">Beispiel 10: Aktualisieren eines speicherkontos durch Aktivieren von Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7ae58-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="7ae58-131">Der Befehl Aktualisieren eines speicherkontos durch Aktivieren von Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="7ae58-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="7ae58-132">Beispiel 11: Aktualisieren eines speicherkontos durch Aktivieren von "Dateien" Active Directory-Domänendienst Authentifizierung und Anzeigen der Authentifizierungseinstellung "Datei Identität basiert"</span><span class="sxs-lookup"><span data-stu-id="7ae58-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="7ae58-133">Der Befehl aktualisiert ein Speicherkonto durch Aktivieren der Active Directory-Domänendienst Authentifizierung für Azure-Dateien und zeigt dann die Einstellung "Datei identitätsbasierte Authentifizierung" an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="7ae58-134">Beispiel 12: Einrichten von MinimumTlsVersion und AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="7ae58-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="7ae58-135">Der Befehl legt MinimumTlsVersion und AllowBlobPublicAccess fest und zeigt dann die zwei Eigenschaften des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="7ae58-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ae58-136">PARAMETERS</span></span>

### <span data-ttu-id="7ae58-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7ae58-137">-AccessTier</span></span>
<span data-ttu-id="7ae58-138">Gibt die Zugriffsebene des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7ae58-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="7ae58-139">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="7ae58-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="7ae58-140">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="7ae58-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="7ae58-141">Weitere Informationen finden Sie unter [Azure-BLOB-Speicher: heiße und kühle Speicherebenen](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="7ae58-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="7ae58-142">Wenn das Speicherkonto eine Art StorageV2 oder BlobStorage hat, können Sie den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7ae58-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="7ae58-143">Wenn das Speicherkonto eine Art Speicher ist, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="7ae58-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="7ae58-145">Gibt die Sicherheits-ID (Security Identifier, SID) für Azure Storage an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="7ae58-146">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="7ae58-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="7ae58-148">Gibt die GUID der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-148">Specifies the domain GUID.</span></span> <span data-ttu-id="7ae58-149">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="7ae58-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="7ae58-151">Gibt die primäre Domäne an, für die der AD-DNS-Server autorisierend ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="7ae58-152">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="7ae58-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="7ae58-154">Gibt die Sicherheits-ID (Security Identifier, SID) an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="7ae58-155">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="7ae58-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="7ae58-157">Gibt die Active Directory-Gesamtstruktur an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ae58-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="7ae58-158">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="7ae58-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="7ae58-160">Gibt den NetBIOS-Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="7ae58-161">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="7ae58-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="7ae58-163">Zulassen oder Verweigern des öffentlichen Zugriffs auf alle Blobs oder Container im Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7ae58-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ae58-164">-AsJob</span></span>
<span data-ttu-id="7ae58-165">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7ae58-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ae58-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7ae58-166">-AssignIdentity</span></span>
<span data-ttu-id="7ae58-167">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="7ae58-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7ae58-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7ae58-168">-CustomDomainName</span></span>
<span data-ttu-id="7ae58-169">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="7ae58-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae58-170">-DefaultProfile</span></span>
<span data-ttu-id="7ae58-171">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ae58-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae58-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7ae58-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7ae58-173">Aktivieren von Azure-Dateien Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7ae58-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="7ae58-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="7ae58-175">Aktivieren von Azure-Dateien Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="7ae58-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="7ae58-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="7ae58-177">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7ae58-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="7ae58-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="7ae58-179">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 tib-Kapazität unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="7ae58-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="7ae58-180">Sobald das Konto aktiviert ist, kann das Feature nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7ae58-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="7ae58-181">Wird derzeit nur für LRS-und ZRS-Replikationstypen unterstützt, daher sind Konto Konvertierungen in Geo-redundante Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="7ae58-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="7ae58-182">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="7ae58-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="7ae58-183">-Force</span><span class="sxs-lookup"><span data-stu-id="7ae58-183">-Force</span></span>
<span data-ttu-id="7ae58-184">Erzwingt, dass die Änderung in das Speicherkonto geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7ae58-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="7ae58-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7ae58-185">-KeyName</span></span>
<span data-ttu-id="7ae58-186">Wenn Sie-KeyvaultEncryption verwenden, um die Verschlüsselung mit Key Vault zu aktivieren, geben Sie die KeyName-Eigenschaft mit dieser Option an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7ae58-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="7ae58-188">Gibt an, ob Sie Microsoft keyvault für die Verschlüsselungsschlüssel verwenden möchten, wenn Sie die Speicherdienst Verschlüsselung verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ae58-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="7ae58-189">Wenn keyName, keyversion und KeyVaultUri eingestellt sind, wird keySource auf Microsoft. keyvault festgesetzt, ob dieser Parameter festgesetzt ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="7ae58-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7ae58-190">-KeyVaultUri</span></span>
<span data-ttu-id="7ae58-191">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für den schlüsseltresor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7ae58-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-192">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="7ae58-192">-KeyVersion</span></span>
<span data-ttu-id="7ae58-193">Verwenden Sie bei Verwendung der Schlüssel Vault-Verschlüsselung durch Angabe des-KeyvaultEncryption-Parameters diese Option, um den URI für die Schlüssel Version anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7ae58-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7ae58-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="7ae58-195">Die minimale TLS-Version, die bei Speicheranforderungen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-195">The minimum TLS version to be permitted on requests to storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-196">-Name</span><span class="sxs-lookup"><span data-stu-id="7ae58-196">-Name</span></span>
<span data-ttu-id="7ae58-197">Gibt den Namen des zu ändernden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-197">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ae58-198">-NetworkRuleSet</span></span>
<span data-ttu-id="7ae58-199">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7ae58-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae58-200">-ResourceGroupName</span></span>
<span data-ttu-id="7ae58-201">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ae58-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="7ae58-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7ae58-202">-SkuName</span></span>
<span data-ttu-id="7ae58-203">Gibt den SKU-Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="7ae58-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="7ae58-204">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7ae58-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ae58-205">Standard_LRS-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7ae58-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="7ae58-206">Standard_ZRS Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7ae58-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="7ae58-207">Standard_GRS-Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="7ae58-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="7ae58-208">Standard_RAGRS Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="7ae58-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="7ae58-209">Premium_LRS-Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7ae58-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="7ae58-210">Standard_GZRS-Geo-redundante Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7ae58-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="7ae58-211">Standard_RAGZRS-Read Access Geo-redundant Zone-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="7ae58-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="7ae58-212">Standard_ZRS-und Premium_LRS Typen können nicht in andere Kontotypen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7ae58-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="7ae58-213">Sie können andere Kontotypen nicht in Standard_ZRS oder Premium_LRS ändern.</span><span class="sxs-lookup"><span data-stu-id="7ae58-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="7ae58-214">-StorageEncryption</span></span>
<span data-ttu-id="7ae58-215">Gibt an, ob die Speicherkonto Verschlüsselung für die Verwendung von Microsoft-verwalteten Schlüsseln festgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ae58-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-216">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ae58-216">-Tag</span></span>
<span data-ttu-id="7ae58-217">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7ae58-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7ae58-218">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7ae58-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7ae58-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="7ae58-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="7ae58-220">Upgrade des speicherkontos Art von Speicher-oder BlobStorage auf StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7ae58-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="7ae58-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="7ae58-221">-UseSubDomain</span></span>
<span data-ttu-id="7ae58-222">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ae58-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="7ae58-223">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ae58-223">-Confirm</span></span>
<span data-ttu-id="7ae58-224">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ae58-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae58-225">-WhatIf</span></span>
<span data-ttu-id="7ae58-226">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ae58-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ae58-227">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ae58-227">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae58-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae58-228">CommonParameters</span></span>
<span data-ttu-id="7ae58-229">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae58-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae58-230">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae58-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae58-231">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ae58-231">INPUTS</span></span>

### <span data-ttu-id="7ae58-232">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae58-232">System.String</span></span>

### <span data-ttu-id="7ae58-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ae58-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ae58-234">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ae58-234">OUTPUTS</span></span>

### <span data-ttu-id="7ae58-235">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ae58-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7ae58-236">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ae58-236">NOTES</span></span>

## <span data-ttu-id="7ae58-237">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ae58-237">RELATED LINKS</span></span>

[<span data-ttu-id="7ae58-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ae58-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="7ae58-239">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ae58-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="7ae58-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ae58-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
