---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939848"
---
# <span data-ttu-id="a3a89-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3a89-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="a3a89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3a89-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a89-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a3a89-103">Creates a Storage account.</span></span>

## <span data-ttu-id="a3a89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3a89-104">SYNTAX</span></span>

### <span data-ttu-id="a3a89-105">AzureActiveDirectoryDomainServicesForFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3a89-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="a3a89-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a3a89-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3a89-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3a89-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a89-108">Das **Cmdlet New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="a3a89-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="a3a89-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3a89-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a89-110">Beispiel 1: Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a3a89-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="a3a89-111">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen MyResourceGroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="a3a89-112">Beispiel 2: Erstellen eines Blob Storage-Kontos mit BlobStorage Kind und hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="a3a89-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="a3a89-113">Mit diesem Befehl wird ein Blob Storage-Konto erstellt, das mit BlobStorage Kind und hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="a3a89-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="a3a89-114">Beispiel 3: Erstellen eines Speicherkontos mit Kind StorageV2 und Generieren und Zuweisen einer Identität für Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a3a89-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="a3a89-115">Mit diesem Befehl wird ein Speicherkonto mit Kind StorageV2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="a3a89-116">Außerdem wird eine Identität generiert und zugewiesen, die zum Verwalten von Kontoschlüsseln über Azure KeyVault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a3a89-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="a3a89-117">Beispiel 4: Erstellen eines Speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="a3a89-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="a3a89-118">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="a3a89-119">Beispiel 5: Erstellen eines Speicherkontos mit aktivierter Hierarchischer Namespace.</span><span class="sxs-lookup"><span data-stu-id="a3a89-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="a3a89-120">Mit diesem Befehl wird ein Speicherkonto erstellt, bei dem hierarchischer Namespace aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="a3a89-121">Beispiel 6: Erstellen Sie ein Speicherkonto mit azure files AAD DS Authentication, und aktivieren Sie die große Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="a3a89-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="a3a89-122">Mit diesem Befehl wird ein Speicherkonto mit azure files AAD DS Authentication erstellt, und es wird eine große Dateifreigabe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3a89-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="a3a89-123">Beispiel 7: Erstellen eines Speicherkontos mit Aktivieren der Active Directory-Domänendienstauthentifizierung für Dateien.</span><span class="sxs-lookup"><span data-stu-id="a3a89-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="a3a89-124">Mit diesem Befehl wird ein Speicherkonto mit der Active Directory-Domänendienstauthentifizierung für Dateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="a3a89-125">Beispiel 8: Erstellen eines Speicherkontos mit dem Verschlüsselungsschlüssel "Warteschlange" und "Tabellendienst" verwenden den Verschlüsselungsschlüssel für den Kontobereich und Infrastrukturverschlüsselung erfordern.</span><span class="sxs-lookup"><span data-stu-id="a3a89-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="a3a89-126">Mit diesem Befehl wird ein Speicherkonto erstellt, bei dem Warteschlangen- und Tabellendienst den Verschlüsselungsschlüssel für den Kontobereich verwenden und Infrastrukturverschlüsselung erfordern. Warteschlange und Tabelle verwenden also denselben Verschlüsselungsschlüssel mit Blob- und File-Dienst, und der Dienst verwendet eine sekundäre Verschlüsselungsebene mit plattformver verwalteten Schlüsseln für ruhende Daten.</span><span class="sxs-lookup"><span data-stu-id="a3a89-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="a3a89-127">Holen Sie sich dann die Eigenschaften des Speicherkontos, und zeigen Sie den Verschlüsselungsschlüsseltyp "Warteschlangen- und Tabellendienst" sowie den Wert "RequireInfrastructureEncryption" an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="a3a89-128">Beispiel 9: Erstellen eines Kontos MinimumTlsVersion und AllowBlobPublicAccess und Deaktivieren von SharedKey Access</span><span class="sxs-lookup"><span data-stu-id="a3a89-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="a3a89-129">Mit dem Befehl Konto erstellen mit MinimumTlsVersion, AllowBlobPublicAccess und Deaktivieren des SharedKey-Zugriffs auf das Konto, und zeigen Sie dann die drei Eigenschaften des erstellten Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="a3a89-130">Beispiel 10: Erstellen eines Speicherkontos mit RoutingPreference-Einstellung</span><span class="sxs-lookup"><span data-stu-id="a3a89-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="a3a89-131">Mit diesem Befehl wird ein Speicherkonto mit der Einstellung RoutingPreference erstellt: PublishMicrosoftEndpoint und PublishInternetEndpoint als true und RoutingChoice als MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="a3a89-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="a3a89-132">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3a89-132">PARAMETERS</span></span>

