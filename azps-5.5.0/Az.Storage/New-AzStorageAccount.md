---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163004"
---
# <span data-ttu-id="8a790-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a790-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="8a790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a790-102">SYNOPSIS</span></span>
<span data-ttu-id="8a790-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="8a790-103">Creates a Storage account.</span></span>

## <span data-ttu-id="8a790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a790-104">SYNTAX</span></span>

### <span data-ttu-id="8a790-105">AzureActiveDirectoryDomainServicesForFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a790-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="8a790-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="8a790-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a790-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a790-107">DESCRIPTION</span></span>
<span data-ttu-id="8a790-108">Das **Cmdlet "New-AzStorageAccount"** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="8a790-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="8a790-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a790-109">EXAMPLES</span></span>

### <span data-ttu-id="8a790-110">Beispiel 1: Erstellen eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8a790-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="8a790-111">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen "MyResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a790-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="8a790-112">Beispiel 2: Erstellen eines Blob Storage-Kontos mit BlobStorage Kind und hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="8a790-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="8a790-113">Mit diesem Befehl wird ein Blob Storage-Konto erstellt, das blobStorage Kind und hot AccessTier verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a790-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="8a790-114">Beispiel 3: Erstellen Sie ein Speicherkonto mit Kind StorageV2, und generieren und weisen Sie eine Identität für Azure KeyVault zu.</span><span class="sxs-lookup"><span data-stu-id="8a790-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="8a790-115">Mit diesem Befehl wird ein Speicherkonto mit Kind StorageV2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a790-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="8a790-116">Außerdem wird eine Identität generiert und zugewiesen, die zum Verwalten von Kontoschlüsseln über Azure KeyVault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a790-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="8a790-117">Beispiel 4: Erstellen eines Speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="8a790-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="8a790-118">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die Eigenschaft "NetworkRuleSet" von JSON verfügt.</span><span class="sxs-lookup"><span data-stu-id="8a790-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="8a790-119">Beispiel 5: Erstellen eines Speicherkontos mit aktivierten hierarchischem Namespace</span><span class="sxs-lookup"><span data-stu-id="8a790-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="8a790-120">Mit diesem Befehl wird ein Speicherkonto mit aktivierten hierarchischem Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="8a790-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="8a790-121">Beispiel 6: Erstellen Sie ein Speicherkonto mit Azure Files AAD DS Authentication, und aktivieren Sie die große Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="8a790-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="8a790-122">Mit diesem Befehl wird ein Speicherkonto mit Azure Files AAD DS Authentication erstellt und große Dateifreigaben aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a790-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="8a790-123">Beispiel 7: Erstellen eines Speicherkontos mit aktivierter Active Directory-Domänendienstauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="8a790-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="8a790-124">Mit diesem Befehl wird ein Speicherkonto erstellt, für das die Active Directory-Domänendienstauthentifizierung aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a790-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="8a790-125">Beispiel 8: Erstellen eines Speicherkontos mit "Warteschlange" und "Tabellendienst" verwenden den Verschlüsselungsschlüssel mit Kontobereich und "Infrastrukturverschlüsselung erforderlich".</span><span class="sxs-lookup"><span data-stu-id="8a790-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="8a790-126">Dieser Befehl erstellt ein Speicherkonto mit Verschlüsselungsschlüssel mit Kontobereich und Tabellendienst und erfordert Infrastrukturverschlüsselung. Warteschlange und Tabelle verwenden also denselben Verschlüsselungsschlüssel mit blob- und file-Dienst, und der Dienst wenden eine sekundäre Verschlüsselungsebene mit plattformver verwalteten Schlüsseln für ruhede Daten an.</span><span class="sxs-lookup"><span data-stu-id="8a790-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="8a790-127">Holen Sie sich dann die Eigenschaften des Speicherkontos, zeigen Sie den Verschlüsselungsschlüsseltyp von Warteschlangen- und Tabellendienst sowie den Wert der Kryption "RequireInfrastructureEncryption" an.</span><span class="sxs-lookup"><span data-stu-id="8a790-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="8a790-128">Beispiel 9: Erstellen des Kontos "MinimumTlsVersion" und "AllowBlobPublicAccess"</span><span class="sxs-lookup"><span data-stu-id="8a790-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="8a790-129">Der Befehl "Konto erstellen" mit "MinimumTlsVersion" und "AllowBlobPublicAccess" und zeigt dann die zwei Eigenschaften des erstellten Kontos an.</span><span class="sxs-lookup"><span data-stu-id="8a790-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

