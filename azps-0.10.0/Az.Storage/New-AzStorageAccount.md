---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 3ded950659546b6ec2a25271bc09718c937d401b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843031"
---
# <span data-ttu-id="58bb1-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58bb1-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="58bb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="58bb1-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="58bb1-103">Creates a Storage account.</span></span>

## <span data-ttu-id="58bb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58bb1-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>]
 [-UseSubDomain <Boolean>] [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58bb1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58bb1-105">DESCRIPTION</span></span>
<span data-ttu-id="58bb1-106">Das Cmdlet **New-AzStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="58bb1-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="58bb1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58bb1-107">EXAMPLES</span></span>

### <span data-ttu-id="58bb1-108">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="58bb1-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="58bb1-109">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="58bb1-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="58bb1-110">Beispiel 2: Erstellen eines BLOB-speicherkontos mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="58bb1-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="58bb1-111">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das mit BlobStorage-freundlicher und heißer AccessTier</span><span class="sxs-lookup"><span data-stu-id="58bb1-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="58bb1-112">Beispiel 3: Erstellen eines speicherkontos mit der Art StorageV2 und generieren und Zuweisen einer Identität für Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="58bb1-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="58bb1-113">Dieser Befehl erstellt ein Speicherkonto mit der Art StorageV2.</span><span class="sxs-lookup"><span data-stu-id="58bb1-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="58bb1-114">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="58bb1-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="58bb1-115">Beispiel 4: Erstellen eines speicherkontos mit NetworkRuleSet aus JSON</span><span class="sxs-lookup"><span data-stu-id="58bb1-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="58bb1-116">Mit diesem Befehl wird ein Speicherkonto erstellt, das über die NetworkRuleSet-Eigenschaft von JSON verfügt</span><span class="sxs-lookup"><span data-stu-id="58bb1-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

## <span data-ttu-id="58bb1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="58bb1-117">PARAMETERS</span></span>

### <span data-ttu-id="58bb1-118">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="58bb1-118">-AccessTier</span></span>
<span data-ttu-id="58bb1-119">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-119">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="58bb1-120">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="58bb1-120">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="58bb1-121">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="58bb1-121">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="58bb1-122">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-122">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="58bb1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58bb1-123">-AsJob</span></span>
<span data-ttu-id="58bb1-124">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58bb1-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58bb1-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="58bb1-125">-AssignIdentity</span></span>
<span data-ttu-id="58bb1-126">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="58bb1-126">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="58bb1-127">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="58bb1-127">-CustomDomainName</span></span>
<span data-ttu-id="58bb1-128">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-128">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="58bb1-129">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="58bb1-129">The default value is Storage.</span></span>

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

### <span data-ttu-id="58bb1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bb1-130">-DefaultProfile</span></span>
<span data-ttu-id="58bb1-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58bb1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58bb1-132">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="58bb1-132">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="58bb1-133">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="58bb1-133">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58bb1-134">-Art</span><span class="sxs-lookup"><span data-stu-id="58bb1-134">-Kind</span></span>
<span data-ttu-id="58bb1-135">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-135">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="58bb1-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58bb1-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58bb1-137">Speicher.</span><span class="sxs-lookup"><span data-stu-id="58bb1-137">Storage.</span></span> <span data-ttu-id="58bb1-138">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58bb1-138">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="58bb1-139">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="58bb1-139">StorageV2.</span></span> <span data-ttu-id="58bb1-140">GPv2-Speicherkonto (General Purpose Version 2), das BLOBs, Tabellen, Warteschlangen, Dateien und Datenträger mit erweiterten Features wie Datenebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58bb1-140">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="58bb1-141">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="58bb1-141">BlobStorage.</span></span> <span data-ttu-id="58bb1-142">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58bb1-142">Blob Storage account which supports storage of Blobs only.</span></span>
<span data-ttu-id="58bb1-143">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="58bb1-143">The default value is Storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58bb1-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="58bb1-144">-Location</span></span>
<span data-ttu-id="58bb1-145">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-145">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="58bb1-146">-Name</span><span class="sxs-lookup"><span data-stu-id="58bb1-146">-Name</span></span>
<span data-ttu-id="58bb1-147">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bb1-147">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="58bb1-148">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="58bb1-148">-NetworkRuleSet</span></span>
<span data-ttu-id="58bb1-149">NetworkRuleSet wird verwendet, um eine Reihe von Konfigurationsregeln für Firewalls und virtuelle Netzwerke zu definieren sowie Werte für Netzwerkeigenschaften festzulegen, beispielsweise Dienste, die die Regeln umgehen dürfen, und die Behandlung von Anforderungen, die keiner der definierten Regeln entsprechen.</span><span class="sxs-lookup"><span data-stu-id="58bb1-149">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="58bb1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58bb1-150">-ResourceGroupName</span></span>
<span data-ttu-id="58bb1-151">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58bb1-151">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="58bb1-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58bb1-152">-SkuName</span></span>
<span data-ttu-id="58bb1-153">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="58bb1-153">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="58bb1-154">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58bb1-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58bb1-155">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="58bb1-155">Standard_LRS.</span></span> <span data-ttu-id="58bb1-156">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="58bb1-156">Locally-redundant storage.</span></span>
- <span data-ttu-id="58bb1-157">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="58bb1-157">Standard_ZRS.</span></span> <span data-ttu-id="58bb1-158">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="58bb1-158">Zone-redundant storage.</span></span>
- <span data-ttu-id="58bb1-159">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="58bb1-159">Standard_GRS.</span></span> <span data-ttu-id="58bb1-160">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="58bb1-160">Geo-redundant storage.</span></span>
- <span data-ttu-id="58bb1-161">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="58bb1-161">Standard_RAGRS.</span></span> <span data-ttu-id="58bb1-162">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="58bb1-162">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="58bb1-163">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="58bb1-163">Premium_LRS.</span></span> <span data-ttu-id="58bb1-164">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="58bb1-164">Premium locally-redundant storage.</span></span>

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

### <span data-ttu-id="58bb1-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="58bb1-165">-Tag</span></span>
<span data-ttu-id="58bb1-166">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="58bb1-166">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="58bb1-167">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="58bb1-167">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58bb1-168">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="58bb1-168">-UseSubDomain</span></span>
<span data-ttu-id="58bb1-169">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58bb1-169">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="58bb1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bb1-170">CommonParameters</span></span>
<span data-ttu-id="58bb1-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58bb1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bb1-172">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bb1-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bb1-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58bb1-173">INPUTS</span></span>

### <span data-ttu-id="58bb1-174">System. String</span><span class="sxs-lookup"><span data-stu-id="58bb1-174">System.String</span></span>

### <span data-ttu-id="58bb1-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="58bb1-175">System.Boolean</span></span>

## <span data-ttu-id="58bb1-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58bb1-176">OUTPUTS</span></span>

### <span data-ttu-id="58bb1-177">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58bb1-177">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="58bb1-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="58bb1-178">NOTES</span></span>

## <span data-ttu-id="58bb1-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58bb1-179">RELATED LINKS</span></span>

[<span data-ttu-id="58bb1-180">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58bb1-180">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="58bb1-181">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58bb1-181">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="58bb1-182">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="58bb1-182">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