### <span data-ttu-id="a3a89-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="a3a89-133">-AccessTier</span></span>
<span data-ttu-id="a3a89-134">Gibt die Zugriffsebene des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3a89-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="a3a89-135">Die zulässigen Werte für diesen Parameter sind: "Warm" und "Cool".</span><span class="sxs-lookup"><span data-stu-id="a3a89-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="a3a89-136">Wenn Sie einen Wert von BlobStorage für den *Parameter Kind* angeben, müssen Sie einen Wert für den *AccessTier-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="a3a89-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="a3a89-137">Wenn Sie einen Wert von Storage für diesen *Parameter "Kind"* angeben, geben Sie den *Parameter AccessTier nicht* an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="a3a89-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="a3a89-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="a3a89-139">Gibt den Sicherheitsbezeichner (Security Identifier, SID) für Azure Storage an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="a3a89-140">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="a3a89-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="a3a89-142">Gibt die Domänen-GUID an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-142">Specifies the domain GUID.</span></span> <span data-ttu-id="a3a89-143">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="a3a89-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="a3a89-145">Gibt die primäre Domäne an, für die der AD -DNS-Server autoritativ ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="a3a89-146">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="a3a89-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="a3a89-148">Gibt den Sicherheitsbezeichner (SID) an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="a3a89-149">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="a3a89-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="a3a89-151">Gibt die zu erhaltende Active Directory-Gesamtstruktur an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="a3a89-152">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="a3a89-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="a3a89-154">Gibt den NetBIOS-Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="a3a89-155">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="a3a89-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="a3a89-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="a3a89-157">Zulassen des öffentlichen Zugriffs auf alle Blobs oder Container im Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a3a89-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="a3a89-158">Die Standardinterpretation gilt für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a3a89-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="a3a89-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="a3a89-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="a3a89-160">Gibt an, ob das Speicherkonto die Genehmigung von Anforderungen mit dem Kontozugriffsschlüssel über freigegebenen Schlüssel zulässt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="a3a89-161">Ist false, müssen alle Anforderungen, einschließlich Signaturen für den gemeinsamen Zugriff, mit Azure Active Directory (Azure AD) autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3a89-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="a3a89-162">Der Standardwert ist null, was dem Wert "true" entspricht.</span><span class="sxs-lookup"><span data-stu-id="a3a89-162">The default value is null, which is equivalent to true.</span></span>

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

