---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c88e56a485f9e42daf229667ab4c07d7a7464578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003352"
---
# <span data-ttu-id="38fbb-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38fbb-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="38fbb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="38fbb-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-103">Creates a Storage account.</span></span>

## <span data-ttu-id="38fbb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38fbb-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38fbb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="38fbb-106">Das Cmdlet **New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="38fbb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="38fbb-108">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="38fbb-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="38fbb-109">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="38fbb-110">Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="38fbb-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="38fbb-111">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="38fbb-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="38fbb-112">Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="38fbb-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="38fbb-113">Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.</span><span class="sxs-lookup"><span data-stu-id="38fbb-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="38fbb-114">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="38fbb-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="38fbb-115">Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="38fbb-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="38fbb-116">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt</span><span class="sxs-lookup"><span data-stu-id="38fbb-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="38fbb-117">Beispiel 5: Erstellen eines speicherkontos mit aktiviertem hierarchischen Namespace</span><span class="sxs-lookup"><span data-stu-id="38fbb-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="38fbb-118">Mit diesem Befehl wird ein Speicherkonto mit aktiviertem hierarchischen Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="38fbb-119">Beispiel 6: Erstellen eines speicherkontos mit Azure-Dateien Aad DS-Authentifizierung und Aktivieren einer umfangreichen Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="38fbb-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="38fbb-120">Mit diesem Befehl wird ein Speicherkonto mit Azure-Dateien Aad DS-Authentifizierung erstellt und eine große Dateifreigabe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="38fbb-120">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share..</span></span>

