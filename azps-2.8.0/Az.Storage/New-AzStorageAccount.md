---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c8ac7139c44adc8bd748eef9a6c762a71c3a777f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826696"
---
# <span data-ttu-id="bfe2e-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfe2e-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="bfe2e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bfe2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe2e-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-103">Creates a Storage account.</span></span>

## <span data-ttu-id="bfe2e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfe2e-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfe2e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bfe2e-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe2e-106">Das Cmdlet **New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="bfe2e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfe2e-107">EXAMPLES</span></span>

### <span data-ttu-id="bfe2e-108">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bfe2e-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="bfe2e-109">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="bfe2e-110">Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="bfe2e-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="bfe2e-111">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="bfe2e-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="bfe2e-112">Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="bfe2e-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="bfe2e-113">Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="bfe2e-114">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="bfe2e-115">Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="bfe2e-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="bfe2e-116">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt</span><span class="sxs-lookup"><span data-stu-id="bfe2e-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="bfe2e-117">Beispiel 5: Erstellen eines speicherkontos mit aktiviertem hierarchischen Namespace</span><span class="sxs-lookup"><span data-stu-id="bfe2e-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="bfe2e-118">Mit diesem Befehl wird ein Speicherkonto mit aktiviertem hierarchischen Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="bfe2e-119">Beispiel 6: Erstellen eines speicherkontos mit Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="bfe2e-120">Dieser Befehl erstellt ein Speicherkonto mit Azure-Dateien Aad DS-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-120">This command creates a Storage account with Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="bfe2e-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfe2e-121">PARAMETERS</span></span>

### <span data-ttu-id="bfe2e-122">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="bfe2e-122">-AccessTier</span></span>
<span data-ttu-id="bfe2e-123">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-123">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="bfe2e-124">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-124">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="bfe2e-125">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-125">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="bfe2e-126">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-126">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="bfe2e-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfe2e-127">-AsJob</span></span>
<span data-ttu-id="bfe2e-128">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bfe2e-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bfe2e-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bfe2e-129">-AssignIdentity</span></span>
<span data-ttu-id="bfe2e-130">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="bfe2e-130">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="bfe2e-131">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bfe2e-131">-CustomDomainName</span></span>
<span data-ttu-id="bfe2e-132">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-132">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="bfe2e-133">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-133">The default value is Storage.</span></span>

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

### <span data-ttu-id="bfe2e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe2e-134">-DefaultProfile</span></span>
<span data-ttu-id="bfe2e-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfe2e-136">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bfe2e-136">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="bfe2e-137">Aktivieren Sie Azure-Dateien Azure Active Directory-Domänendienst Authentifizierung für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-137">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="bfe2e-138">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="bfe2e-138">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="bfe2e-139">Gibt an, ob das Speicherkonto den hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-139">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="bfe2e-140">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="bfe2e-140">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="bfe2e-141">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-141">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="bfe2e-142">-Art</span><span class="sxs-lookup"><span data-stu-id="bfe2e-142">-Kind</span></span>
<span data-ttu-id="bfe2e-143">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-143">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="bfe2e-144">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bfe2e-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bfe2e-145">Speicher.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-145">Storage.</span></span> <span data-ttu-id="bfe2e-146">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-146">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="bfe2e-147">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-147">StorageV2.</span></span> <span data-ttu-id="bfe2e-148">GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-148">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="bfe2e-149">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-149">BlobStorage.</span></span> <span data-ttu-id="bfe2e-150">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-150">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="bfe2e-151">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-151">BlockBlobStorage.</span></span> <span data-ttu-id="bfe2e-152">Blockieren des BLOB-speicherkontos, das nur die Speicherung von BLOB-Blöcken unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-152">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="bfe2e-153">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-153">FileStorage.</span></span> <span data-ttu-id="bfe2e-154">Dateispeicher Konto, das nur die Speicherung von Dateien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-154">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="bfe2e-155">Der Standardwert ist StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-155">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="bfe2e-156">-Standort</span><span class="sxs-lookup"><span data-stu-id="bfe2e-156">-Location</span></span>
<span data-ttu-id="bfe2e-157">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-157">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="bfe2e-158">-Name</span><span class="sxs-lookup"><span data-stu-id="bfe2e-158">-Name</span></span>
<span data-ttu-id="bfe2e-159">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-159">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="bfe2e-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bfe2e-160">-NetworkRuleSet</span></span>
<span data-ttu-id="bfe2e-161">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="bfe2e-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe2e-162">-ResourceGroupName</span></span>
<span data-ttu-id="bfe2e-163">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-163">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="bfe2e-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bfe2e-164">-SkuName</span></span>
<span data-ttu-id="bfe2e-165">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-165">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="bfe2e-166">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bfe2e-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bfe2e-167">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-167">Standard_LRS.</span></span> <span data-ttu-id="bfe2e-168">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-168">Locally-redundant storage.</span></span>
- <span data-ttu-id="bfe2e-169">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-169">Standard_ZRS.</span></span> <span data-ttu-id="bfe2e-170">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-170">Zone-redundant storage.</span></span>
- <span data-ttu-id="bfe2e-171">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-171">Standard_GRS.</span></span> <span data-ttu-id="bfe2e-172">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-172">Geo-redundant storage.</span></span>
- <span data-ttu-id="bfe2e-173">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-173">Standard_RAGRS.</span></span> <span data-ttu-id="bfe2e-174">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-174">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="bfe2e-175">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-175">Premium_LRS.</span></span> <span data-ttu-id="bfe2e-176">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-176">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="bfe2e-177">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-177">Premium_ZRS.</span></span> <span data-ttu-id="bfe2e-178">Premium Zone – redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-178">Premium zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe2e-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="bfe2e-179">-Tag</span></span>
<span data-ttu-id="bfe2e-180">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-180">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="bfe2e-181">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="bfe2e-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bfe2e-182">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="bfe2e-182">-UseSubDomain</span></span>
<span data-ttu-id="bfe2e-183">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-183">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="bfe2e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe2e-184">CommonParameters</span></span>
<span data-ttu-id="bfe2e-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe2e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe2e-186">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe2e-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe2e-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bfe2e-187">INPUTS</span></span>

### <span data-ttu-id="bfe2e-188">System. String</span><span class="sxs-lookup"><span data-stu-id="bfe2e-188">System.String</span></span>

## <span data-ttu-id="bfe2e-189">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bfe2e-189">OUTPUTS</span></span>

### <span data-ttu-id="bfe2e-190">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfe2e-190">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bfe2e-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="bfe2e-191">NOTES</span></span>

## <span data-ttu-id="bfe2e-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bfe2e-192">RELATED LINKS</span></span>

[<span data-ttu-id="bfe2e-193">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfe2e-193">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="bfe2e-194">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfe2e-194">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="bfe2e-195">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bfe2e-195">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