### <span data-ttu-id="8a790-130">Beispiel 10: Erstellen eines Speicherkontos mit Einstellung "RoutingPreference"</span><span class="sxs-lookup"><span data-stu-id="8a790-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
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

<span data-ttu-id="8a790-131">Mit diesem Befehl wird ein Speicherkonto mit der Einstellung "RoutingPreference" erstellt: "PublishMicrosoftEndpoint" und "PublishInternetEndpoint" als "true" und "RoutingChoice" als "MicrosoftRouting".</span><span class="sxs-lookup"><span data-stu-id="8a790-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="8a790-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a790-132">PARAMETERS</span></span>

### <span data-ttu-id="8a790-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="8a790-133">-AccessTier</span></span>
<span data-ttu-id="8a790-134">Gibt die Zugriffsebene des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a790-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8a790-135">Die zulässigen Werte für diesen Parameter sind: "Hot" und "Cool".</span><span class="sxs-lookup"><span data-stu-id="8a790-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="8a790-136">Wenn Sie einen Wert von BlobStorage für den Parameter *"Kind"* angeben, müssen Sie einen Wert für den *Parameter "AccessTier"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8a790-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="8a790-137">Wenn Sie einen Wert von "Storage" für diesen *Parameter "Kind"* angeben, geben Sie nicht den *"AccessTier"-Parameter* an.</span><span class="sxs-lookup"><span data-stu-id="8a790-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="8a790-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="8a790-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="8a790-139">Gibt die Sicherheits-ID (SID) für Azure Storage an.</span><span class="sxs-lookup"><span data-stu-id="8a790-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="8a790-140">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="8a790-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="8a790-142">Gibt die Domänen-GUID an.</span><span class="sxs-lookup"><span data-stu-id="8a790-142">Specifies the domain GUID.</span></span> <span data-ttu-id="8a790-143">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="8a790-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="8a790-145">Gibt die primäre Domäne an, für die der AD -DNS-Server autoritativ ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="8a790-146">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="8a790-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="8a790-148">Gibt die Sicherheits-ID (SID) an.</span><span class="sxs-lookup"><span data-stu-id="8a790-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="8a790-149">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="8a790-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="8a790-151">Gibt die active Directory-Gesamtstruktur an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="8a790-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="8a790-152">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-153">-ActiveDirectoryNetDomäneName</span><span class="sxs-lookup"><span data-stu-id="8a790-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="8a790-154">Gibt den Domänennamen von NetERGEBNISS an.</span><span class="sxs-lookup"><span data-stu-id="8a790-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="8a790-155">Dieser Parameter muss festgelegt werden, wenn "-EnableActiveDirectoryDomainServicesForFile" auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="8a790-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="8a790-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="8a790-157">Lassen Sie den öffentlichen Zugriff auf alle BLOBS oder Container im Speicherkonto zu.</span><span class="sxs-lookup"><span data-stu-id="8a790-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="8a790-158">Die Standarddeutung gilt für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8a790-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="8a790-159">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a790-159">-AsJob</span></span>
<span data-ttu-id="8a790-160">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8a790-160">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a790-161">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8a790-161">-AssignIdentity</span></span>
<span data-ttu-id="8a790-162">Generieren und zuweisen Sie eine neue Speicherkontoidentität für dieses Speicherkonto zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8a790-162">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8a790-163">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="8a790-163">-CustomDomainName</span></span>
<span data-ttu-id="8a790-164">Gibt den Namen der benutzerdefinierten Domäne des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="8a790-164">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="8a790-165">Der Standardwert ist "Storage".</span><span class="sxs-lookup"><span data-stu-id="8a790-165">The default value is Storage.</span></span>

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