### <span data-ttu-id="38fbb-121">Beispiel 8: Erstellen eines speicherkontos mit Warteschlangen-und tabellendienst verwenden Sie den Konto bezogenen Verschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="38fbb-121">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account
```

<span data-ttu-id="38fbb-122">Mit diesem Befehl wird ein Speicherkonto mit Warteschlange und tabellendienst erstellt. verwenden Sie den Konto bezogenen Verschlüsselungsschlüssel, damit Warteschlange und Tabelle denselben Verschlüsselungsschlüssel mit BLOB-und Dateidienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="38fbb-122">This command creates a Storage account with Queue and Table Service use account-scoped encryption key, so Queue and Table will use same encryption key with Blob and File service.</span></span> <span data-ttu-id="38fbb-123">Rufen Sie dann die Eigenschaften des speicherkontos ab, und zeigen Sie den Verschlüsselungs-KeyType der Warteschlange und des Tabellen Diensts an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-123">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service.</span></span>

## <span data-ttu-id="38fbb-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="38fbb-124">PARAMETERS</span></span>

### <span data-ttu-id="38fbb-125">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="38fbb-125">-AccessTier</span></span>
<span data-ttu-id="38fbb-126">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-126">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="38fbb-127">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="38fbb-127">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="38fbb-128">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="38fbb-128">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="38fbb-129">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-129">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="38fbb-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38fbb-130">-AsJob</span></span>
<span data-ttu-id="38fbb-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="38fbb-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38fbb-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="38fbb-132">-AssignIdentity</span></span>
<span data-ttu-id="38fbb-133">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="38fbb-133">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="38fbb-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="38fbb-134">-CustomDomainName</span></span>
<span data-ttu-id="38fbb-135">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-135">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="38fbb-136">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="38fbb-136">The default value is Storage.</span></span>

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

### <span data-ttu-id="38fbb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fbb-137">-DefaultProfile</span></span>
<span data-ttu-id="38fbb-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38fbb-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38fbb-139">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="38fbb-139">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="38fbb-140">Aktivieren Sie Azure-Dateien Azure Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-140">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="38fbb-141">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="38fbb-141">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="38fbb-142">Gibt an, ob das Speicherkonto den hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="38fbb-142">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="38fbb-143">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="38fbb-143">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="38fbb-144">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="38fbb-144">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="38fbb-145">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="38fbb-145">-EnableLargeFileShare</span></span>
<span data-ttu-id="38fbb-146">Gibt an, ob das Speicherkonto große Dateifreigaben mit mehr als 5 tib-Kapazität unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="38fbb-146">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="38fbb-147">Sobald das Konto aktiviert ist, kann das Feature nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="38fbb-147">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="38fbb-148">Wird derzeit nur für LRS-und ZRS-Replikationstypen unterstützt, daher sind Konto Konvertierungen in Geo-redundante Konten nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="38fbb-148">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="38fbb-149">Weitere Informationen finden Sie unter https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="38fbb-149">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="38fbb-150">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="38fbb-150">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="38fbb-151">Stellen Sie den Verschlüsselungs-KeyType für Queue ein.</span><span class="sxs-lookup"><span data-stu-id="38fbb-151">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="38fbb-152">Der Standardwert ist Service.</span><span class="sxs-lookup"><span data-stu-id="38fbb-152">The default value is Service.</span></span>
<span data-ttu-id="38fbb-153">-Konto: die Warteschlange wird mit dem Konto bezogenen Verschlüsselungsschlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-153">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="38fbb-154">-Service: Queue wird immer mit Service-Managed Schlüsseln verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-154">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="38fbb-155">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="38fbb-155">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="38fbb-156">Setzen Sie den Verschlüsselungs-KeyType für Table.</span><span class="sxs-lookup"><span data-stu-id="38fbb-156">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="38fbb-157">Der Standardwert ist Service.</span><span class="sxs-lookup"><span data-stu-id="38fbb-157">The default value is Service.</span></span>
- <span data-ttu-id="38fbb-158">Konto: die Tabelle wird mit dem Konto bezogenen Verschlüsselungsschlüssel verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-158">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="38fbb-159">Dienst: die Tabelle wird immer mit Service-Managed Schlüsseln verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-159">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="38fbb-160">-Art</span><span class="sxs-lookup"><span data-stu-id="38fbb-160">-Kind</span></span>
<span data-ttu-id="38fbb-161">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-161">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="38fbb-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="38fbb-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38fbb-163">Speicher.</span><span class="sxs-lookup"><span data-stu-id="38fbb-163">Storage.</span></span> <span data-ttu-id="38fbb-164">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-164">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="38fbb-165">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="38fbb-165">StorageV2.</span></span> <span data-ttu-id="38fbb-166">GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-166">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="38fbb-167">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="38fbb-167">BlobStorage.</span></span> <span data-ttu-id="38fbb-168">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-168">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="38fbb-169">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="38fbb-169">BlockBlobStorage.</span></span> <span data-ttu-id="38fbb-170">Blockieren des BLOB-speicherkontos, das nur die Speicherung von BLOB-Blöcken unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-170">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="38fbb-171">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="38fbb-171">FileStorage.</span></span> <span data-ttu-id="38fbb-172">Dateispeicher Konto, das nur die Speicherung von Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-172">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="38fbb-173">Der Standardwert ist StorageV2.</span><span class="sxs-lookup"><span data-stu-id="38fbb-173">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38fbb-174">-Standort</span><span class="sxs-lookup"><span data-stu-id="38fbb-174">-Location</span></span>
<span data-ttu-id="38fbb-175">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-175">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="38fbb-176">-Name</span><span class="sxs-lookup"><span data-stu-id="38fbb-176">-Name</span></span>
<span data-ttu-id="38fbb-177">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="38fbb-177">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="38fbb-178">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="38fbb-178">-NetworkRuleSet</span></span>
<span data-ttu-id="38fbb-179">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="38fbb-179">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="38fbb-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fbb-180">-ResourceGroupName</span></span>
<span data-ttu-id="38fbb-181">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38fbb-181">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="38fbb-182">-SkuName</span><span class="sxs-lookup"><span data-stu-id="38fbb-182">-SkuName</span></span>
<span data-ttu-id="38fbb-183">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="38fbb-183">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="38fbb-184">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="38fbb-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38fbb-185">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-185">Standard_LRS.</span></span> <span data-ttu-id="38fbb-186">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="38fbb-186">Locally-redundant storage.</span></span>
- <span data-ttu-id="38fbb-187">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-187">Standard_ZRS.</span></span> <span data-ttu-id="38fbb-188">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="38fbb-188">Zone-redundant storage.</span></span>
- <span data-ttu-id="38fbb-189">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-189">Standard_GRS.</span></span> <span data-ttu-id="38fbb-190">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="38fbb-190">Geo-redundant storage.</span></span>
- <span data-ttu-id="38fbb-191">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-191">Standard_RAGRS.</span></span> <span data-ttu-id="38fbb-192">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="38fbb-192">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="38fbb-193">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-193">Premium_LRS.</span></span> <span data-ttu-id="38fbb-194">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="38fbb-194">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="38fbb-195">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="38fbb-195">Premium_ZRS.</span></span> <span data-ttu-id="38fbb-196">Premium Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="38fbb-196">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="38fbb-197">Standard_GZRS-Geo-redundante Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="38fbb-197">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="38fbb-198">Standard_RAGZRS-Read Access Geo-redundant Zone-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="38fbb-198">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="38fbb-199">-Tag</span><span class="sxs-lookup"><span data-stu-id="38fbb-199">-Tag</span></span>
<span data-ttu-id="38fbb-200">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="38fbb-200">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="38fbb-201">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="38fbb-201">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="38fbb-202">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="38fbb-202">-UseSubDomain</span></span>
<span data-ttu-id="38fbb-203">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="38fbb-203">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="38fbb-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fbb-204">CommonParameters</span></span>
<span data-ttu-id="38fbb-205">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fbb-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fbb-206">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38fbb-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fbb-207">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38fbb-207">INPUTS</span></span>

### <span data-ttu-id="38fbb-208">System. String</span><span class="sxs-lookup"><span data-stu-id="38fbb-208">System.String</span></span>

## <span data-ttu-id="38fbb-209">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38fbb-209">OUTPUTS</span></span>

### <span data-ttu-id="38fbb-210">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38fbb-210">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="38fbb-211">Notizen</span><span class="sxs-lookup"><span data-stu-id="38fbb-211">NOTES</span></span>

## <span data-ttu-id="38fbb-212">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38fbb-212">RELATED LINKS</span></span>

[<span data-ttu-id="38fbb-213">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38fbb-213">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="38fbb-214">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38fbb-214">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="38fbb-215">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38fbb-215">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
