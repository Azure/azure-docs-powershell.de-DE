---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177395"
---
# <span data-ttu-id="ec537-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec537-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="ec537-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec537-102">SYNOPSIS</span></span>
<span data-ttu-id="ec537-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="ec537-103">Creates a Storage account.</span></span>

## <span data-ttu-id="ec537-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec537-104">SYNTAX</span></span>

### <span data-ttu-id="ec537-105">AzureActiveDirectoryDomainServicesForFile (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec537-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec537-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ec537-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec537-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec537-107">DESCRIPTION</span></span>
<span data-ttu-id="ec537-108">Das Cmdlet **New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="ec537-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="ec537-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec537-109">EXAMPLES</span></span>

### <span data-ttu-id="ec537-110">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="ec537-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="ec537-111">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec537-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="ec537-112">Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="ec537-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="ec537-113">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="ec537-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="ec537-114">Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="ec537-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="ec537-115">Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ec537-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="ec537-116">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec537-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="ec537-117">Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="ec537-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="ec537-118">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt</span><span class="sxs-lookup"><span data-stu-id="ec537-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="ec537-119">Beispiel 5: Erstellen eines speicherkontos mit aktiviertem hierarchischen Namespace</span><span class="sxs-lookup"><span data-stu-id="ec537-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="ec537-120">Mit diesem Befehl wird ein Speicherkonto mit aktiviertem hierarchischen Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec537-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="ec537-121">Beispiel 6: Erstellen eines speicherkontos mit Azure-Dateien Aad DS-Authentifizierung und Aktivieren einer umfangreichen Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="ec537-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="ec537-122">Mit diesem Befehl wird ein Speicherkonto mit Azure-Dateien Aad DS-Authentifizierung erstellt und eine große Dateifreigabe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec537-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="ec537-123">Beispiel 7: Erstellen eines speicherkontos mit enable files Active Directory-Domänendienst Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ec537-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="ec537-124">Mit diesem Befehl wird ein Speicherkonto withenable Dateien Active Directory-Domänendienst Authentifizierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec537-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="ec537-125">Beispiel 8: Erstellen eines speicherkontos mit Warteschlangen-und tabellendienst verwenden Sie den Konto bezogenen Verschlüsselungsschlüssel, und fordern Sie eine Infrastruktur Verschlüsselung an.</span><span class="sxs-lookup"><span data-stu-id="ec537-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="ec537-126">Mit diesem Befehl wird ein Speicherkonto mit Warteschlangen-und tabellendienst erstellt. verwenden Sie den Konto bezogenen Verschlüsselungsschlüssel, und fordern Sie eine Infrastruktur Verschlüsselung an, damit Warteschlange und Tabelle denselben Verschlüsselungsschlüssel für BLOB-und Dateidienste verwenden, und der Dienst eine sekundäre Verschlüsselungsebene mit Platt Form verwalteten Schlüsseln für Daten in Ruhe anwendet.</span><span class="sxs-lookup"><span data-stu-id="ec537-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="ec537-127">Rufen Sie dann die Eigenschaften des speicherkontos ab, und zeigen Sie den Verschlüsselungs-KeyType der Warteschlange und des Tabellen Diensts sowie den RequireInfrastructureEncryption-Wert an.</span><span class="sxs-lookup"><span data-stu-id="ec537-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="ec537-128">Beispiel 9: Erstellen von Konto MinimumTlsVersion und AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="ec537-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="ec537-129">Der Befehl Konto mit MinimumTlsVersion und AllowBlobPublicAccess erstellen und dann die 2 Eigenschaften des erstellten Kontos anzeigen</span><span class="sxs-lookup"><span data-stu-id="ec537-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="ec537-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec537-130">PARAMETERS</span></span>