### <span data-ttu-id="a3a89-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3a89-163">-AsJob</span></span>
<span data-ttu-id="a3a89-164">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3a89-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3a89-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a3a89-165">-AssignIdentity</span></span>
<span data-ttu-id="a3a89-166">Generieren und Zuweisen einer neuen Speicherkontoidentität für dieses Speicherkonto für die Verwendung mit wichtigen Verwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a3a89-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a3a89-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a3a89-167">-CustomDomainName</span></span>
<span data-ttu-id="a3a89-168">Gibt den Namen der benutzerdefinierten Domäne des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="a3a89-169">Der Standardwert ist Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="a3a89-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a89-170">-DefaultProfile</span></span>
<span data-ttu-id="a3a89-171">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3a89-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a89-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a3a89-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="a3a89-173">Aktivieren Sie azure files Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a3a89-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="a3a89-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="a3a89-175">Aktivieren Sie Azure Files Azure Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="a3a89-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="a3a89-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="a3a89-177">Gibt an, ob das Speicherkonto hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3a89-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="a3a89-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="a3a89-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="a3a89-179">Gibt an, ob das Speicherkonto nur den HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3a89-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="a3a89-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="a3a89-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="a3a89-181">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 TiB-Kapazität unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a3a89-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="a3a89-182">Nachdem das Konto aktiviert wurde, kann das Feature nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a3a89-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="a3a89-183">Derzeit wird nur für LRS- und ZRS-Replikationstypen unterstützt, daher wären Kontokonvertierungen in georedundant konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="a3a89-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="a3a89-184">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="a3a89-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="a3a89-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="a3a89-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="a3a89-186">Legen Sie den Verschlüsselungsschlüsseltyp für warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="a3a89-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="a3a89-187">Der Standardwert ist Dienst.</span><span class="sxs-lookup"><span data-stu-id="a3a89-187">The default value is Service.</span></span>
<span data-ttu-id="a3a89-188">-Konto: Die Warteschlange wird mit dem Verschlüsselungsschlüssel für den Kontobereich verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="a3a89-189">-Dienst: Die Warteschlange wird immer mit Service-Managed verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="a3a89-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="a3a89-191">Legen Sie den Verschlüsselungsschlüsseltyp für Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="a3a89-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="a3a89-192">Der Standardwert ist Dienst.</span><span class="sxs-lookup"><span data-stu-id="a3a89-192">The default value is Service.</span></span>
- <span data-ttu-id="a3a89-193">Konto: Die Tabelle wird mit dem Verschlüsselungsschlüssel für den Kontobereich verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="a3a89-194">Dienst: Die Tabelle wird immer mit Service-Managed verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="a3a89-195">-Kind</span></span>
<span data-ttu-id="a3a89-196">Gibt die Art des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3a89-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="a3a89-197">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a3a89-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3a89-198">Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-198">Storage.</span></span> <span data-ttu-id="a3a89-199">Allgemeines Speicherkonto, das das Speichern von Blobs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="a3a89-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a3a89-200">StorageV2.</span></span> <span data-ttu-id="a3a89-201">Allgemeine Version 2 (GPv2) Speicherkonto, das Blobs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="a3a89-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="a3a89-202">BlobStorage.</span></span> <span data-ttu-id="a3a89-203">Blob Storage-Konto, das nur das Speichern von Blobs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="a3a89-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="a3a89-204">BlockBlobStorage.</span></span> <span data-ttu-id="a3a89-205">Block blob storage account which supports storage of Block Blobs only.</span><span class="sxs-lookup"><span data-stu-id="a3a89-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="a3a89-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="a3a89-206">FileStorage.</span></span> <span data-ttu-id="a3a89-207">Dateispeicherkonto, das nur das Speichern von Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a3a89-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="a3a89-208">Der Standardwert ist StorageV2.</span><span class="sxs-lookup"><span data-stu-id="a3a89-208">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-209">-Location</span><span class="sxs-lookup"><span data-stu-id="a3a89-209">-Location</span></span>
<span data-ttu-id="a3a89-210">Gibt den Speicherort des zu erstellenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-210">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a3a89-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="a3a89-212">Die mindeste TLS-Version, die für Speicheranforderungen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="a3a89-213">Die Standardinterpretation ist TLS 1.0 für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a3a89-213">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="a3a89-214">-Name</span><span class="sxs-lookup"><span data-stu-id="a3a89-214">-Name</span></span>
<span data-ttu-id="a3a89-215">Gibt den Namen des zu erstellenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="a3a89-215">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="a3a89-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a3a89-216">-NetworkRuleSet</span></span>
<span data-ttu-id="a3a89-217">NetworkRuleSet wird zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften wie Dienste verwendet, die die Regeln umgehen dürfen, und zum Behandeln von Anforderungen, die nicht mit den definierten Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a3a89-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="a3a89-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3a89-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="a3a89-219">Gibt an, ob Internetroutingspeicherendpunkte veröffentlicht werden sollen</span><span class="sxs-lookup"><span data-stu-id="a3a89-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="a3a89-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3a89-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="a3a89-221">Gibt an, ob Microsoft-Routingspeicherendpunkte veröffentlicht werden sollen</span><span class="sxs-lookup"><span data-stu-id="a3a89-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="a3a89-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="a3a89-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="a3a89-223">Der Dienst verwendet eine sekundäre Verschlüsselungsebene mit plattform verwalteten Schlüsseln für ruhende Daten.</span><span class="sxs-lookup"><span data-stu-id="a3a89-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="a3a89-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a89-224">-ResourceGroupName</span></span>
<span data-ttu-id="a3a89-225">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3a89-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="a3a89-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="a3a89-226">-RoutingChoice</span></span>
<span data-ttu-id="a3a89-227">RoutingAuswahl definiert die Art des vom Benutzer gewählten Netzwerkroutings.</span><span class="sxs-lookup"><span data-stu-id="a3a89-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="a3a89-228">Mögliche Werte sind: "MicrosoftRouting", "InternetRouting"</span><span class="sxs-lookup"><span data-stu-id="a3a89-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="a3a89-229">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a3a89-229">-SkuName</span></span>
<span data-ttu-id="a3a89-230">Gibt den SKU-Namen des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a3a89-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="a3a89-231">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a3a89-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3a89-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-232">Standard_LRS.</span></span> <span data-ttu-id="a3a89-233">Lokal redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="a3a89-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-234">Standard_ZRS.</span></span> <span data-ttu-id="a3a89-235">Zone-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="a3a89-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-236">Standard_GRS.</span></span> <span data-ttu-id="a3a89-237">Georedundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="a3a89-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-238">Standard_RAGRS.</span></span> <span data-ttu-id="a3a89-239">Lesezugriff auf georedundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="a3a89-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-240">Premium_LRS.</span></span> <span data-ttu-id="a3a89-241">Lokal redundanten Premiumspeicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="a3a89-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="a3a89-242">Premium_ZRS.</span></span> <span data-ttu-id="a3a89-243">Premium zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="a3a89-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="a3a89-244">Standard_GZRS – Georedundanter zonenredundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="a3a89-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="a3a89-245">Standard_RAGZRS – Georedundanter zonenredundanter Speicher mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="a3a89-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3a89-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3a89-246">-Tag</span></span>
<span data-ttu-id="a3a89-247">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a3a89-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="a3a89-248">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a3a89-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a3a89-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="a3a89-249">-UseSubDomain</span></span>
<span data-ttu-id="a3a89-250">Gibt an, ob die indirekte #A0 aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3a89-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="a3a89-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a89-251">CommonParameters</span></span>
<span data-ttu-id="a3a89-252">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a89-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a89-253">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a89-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a89-254">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3a89-254">INPUTS</span></span>

### <span data-ttu-id="a3a89-255">System.String</span><span class="sxs-lookup"><span data-stu-id="a3a89-255">System.String</span></span>

## <span data-ttu-id="a3a89-256">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3a89-256">OUTPUTS</span></span>

### <span data-ttu-id="a3a89-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3a89-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a3a89-258">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3a89-258">NOTES</span></span>

## <span data-ttu-id="a3a89-259">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3a89-259">RELATED LINKS</span></span>

[<span data-ttu-id="a3a89-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3a89-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="a3a89-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3a89-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="a3a89-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3a89-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
