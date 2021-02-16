---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150404"
---
# <span data-ttu-id="aa073-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa073-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="aa073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa073-102">SYNOPSIS</span></span>
<span data-ttu-id="aa073-103">Ändert ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="aa073-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="aa073-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa073-104">SYNTAX</span></span>

### <span data-ttu-id="aa073-105">StorageEncryption (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa073-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa073-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="aa073-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa073-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="aa073-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa073-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa073-108">DESCRIPTION</span></span>
<span data-ttu-id="aa073-109">Das **Cmdlet Set-AzStorageAccount** ändert ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="aa073-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="aa073-110">Mit diesem Cmdlet können Sie den Kontotyp ändern, eine Kundendomäne aktualisieren oder Tags für ein Speicherkonto festlegen.</span><span class="sxs-lookup"><span data-stu-id="aa073-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="aa073-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa073-111">EXAMPLES</span></span>

### <span data-ttu-id="aa073-112">Beispiel 1: Festlegen des Kontotyps "Speicher"</span><span class="sxs-lookup"><span data-stu-id="aa073-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="aa073-113">Mit diesem Befehl wird der Typ des Speicherkontos auf Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="aa073-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="aa073-114">Beispiel 2: Festlegen einer benutzerdefinierten Domäne für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="aa073-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="aa073-115">Dieser Befehl legt eine benutzerdefinierte Domäne für ein Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="aa073-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="aa073-116">Beispiel 3: Festlegen des Zugriffsstufenwerts</span><span class="sxs-lookup"><span data-stu-id="aa073-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="aa073-117">Mit dem Befehl wird der Wert der Zugriffsebene auf "cool" definiert.</span><span class="sxs-lookup"><span data-stu-id="aa073-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="aa073-118">Beispiel 4: Festlegen der benutzerdefinierten Domäne und Tags</span><span class="sxs-lookup"><span data-stu-id="aa073-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="aa073-119">Der Befehl legt die benutzerdefinierte Domäne und Tags für ein Speicherkonto fest.</span><span class="sxs-lookup"><span data-stu-id="aa073-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="aa073-120">Beispiel 5: Festlegen von Verschlüsselungsschlüsselquelle auf Keyvault</span><span class="sxs-lookup"><span data-stu-id="aa073-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="aa073-121">Dieser Befehl setzt "Encryption KeySource" mit einem neu erstellten Keyvault.</span><span class="sxs-lookup"><span data-stu-id="aa073-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="aa073-122">Beispiel 6: Festlegen von Verschlüsselungsschlüsselquelle auf "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="aa073-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="aa073-123">Mit diesem Befehl wurde "Encryption KeySource" auf "Microsoft.Storage" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa073-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="aa073-124">Beispiel 7: Festlegen der Eigenschaft "NetworkRuleSet" eines Speicherkontos mit JSON</span><span class="sxs-lookup"><span data-stu-id="aa073-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="aa073-125">Dieser Befehl legt die "NetworkRuleSet"-Eigenschaft eines Speicherkontos mit JSON fest.</span><span class="sxs-lookup"><span data-stu-id="aa073-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="aa073-126">Beispiel 8: Erhalten der Eigenschaft "NetworkRuleSet" aus einem Speicherkonto und Festlegen der Eigenschaft auf ein anderes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="aa073-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="aa073-127">Mit diesem ersten Befehl wird die Eigenschaft "NetworkRuleSet" aus einem Speicherkonto und mit dem zweiten Befehl auf ein anderes Speicherkonto definiert.</span><span class="sxs-lookup"><span data-stu-id="aa073-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="aa073-128">Beispiel 9: Upgrade eines Speicherkontos mit der Art "Storage" oder "BlobStorage" auf das Speicherkonto der Art "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="aa073-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="aa073-129">Mit dem Befehl wird ein Speicherkonto mit dem Kind "Storage" oder "BlobStorage" auf das Speicherkonto der Art "StorageV2" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aa073-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="aa073-130">Beispiel 10: Aktualisieren eines Speicherkontos durch Aktivieren der Azure Files AAD DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="aa073-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="aa073-131">Mit dem Befehl wird ein Speicherkonto aktualisiert, indem Azure Files AAD DS Authentication aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="aa073-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="aa073-132">Beispiel 11: Aktualisieren eines Speicherkontos durch Aktivieren der Active Directory-Domänendienstauthentifizierung und Anzeigen der Einstellung für die dateiidentitätsbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="aa073-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="aa073-133">Der Befehl aktualisiert ein Speicherkonto, indem Azure Files Active Directory Domain Service Authentication aktiviert wird, und zeigt dann die Einstellung für die dateiidentitätsbasierte Authentifizierung an.</span><span class="sxs-lookup"><span data-stu-id="aa073-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="aa073-134">Beispiel 12: Festlegen von MinimumTlsVersion und AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="aa073-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="aa073-135">Der Befehl legt "MinimumTlsVersion" und "AllowBlobPublicAccess" fest und zeigt dann die zwei Eigenschaften des Kontos an.</span><span class="sxs-lookup"><span data-stu-id="aa073-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="aa073-136">Beispiel 13: Aktualisieren eines Speicherkontos mit der Einstellung "RoutingPreference"</span><span class="sxs-lookup"><span data-stu-id="aa073-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="aa073-137">Mit diesem Befehl wird ein Speicherkonto mit der Einstellung "RoutingPreference" aktualisiert: "PublishMicrosoftEndpoint" als "false", "PublishInternetEndpoint as true" und "RoutingChoice" als "MicrosoftRouting".</span><span class="sxs-lookup"><span data-stu-id="aa073-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="aa073-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa073-138">PARAMETERS</span></span>