### <span data-ttu-id="ec537-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ec537-131">-AccessTier</span></span>
<span data-ttu-id="ec537-132">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ec537-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ec537-133">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="ec537-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="ec537-134">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="ec537-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="ec537-135">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="ec537-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="ec537-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="ec537-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="ec537-137">Gibt die Sicherheits-ID (Security Identifier, SID) für Azure Storage an.</span><span class="sxs-lookup"><span data-stu-id="ec537-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="ec537-138">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="ec537-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="ec537-140">Gibt die GUID der Domäne an.</span><span class="sxs-lookup"><span data-stu-id="ec537-140">Specifies the domain GUID.</span></span> <span data-ttu-id="ec537-141">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="ec537-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="ec537-143">Gibt die primäre Domäne an, für die der AD-DNS-Server autorisierend ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="ec537-144">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="ec537-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="ec537-146">Gibt die Sicherheits-ID (Security Identifier, SID) an.</span><span class="sxs-lookup"><span data-stu-id="ec537-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="ec537-147">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="ec537-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="ec537-149">Gibt die Active Directory-Gesamtstruktur an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec537-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="ec537-150">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="ec537-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="ec537-152">Gibt den NetBIOS-Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="ec537-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="ec537-153">Dieser Parameter muss festgelegt werden, wenn-EnableActiveDirectoryDomainServicesForFile auf "true" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="ec537-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="ec537-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="ec537-155">Gewähren des öffentlichen Zugriffs auf alle Blobs oder Container im Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="ec537-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="ec537-156">Die Standardinterpretation für diese Eigenschaft ist wahr.</span><span class="sxs-lookup"><span data-stu-id="ec537-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="ec537-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec537-157">-AsJob</span></span>
<span data-ttu-id="ec537-158">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ec537-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec537-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ec537-159">-AssignIdentity</span></span>
<span data-ttu-id="ec537-160">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="ec537-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec537-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ec537-161">-CustomDomainName</span></span>
<span data-ttu-id="ec537-162">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ec537-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="ec537-163">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="ec537-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="ec537-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec537-164">-DefaultProfile</span></span>
<span data-ttu-id="ec537-165">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec537-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec537-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ec537-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="ec537-167">Aktivieren von Azure-Dateien Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="ec537-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="ec537-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="ec537-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="ec537-169">Aktivieren Sie Azure-Dateien Azure Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="ec537-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="ec537-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="ec537-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="ec537-171">Gibt an, ob das Speicherkonto den hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec537-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="ec537-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="ec537-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="ec537-173">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ec537-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="ec537-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="ec537-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="ec537-175">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 tib-Kapazität unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="ec537-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="ec537-176">Sobald das Konto aktiviert ist, kann das Feature nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ec537-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="ec537-177">Wird derzeit nur für LRS-und ZRS-Replikationstypen unterstützt, daher sind Konto Konvertierungen in Geo-redundante Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ec537-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="ec537-178">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="ec537-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="ec537-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="ec537-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="ec537-180">Stellen Sie den Verschlüsselungs-KeyType für Queue ein.</span><span class="sxs-lookup"><span data-stu-id="ec537-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="ec537-181">Der Standardwert ist Service.</span><span class="sxs-lookup"><span data-stu-id="ec537-181">The default value is Service.</span></span>
<span data-ttu-id="ec537-182">-Konto: die Warteschlange wird mit dem Konto bezogenen Verschlüsselungsschlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="ec537-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="ec537-183">-Service: Queue wird immer mit Service-Managed Schlüsseln verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="ec537-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="ec537-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="ec537-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="ec537-185">Setzen Sie den Verschlüsselungs-KeyType für Table.</span><span class="sxs-lookup"><span data-stu-id="ec537-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="ec537-186">Der Standardwert ist Service.</span><span class="sxs-lookup"><span data-stu-id="ec537-186">The default value is Service.</span></span>
- <span data-ttu-id="ec537-187">Konto: die Tabelle wird mit dem Konto bezogenen Verschlüsselungsschlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="ec537-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="ec537-188">Dienst: die Tabelle wird immer mit Service-Managed Schlüsseln verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="ec537-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="ec537-189">-Art</span><span class="sxs-lookup"><span data-stu-id="ec537-189">-Kind</span></span>
<span data-ttu-id="ec537-190">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ec537-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ec537-191">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ec537-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec537-192">Speicher.</span><span class="sxs-lookup"><span data-stu-id="ec537-192">Storage.</span></span> <span data-ttu-id="ec537-193">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec537-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="ec537-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ec537-194">StorageV2.</span></span> <span data-ttu-id="ec537-195">GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec537-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="ec537-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="ec537-196">BlobStorage.</span></span> <span data-ttu-id="ec537-197">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec537-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="ec537-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="ec537-198">BlockBlobStorage.</span></span> <span data-ttu-id="ec537-199">Blockieren des BLOB-speicherkontos, das nur die Speicherung von BLOB-Blöcken unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec537-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="ec537-200">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="ec537-200">FileStorage.</span></span> <span data-ttu-id="ec537-201">Dateispeicher Konto, das nur die Speicherung von Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec537-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="ec537-202">Der Standardwert ist StorageV2.</span><span class="sxs-lookup"><span data-stu-id="ec537-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="ec537-203">-Standort</span><span class="sxs-lookup"><span data-stu-id="ec537-203">-Location</span></span>
<span data-ttu-id="ec537-204">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ec537-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="ec537-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ec537-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="ec537-206">Die minimale TLS-Version, die bei Speicheranforderungen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="ec537-207">Die Standardinterpretation ist TLS 1,0 für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ec537-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="ec537-208">-Name</span><span class="sxs-lookup"><span data-stu-id="ec537-208">-Name</span></span>
<span data-ttu-id="ec537-209">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="ec537-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="ec537-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ec537-210">-NetworkRuleSet</span></span>
<span data-ttu-id="ec537-211">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ec537-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="ec537-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="ec537-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="ec537-213">Der Dienst wendet eine sekundäre Verschlüsselungsebene mit Platt Form verwalteten Schlüsseln für ruhende Daten an.</span><span class="sxs-lookup"><span data-stu-id="ec537-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="ec537-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec537-214">-ResourceGroupName</span></span>
<span data-ttu-id="ec537-215">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec537-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="ec537-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ec537-216">-SkuName</span></span>
<span data-ttu-id="ec537-217">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec537-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="ec537-218">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ec537-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec537-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-219">Standard_LRS.</span></span> <span data-ttu-id="ec537-220">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ec537-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="ec537-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-221">Standard_ZRS.</span></span> <span data-ttu-id="ec537-222">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="ec537-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="ec537-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-223">Standard_GRS.</span></span> <span data-ttu-id="ec537-224">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="ec537-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="ec537-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-225">Standard_RAGRS.</span></span> <span data-ttu-id="ec537-226">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="ec537-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="ec537-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-227">Premium_LRS.</span></span> <span data-ttu-id="ec537-228">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ec537-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="ec537-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="ec537-229">Premium_ZRS.</span></span> <span data-ttu-id="ec537-230">Premium Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ec537-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="ec537-231">Standard_GZRS-Geo-redundante Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="ec537-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="ec537-232">Standard_RAGZRS-Read Access Geo-redundant Zone-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="ec537-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="ec537-233">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec537-233">-Tag</span></span>
<span data-ttu-id="ec537-234">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ec537-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ec537-235">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ec537-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec537-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="ec537-236">-UseSubDomain</span></span>
<span data-ttu-id="ec537-237">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec537-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="ec537-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec537-238">CommonParameters</span></span>
<span data-ttu-id="ec537-239">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec537-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec537-240">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec537-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec537-241">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec537-241">INPUTS</span></span>

### <span data-ttu-id="ec537-242">System. String</span><span class="sxs-lookup"><span data-stu-id="ec537-242">System.String</span></span>

## <span data-ttu-id="ec537-243">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec537-243">OUTPUTS</span></span>

### <span data-ttu-id="ec537-244">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec537-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ec537-245">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec537-245">NOTES</span></span>

## <span data-ttu-id="ec537-246">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec537-246">RELATED LINKS</span></span>

[<span data-ttu-id="ec537-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec537-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="ec537-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec537-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="ec537-249">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ec537-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