### <span data-ttu-id="8a790-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a790-166">-DefaultProfile</span></span>
<span data-ttu-id="8a790-167">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a790-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a790-168">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="8a790-168">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="8a790-169">Aktivieren Sie azure files Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="8a790-169">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="8a790-170">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="8a790-170">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="8a790-171">Aktivieren Sie Azure Files Azure Active Directory Domain Service Authentication für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="8a790-171">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="8a790-172">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="8a790-172">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="8a790-173">Gibt an, ob das Konto "Storage" den hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a790-173">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="8a790-174">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="8a790-174">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="8a790-175">Gibt an, ob das Speicherkonto nur den HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8a790-175">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="8a790-176">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="8a790-176">-EnableLargeFileShare</span></span>
<span data-ttu-id="8a790-177">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 TiB-Kapazität unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="8a790-177">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="8a790-178">Sobald das Konto aktiviert ist, kann das Feature nicht mehr deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="8a790-178">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="8a790-179">Derzeit nur für LRS- und ZRS-Replikationstypen unterstützt, daher sind Kontokonvertierungen in georedundanter Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="8a790-179">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="8a790-180">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="8a790-180">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="8a790-181">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="8a790-181">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="8a790-182">Legen Sie den Verschlüsselungsschlüsseltyp für die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="8a790-182">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="8a790-183">Der Standardwert ist "Dienst".</span><span class="sxs-lookup"><span data-stu-id="8a790-183">The default value is Service.</span></span>
<span data-ttu-id="8a790-184">-Konto: Die Warteschlange wird mit dem Verschlüsselungsschlüssel mit Kontobereich verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8a790-184">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="8a790-185">-Dienst: Die Warteschlange wird immer mit Service-Managed verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8a790-185">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="8a790-186">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="8a790-186">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="8a790-187">Legen Sie den Verschlüsselungsschlüsseltyp für "Table" ein.</span><span class="sxs-lookup"><span data-stu-id="8a790-187">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="8a790-188">Der Standardwert ist "Dienst".</span><span class="sxs-lookup"><span data-stu-id="8a790-188">The default value is Service.</span></span>
- <span data-ttu-id="8a790-189">Konto: Die Tabelle wird mit dem Verschlüsselungsschlüssel mit Kontobereich verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8a790-189">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="8a790-190">Dienst: Die Tabelle wird immer mit Service-Managed verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="8a790-190">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="8a790-191">-Kind</span><span class="sxs-lookup"><span data-stu-id="8a790-191">-Kind</span></span>
<span data-ttu-id="8a790-192">Gibt die Art des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a790-192">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8a790-193">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8a790-193">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a790-194">Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a790-194">Storage.</span></span> <span data-ttu-id="8a790-195">Allgemeines Speicherkonto, das die Speicherung von Blobs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8a790-195">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="8a790-196">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="8a790-196">StorageV2.</span></span> <span data-ttu-id="8a790-197">Allgemeine Version 2 (GPv2) Speicherkonto, das Blobs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Daten tiering unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8a790-197">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="8a790-198">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="8a790-198">BlobStorage.</span></span> <span data-ttu-id="8a790-199">Blob Storage account which supports storage of Blobs only.</span><span class="sxs-lookup"><span data-stu-id="8a790-199">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="8a790-200">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="8a790-200">BlockBlobStorage.</span></span> <span data-ttu-id="8a790-201">Block Blob Storage account which supports storage of Block Blobs only.</span><span class="sxs-lookup"><span data-stu-id="8a790-201">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="8a790-202">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="8a790-202">FileStorage.</span></span> <span data-ttu-id="8a790-203">Dateispeicherkonto, das nur das Speichern von Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8a790-203">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="8a790-204">Der Standardwert ist "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="8a790-204">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="8a790-205">-Location</span><span class="sxs-lookup"><span data-stu-id="8a790-205">-Location</span></span>
<span data-ttu-id="8a790-206">Gibt den Speicherort des zu erstellenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="8a790-206">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="8a790-207">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8a790-207">-MinimumTlsVersion</span></span>
<span data-ttu-id="8a790-208">Die mindestens zulässige TLS-Version für Speicheranforderungen.</span><span class="sxs-lookup"><span data-stu-id="8a790-208">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="8a790-209">Die Standarddeutung für diese Eigenschaft ist TLS 1.0.</span><span class="sxs-lookup"><span data-stu-id="8a790-209">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="8a790-210">-Name</span><span class="sxs-lookup"><span data-stu-id="8a790-210">-Name</span></span>
<span data-ttu-id="8a790-211">Gibt den Namen des Speicherkontos an, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a790-211">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="8a790-212">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8a790-212">-NetworkRuleSet</span></span>
<span data-ttu-id="8a790-213">NetworkRuleSet dient zum Definieren einer Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke sowie zum Festlegen von Werten für Netzwerkeigenschaften wie Dienste, die die Regeln umgehen dürfen, und zum Behandeln von Anforderungen, die keine der definierten Regeln erfüllen.</span><span class="sxs-lookup"><span data-stu-id="8a790-213">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="8a790-214">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a790-214">-PublishInternetEndpoint</span></span>
<span data-ttu-id="8a790-215">Gibt an, ob Internetroutingspeicherendpunkte veröffentlicht werden sollen</span><span class="sxs-lookup"><span data-stu-id="8a790-215">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="8a790-216">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="8a790-216">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="8a790-217">Gibt an, ob Microsoft-Routing-Speicherendpunkte veröffentlicht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8a790-217">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="8a790-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a790-218">-ResourceGroupName</span></span>
<span data-ttu-id="8a790-219">Gibt den Namen der Ressourcengruppe an, der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a790-219">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="8a790-220">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="8a790-220">-RoutingChoice</span></span>
<span data-ttu-id="8a790-221">Die Routingauswahl definiert die Art des vom Benutzer gewählten Netzwerkroutings.</span><span class="sxs-lookup"><span data-stu-id="8a790-221">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="8a790-222">Mögliche Werte sind: "MicrosoftRouting", "InternetRouting".</span><span class="sxs-lookup"><span data-stu-id="8a790-222">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="8a790-223">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8a790-223">-SkuName</span></span>
<span data-ttu-id="8a790-224">Gibt den Namen der SKU des Speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a790-224">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="8a790-225">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="8a790-225">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8a790-226">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-226">Standard_LRS.</span></span> <span data-ttu-id="8a790-227">Lokal redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a790-227">Locally-redundant storage.</span></span>
- <span data-ttu-id="8a790-228">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-228">Standard_ZRS.</span></span> <span data-ttu-id="8a790-229">Zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="8a790-229">Zone-redundant storage.</span></span>
- <span data-ttu-id="8a790-230">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-230">Standard_GRS.</span></span> <span data-ttu-id="8a790-231">Georedundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a790-231">Geo-redundant storage.</span></span>
- <span data-ttu-id="8a790-232">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-232">Standard_RAGRS.</span></span> <span data-ttu-id="8a790-233">Georedundanter Speicher mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="8a790-233">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="8a790-234">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-234">Premium_LRS.</span></span> <span data-ttu-id="8a790-235">Premium für lokal redundanten Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a790-235">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="8a790-236">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="8a790-236">Premium_ZRS.</span></span> <span data-ttu-id="8a790-237">Premium zone-redundant storage.</span><span class="sxs-lookup"><span data-stu-id="8a790-237">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="8a790-238">Standard_GZRS – Georedundanter zonenredundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="8a790-238">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="8a790-239">Standard_RAGZRS – Georedundanter zonenredundanter Speicher mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="8a790-239">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="8a790-240">-Tag</span><span class="sxs-lookup"><span data-stu-id="8a790-240">-Tag</span></span>
<span data-ttu-id="8a790-241">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8a790-241">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="8a790-242">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8a790-242">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8a790-243">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="8a790-243">-UseSubDomain</span></span>
<span data-ttu-id="8a790-244">Gibt an, ob die indirekte #A0 aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a790-244">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="8a790-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a790-245">CommonParameters</span></span>
<span data-ttu-id="8a790-246">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a790-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a790-247">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a790-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a790-248">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a790-248">INPUTS</span></span>

### <span data-ttu-id="8a790-249">System.String</span><span class="sxs-lookup"><span data-stu-id="8a790-249">System.String</span></span>

## <span data-ttu-id="8a790-250">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a790-250">OUTPUTS</span></span>

### <span data-ttu-id="8a790-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a790-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="8a790-252">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8a790-252">NOTES</span></span>

## <span data-ttu-id="8a790-253">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8a790-253">RELATED LINKS</span></span>

[<span data-ttu-id="8a790-254">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a790-254">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="8a790-255">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a790-255">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="8a790-256">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a790-256">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