### <span data-ttu-id="aa073-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="aa073-139">-AccessTier</span></span>
<span data-ttu-id="aa073-140">Gibt die Zugriffsebene des Speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aa073-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="aa073-141">Die zulässigen Werte für diesen Parameter sind: "Hot" und "Cool".</span><span class="sxs-lookup"><span data-stu-id="aa073-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="aa073-142">Wenn Sie die Zugriffsebene ändern, kann dies zu zusätzlichen Gebühren führen.</span><span class="sxs-lookup"><span data-stu-id="aa073-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="aa073-143">Weitere Informationen finden Sie unter [Azure Blob Storage: Hot and cool storage tiers.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="aa073-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="aa073-144">Wenn das Konto "Storage" über "Kind" als "StorageV2" oder "BlobStorage" verfügt, können Sie den Parameter *"AccessTier"* angeben.</span><span class="sxs-lookup"><span data-stu-id="aa073-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="aa073-145">Wenn das Konto "Storage" über "Kind as Storage" verfügt, geben Sie den Parameter *"AccessTier" nicht* an.</span><span class="sxs-lookup"><span data-stu-id="aa073-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="aa073-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="aa073-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="aa073-147">Gibt die Sicherheits-ID (SID) für Azure Storage an.</span><span class="sxs-lookup"><span data-stu-id="aa073-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="aa073-148">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="aa073-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="aa073-150">Gibt die Domänen-GUID an.</span><span class="sxs-lookup"><span data-stu-id="aa073-150">Specifies the domain GUID.</span></span> <span data-ttu-id="aa073-151">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="aa073-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="aa073-153">Gibt die primäre Domäne an, für die der AD -DNS-Server autoritativ ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="aa073-154">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="aa073-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="aa073-156">Gibt die Sicherheits-ID (SID) an.</span><span class="sxs-lookup"><span data-stu-id="aa073-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="aa073-157">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="aa073-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="aa073-159">Gibt die active Directory-Gesamtstruktur an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="aa073-160">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-161">-ActiveDirectoryNetDomäneName</span><span class="sxs-lookup"><span data-stu-id="aa073-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="aa073-162">Gibt den Domänennamen von NetERGEBNISS an.</span><span class="sxs-lookup"><span data-stu-id="aa073-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="aa073-163">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="aa073-164">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="aa073-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="aa073-165">Ermöglichen oder unterbinden Sie den öffentlichen Zugriff auf alle BLOBs oder Container im Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="aa073-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="aa073-166">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa073-166">-AsJob</span></span>
<span data-ttu-id="aa073-167">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aa073-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa073-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="aa073-168">-AssignIdentity</span></span>
<span data-ttu-id="aa073-169">Generieren und zuweisen Sie eine neue Speicherkontoidentität für dieses Speicherkonto zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="aa073-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="aa073-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="aa073-170">-CustomDomainName</span></span>
<span data-ttu-id="aa073-171">Gibt den Namen der benutzerdefinierten Domäne an.</span><span class="sxs-lookup"><span data-stu-id="aa073-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="aa073-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa073-172">-DefaultProfile</span></span>
<span data-ttu-id="aa073-173">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa073-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa073-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="aa073-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="aa073-175">Aktivieren Sie azure files Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="aa073-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="aa073-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="aa073-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="aa073-177">Aktivieren Sie azure files Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="aa073-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="aa073-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="aa073-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="aa073-179">Gibt an, ob das Speicherkonto nur den HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="aa073-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="aa073-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="aa073-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="aa073-181">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 TiB-Kapazität unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="aa073-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="aa073-182">Sobald das Konto aktiviert ist, kann das Feature nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="aa073-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="aa073-183">Derzeit nur für LRS- und ZRS-Replikationstypen unterstützt, daher sind Kontokonvertierungen in georedundanter Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="aa073-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="aa073-184">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="aa073-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="aa073-185">-Force</span><span class="sxs-lookup"><span data-stu-id="aa073-185">-Force</span></span>
<span data-ttu-id="aa073-186">Erzwingt, dass die Änderung in das Speicherkonto geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="aa073-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="aa073-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aa073-187">-KeyName</span></span>
<span data-ttu-id="aa073-188">Wenn Sie die Verschlüsselung mit dem Schlüsseltresor mithilfe der -KeyvaultEncryption aktivieren, geben Sie die Eigenschaft "Keyname" mit dieser Option an.</span><span class="sxs-lookup"><span data-stu-id="aa073-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="aa073-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="aa073-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="aa073-190">Gibt an, ob Bei Verwendung der Speicherdienstverschlüsselung Microsoft KeyVault für die Verschlüsselungsschlüssel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="aa073-191">Wenn KeyName, KeyVersion und KeyVaultUri alle festgelegt sind, wird KeySource auf "Microsoft.Keyvault" festgelegt, unabhängig davon, ob dieser Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="aa073-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="aa073-192">-KeyVaultUri</span></span>
<span data-ttu-id="aa073-193">Wenn Sie die Schlüsseltresorverschlüsselung verwenden, indem Sie den Parameter "-KeyvaultEncryption" angeben, verwenden Sie diese Option, um den URI für den Schlüsseltresor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa073-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="aa073-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="aa073-194">-KeyVersion</span></span>
<span data-ttu-id="aa073-195">Wenn Sie die Schlüsseltresorverschlüsselung verwenden, indem Sie den Parameter "-KeyvaultEncryption" angeben, verwenden Sie diese Option, um den URI für die Schlüsselversion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa073-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="aa073-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="aa073-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="aa073-197">Die mindestens zulässige TLS-Version für Speicheranforderungen.</span><span class="sxs-lookup"><span data-stu-id="aa073-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="aa073-198">-Name</span><span class="sxs-lookup"><span data-stu-id="aa073-198">-Name</span></span>
<span data-ttu-id="aa073-199">Gibt den Namen des Speicherkontos an, das geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="aa073-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa073-200">-NetworkRuleSet</span></span>
<span data-ttu-id="aa073-201">NetworkRuleSet dient zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften wie Dienste, die die Regeln umgehen dürfen, und zum Behandeln von Anforderungen, die keine der definierten Regeln erfüllen.</span><span class="sxs-lookup"><span data-stu-id="aa073-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="aa073-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa073-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="aa073-203">Gibt an, ob Internetroutingspeicherendpunkte veröffentlicht werden sollen</span><span class="sxs-lookup"><span data-stu-id="aa073-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="aa073-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="aa073-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="aa073-205">Gibt an, ob Microsoft-Routing-Speicherendpunkte veröffentlicht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="aa073-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="aa073-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa073-206">-ResourceGroupName</span></span>
<span data-ttu-id="aa073-207">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="aa073-208">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="aa073-208">-RoutingChoice</span></span>
<span data-ttu-id="aa073-209">Die Routingauswahl definiert die Art des vom Benutzer gewählten Netzwerkroutings.</span><span class="sxs-lookup"><span data-stu-id="aa073-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="aa073-210">Mögliche Werte sind: "MicrosoftRouting", "InternetRouting".</span><span class="sxs-lookup"><span data-stu-id="aa073-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa073-211">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aa073-211">-SkuName</span></span>
<span data-ttu-id="aa073-212">Gibt den Namen der SKU des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="aa073-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="aa073-213">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="aa073-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa073-214">Standard_LRS - Lokal redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="aa073-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="aa073-215">Standard_ZRS - Zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="aa073-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="aa073-216">Standard_GRS – Georedundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="aa073-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="aa073-217">Standard_RAGRS – Georedundanter Speicher mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="aa073-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="aa073-218">Premium_LRS – Lokal redundanter Premiumspeicher.</span><span class="sxs-lookup"><span data-stu-id="aa073-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="aa073-219">Standard_GZRS – Georedundanter zonenredundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="aa073-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="aa073-220">Standard_RAGZRS – Georedundanter zonenredundanter Speicher mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="aa073-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="aa073-221">Sie können keine Standard_ZRS und Premium_LRS Typen in andere Kontotypen ändern.</span><span class="sxs-lookup"><span data-stu-id="aa073-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="aa073-222">Sie können keine anderen Kontotypen in "Standard_ZRS" oder "Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="aa073-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="aa073-223">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="aa073-223">-StorageEncryption</span></span>
<span data-ttu-id="aa073-224">Gibt an, ob die Verschlüsselung des Speicherkontos auf die Verwendung von von Microsoft verwalteten Schlüsseln festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="aa073-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa073-225">-Tag</span></span>
<span data-ttu-id="aa073-226">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="aa073-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="aa073-227">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aa073-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa073-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="aa073-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="aa073-229">Aktualisieren Sie die Art des Speicherkontos von "Storage" oder "BlobStorage" auf "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="aa073-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="aa073-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="aa073-230">-UseSubDomain</span></span>
<span data-ttu-id="aa073-231">Gibt an, ob die indirekte #A0 aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa073-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="aa073-232">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa073-232">-Confirm</span></span>
<span data-ttu-id="aa073-233">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa073-233">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa073-234">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aa073-234">-WhatIf</span></span>
<span data-ttu-id="aa073-235">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa073-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa073-236">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa073-236">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa073-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa073-237">CommonParameters</span></span>
<span data-ttu-id="aa073-238">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa073-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa073-239">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa073-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa073-240">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa073-240">INPUTS</span></span>

### <span data-ttu-id="aa073-241">System.String</span><span class="sxs-lookup"><span data-stu-id="aa073-241">System.String</span></span>

### <span data-ttu-id="aa073-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aa073-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aa073-243">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa073-243">OUTPUTS</span></span>

### <span data-ttu-id="aa073-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa073-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="aa073-245">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa073-245">NOTES</span></span>

## <span data-ttu-id="aa073-246">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa073-246">RELATED LINKS</span></span>

[<span data-ttu-id="aa073-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa073-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="aa073-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa073-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="aa073-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa073-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
