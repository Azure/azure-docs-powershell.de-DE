---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 316bcbd8efa101a53dc36ede5e56e2b9379f02e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658837"
---
# <span data-ttu-id="82b91-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82b91-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="82b91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82b91-102">SYNOPSIS</span></span>
<span data-ttu-id="82b91-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="82b91-103">Creates a Storage account.</span></span>

## <span data-ttu-id="82b91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82b91-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82b91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82b91-105">DESCRIPTION</span></span>
<span data-ttu-id="82b91-106">Das Cmdlet **New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="82b91-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="82b91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82b91-107">EXAMPLES</span></span>

### <span data-ttu-id="82b91-108">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="82b91-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="82b91-109">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="82b91-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="82b91-110">Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="82b91-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="82b91-111">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="82b91-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="82b91-112">Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="82b91-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="82b91-113">Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.</span><span class="sxs-lookup"><span data-stu-id="82b91-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="82b91-114">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="82b91-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="82b91-115">Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="82b91-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="82b91-116">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt</span><span class="sxs-lookup"><span data-stu-id="82b91-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="82b91-117">Beispiel 5: Erstellen eines speicherkontos mit aktiviertem hierarchischen Namespace</span><span class="sxs-lookup"><span data-stu-id="82b91-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="82b91-118">Mit diesem Befehl wird ein Speicherkonto mit aktiviertem hierarchischen Namespace erstellt.</span><span class="sxs-lookup"><span data-stu-id="82b91-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

## <span data-ttu-id="82b91-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="82b91-119">PARAMETERS</span></span>

### <span data-ttu-id="82b91-120">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="82b91-120">-AccessTier</span></span>
<span data-ttu-id="82b91-121">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="82b91-121">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="82b91-122">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="82b91-122">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="82b91-123">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="82b91-123">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="82b91-124">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="82b91-124">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="82b91-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b91-125">-AsJob</span></span>
<span data-ttu-id="82b91-126">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82b91-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b91-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="82b91-127">-AssignIdentity</span></span>
<span data-ttu-id="82b91-128">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="82b91-128">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="82b91-129">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="82b91-129">-CustomDomainName</span></span>
<span data-ttu-id="82b91-130">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="82b91-130">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="82b91-131">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="82b91-131">The default value is Storage.</span></span>

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

### <span data-ttu-id="82b91-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b91-132">-DefaultProfile</span></span>
<span data-ttu-id="82b91-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82b91-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b91-134">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="82b91-134">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="82b91-135">Gibt an, ob das Speicherkonto den hierarchischen Namespace aktiviert.</span><span class="sxs-lookup"><span data-stu-id="82b91-135">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="82b91-136">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="82b91-136">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="82b91-137">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="82b91-137">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="82b91-138">-Art</span><span class="sxs-lookup"><span data-stu-id="82b91-138">-Kind</span></span>
<span data-ttu-id="82b91-139">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="82b91-139">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="82b91-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="82b91-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82b91-141">Speicher.</span><span class="sxs-lookup"><span data-stu-id="82b91-141">Storage.</span></span> <span data-ttu-id="82b91-142">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82b91-142">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="82b91-143">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="82b91-143">StorageV2.</span></span> <span data-ttu-id="82b91-144">GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82b91-144">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="82b91-145">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="82b91-145">BlobStorage.</span></span> <span data-ttu-id="82b91-146">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82b91-146">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="82b91-147">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="82b91-147">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b91-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="82b91-148">-Location</span></span>
<span data-ttu-id="82b91-149">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="82b91-149">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="82b91-150">-Name</span><span class="sxs-lookup"><span data-stu-id="82b91-150">-Name</span></span>
<span data-ttu-id="82b91-151">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="82b91-151">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="82b91-152">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="82b91-152">-NetworkRuleSet</span></span>
<span data-ttu-id="82b91-153">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="82b91-153">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="82b91-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b91-154">-ResourceGroupName</span></span>
<span data-ttu-id="82b91-155">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b91-155">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="82b91-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="82b91-156">-SkuName</span></span>
<span data-ttu-id="82b91-157">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="82b91-157">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="82b91-158">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="82b91-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="82b91-159">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="82b91-159">Standard_LRS.</span></span> <span data-ttu-id="82b91-160">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="82b91-160">Locally-redundant storage.</span></span>
- <span data-ttu-id="82b91-161">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="82b91-161">Standard_ZRS.</span></span> <span data-ttu-id="82b91-162">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="82b91-162">Zone-redundant storage.</span></span>
- <span data-ttu-id="82b91-163">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="82b91-163">Standard_GRS.</span></span> <span data-ttu-id="82b91-164">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="82b91-164">Geo-redundant storage.</span></span>
- <span data-ttu-id="82b91-165">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="82b91-165">Standard_RAGRS.</span></span> <span data-ttu-id="82b91-166">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="82b91-166">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="82b91-167">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="82b91-167">Premium_LRS.</span></span> <span data-ttu-id="82b91-168">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="82b91-168">Premium locally-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b91-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="82b91-169">-Tag</span></span>
<span data-ttu-id="82b91-170">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="82b91-170">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="82b91-171">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="82b91-171">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="82b91-172">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="82b91-172">-UseSubDomain</span></span>
<span data-ttu-id="82b91-173">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b91-173">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="82b91-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b91-174">CommonParameters</span></span>
<span data-ttu-id="82b91-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b91-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b91-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b91-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b91-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82b91-177">INPUTS</span></span>

### <span data-ttu-id="82b91-178">System. String</span><span class="sxs-lookup"><span data-stu-id="82b91-178">System.String</span></span>

## <span data-ttu-id="82b91-179">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82b91-179">OUTPUTS</span></span>

### <span data-ttu-id="82b91-180">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82b91-180">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="82b91-181">Notizen</span><span class="sxs-lookup"><span data-stu-id="82b91-181">NOTES</span></span>

## <span data-ttu-id="82b91-182">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82b91-182">RELATED LINKS</span></span>

[<span data-ttu-id="82b91-183">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82b91-183">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="82b91-184">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82b91-184">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="82b91-185">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="82b91-185">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
