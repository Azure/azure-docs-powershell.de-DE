---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 1b00930332d9f3f5a78e4cfe8ab7478a5dc5fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502321"
---
# <span data-ttu-id="4e861-101">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e861-101">New-AzureRmStorageAccount</span></span>

## <span data-ttu-id="4e861-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e861-102">SYNOPSIS</span></span>
<span data-ttu-id="4e861-103">Erstellt ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="4e861-103">Creates a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e861-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e861-104">SYNTAX</span></span>

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4e861-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e861-105">DESCRIPTION</span></span>
<span data-ttu-id="4e861-106">Das Cmdlet **New-AzureRmStorageAccount** erstellt ein Azure Storage-Konto.</span><span class="sxs-lookup"><span data-stu-id="4e861-106">The **New-AzureRmStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="4e861-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e861-107">EXAMPLES</span></span>

### <span data-ttu-id="4e861-108">Beispiel 1: Erstellen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="4e861-108">Example 1: Create a Storage Account</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS"
```

<span data-ttu-id="4e861-109">Mit diesem Befehl wird ein Speicherkonto für den Ressourcengruppennamen myresourcegroup erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e861-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="4e861-110">Beispiel 2: Erstellen eines BLOB-speicherkontos, das die Speicherdienst Verschlüsselung verwendet</span><span class="sxs-lookup"><span data-stu-id="4e861-110">Example 2: Create a Blob Storage account that uses Storage Service Encryption</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

<span data-ttu-id="4e861-111">Mit diesem Befehl wird ein BLOB-Speicherkonto erstellt, das den Typ "heißer Zugriff" verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e861-111">This command creates a Blob Storage account that uses the hot access type.</span></span>
<span data-ttu-id="4e861-112">Das Konto hat die Speicherdienst Verschlüsselung für den BLOB-Dienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e861-112">The account has enabled Storage Service encryption on Blob Service.</span></span>

### <span data-ttu-id="4e861-113">Beispiel 3: Erstellen eines speicherkontos, das die Speicherdienst Verschlüsselung für BLOB-und Dateidienste aktiviert und eine Identität für Azure keyvault generiert und zuweist.</span><span class="sxs-lookup"><span data-stu-id="4e861-113">Example 3: Create a Storage Account that Enables Storage Service Encryption on Blob and File Services, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "West US" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

<span data-ttu-id="4e861-114">Mit diesem Befehl wird ein Speicherkonto erstellt, das die Speicherdienst Verschlüsselung für BLOB-und Dateidienste aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="4e861-114">This command creates a Storage account that enabled Storage Service encryption on Blob and File Services.</span></span>  <span data-ttu-id="4e861-115">Darüber hinaus wird eine Identität generiert und zugewiesen, die zum Verwalten von Konto Schlüsseln über Azure keyvault verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e861-115">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

## <span data-ttu-id="4e861-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e861-116">PARAMETERS</span></span>

### <span data-ttu-id="4e861-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="4e861-117">-AccessTier</span></span>
<span data-ttu-id="4e861-118">Gibt die Zugriffsebene des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4e861-118">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="4e861-119">Die akzeptablen Werte für diesen Parameter sind: heiß und cool.</span><span class="sxs-lookup"><span data-stu-id="4e861-119">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="4e861-120">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4e861-120">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="4e861-121">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="4e861-121">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4e861-122">-AssignIdentity</span></span>
<span data-ttu-id="4e861-123">Generieren und Zuweisen einer neuen Speicherkonto Identität für dieses Speicherkonto für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault</span><span class="sxs-lookup"><span data-stu-id="4e861-123">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4e861-124">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4e861-124">-CustomDomainName</span></span>
<span data-ttu-id="4e861-125">Gibt den Namen der benutzerdefinierten Domäne des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4e861-125">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="4e861-126">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="4e861-126">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-127">-EnableEncryptionService</span><span class="sxs-lookup"><span data-stu-id="4e861-127">-EnableEncryptionService</span></span>
<span data-ttu-id="4e861-128">Gibt an, ob dieses Cmdlet Speicherdienst Verschlüsselung für den Speicherdienst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e861-128">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="4e861-129">Azure-BLOB-und Azure-Dateidienste werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e861-129">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-130">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="4e861-130">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="4e861-131">Gibt an, ob das Speicherkonto nur HTTPS-Datenverkehr aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4e861-131">Indicates whether or not the Storage Account only enable https traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-132">-Information</span><span class="sxs-lookup"><span data-stu-id="4e861-132">-InformationAction</span></span>
<span data-ttu-id="4e861-133">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4e861-133">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4e861-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e861-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e861-135">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4e861-135">Continue</span></span>
- <span data-ttu-id="4e861-136">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4e861-136">Ignore</span></span>
- <span data-ttu-id="4e861-137">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4e861-137">Inquire</span></span>
- <span data-ttu-id="4e861-138">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4e861-138">SilentlyContinue</span></span>
- <span data-ttu-id="4e861-139">Beenden</span><span class="sxs-lookup"><span data-stu-id="4e861-139">Stop</span></span>
- <span data-ttu-id="4e861-140">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4e861-140">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4e861-141">-InformationVariable</span></span>
<span data-ttu-id="4e861-142">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4e861-142">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-143">-Art</span><span class="sxs-lookup"><span data-stu-id="4e861-143">-Kind</span></span>
<span data-ttu-id="4e861-144">Gibt die Art des vom Cmdlet erstellten speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4e861-144">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="4e861-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e861-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e861-146">Speicher.</span><span class="sxs-lookup"><span data-stu-id="4e861-146">Storage.</span></span>
<span data-ttu-id="4e861-147">Speicherkonto für allgemeine Zwecke, das die Speicherung von BLOBs, Tabellen, Warteschlangen, Dateien und Datenträgern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e861-147">General purpose storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>

- <span data-ttu-id="4e861-148">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="4e861-148">BlobStorage.</span></span>
<span data-ttu-id="4e861-149">BLOB-Speicherkonto, das nur BLOB-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e861-149">Blob storage account which supports storage of Blobs only.</span></span>


<span data-ttu-id="4e861-150">Der Standardwert ist Storage.</span><span class="sxs-lookup"><span data-stu-id="4e861-150">The default value is Storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-151">-Standort</span><span class="sxs-lookup"><span data-stu-id="4e861-151">-Location</span></span>
<span data-ttu-id="4e861-152">Gibt den Speicherort des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4e861-152">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-153">-Name</span><span class="sxs-lookup"><span data-stu-id="4e861-153">-Name</span></span>
<span data-ttu-id="4e861-154">Gibt den Namen des zu erstellende speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4e861-154">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e861-155">-ResourceGroupName</span></span>
<span data-ttu-id="4e861-156">Gibt den Namen der Ressourcengruppe an, in der das Speicherkonto hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e861-156">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="4e861-157">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4e861-157">-SkuName</span></span>
<span data-ttu-id="4e861-158">Gibt den SKU-Namen des speicherkontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e861-158">Specifies the SKU name of the storage account that this cmdlet creates.</span></span>
<span data-ttu-id="4e861-159">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e861-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e861-160">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="4e861-160">Standard_LRS.</span></span>
<span data-ttu-id="4e861-161">Lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="4e861-161">Locally-redundant storage.</span></span>
- <span data-ttu-id="4e861-162">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="4e861-162">Standard_ZRS.</span></span>
<span data-ttu-id="4e861-163">Zone – redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="4e861-163">Zone-redundant storage.</span></span>
- <span data-ttu-id="4e861-164">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="4e861-164">Standard_GRS.</span></span>
<span data-ttu-id="4e861-165">Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="4e861-165">Geo-redundant storage.</span></span>
- <span data-ttu-id="4e861-166">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="4e861-166">Standard_RAGRS.</span></span>
<span data-ttu-id="4e861-167">Lesezugriff Geo-redundanter Speicher.</span><span class="sxs-lookup"><span data-stu-id="4e861-167">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="4e861-168">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="4e861-168">Premium_LRS.</span></span>
<span data-ttu-id="4e861-169">Premium-lokal redundanter Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="4e861-169">Premium locally-redundant storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="4e861-170">-Tag</span></span>
<span data-ttu-id="4e861-171">Wenn Sie einen Wert von BlobStorage für den Parameter *Kind* angeben, müssen Sie einen Wert für den *AccessTier* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="4e861-171">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="4e861-172">Wenn Sie einen Wert für Storage für diesen *Art* -Parameter angeben, geben Sie den *AccessTier* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="4e861-172">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-173">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="4e861-173">-UseSubDomain</span></span>
<span data-ttu-id="4e861-174">Gibt an, ob die indirekte CNAME-Validierung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e861-174">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e861-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e861-175">CommonParameters</span></span>
<span data-ttu-id="4e861-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e861-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e861-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e861-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e861-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e861-178">INPUTS</span></span>

### <span data-ttu-id="4e861-179">Keine</span><span class="sxs-lookup"><span data-stu-id="4e861-179">None</span></span>
<span data-ttu-id="4e861-180">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4e861-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e861-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e861-181">OUTPUTS</span></span>

## <span data-ttu-id="4e861-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e861-182">NOTES</span></span>

## <span data-ttu-id="4e861-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e861-183">RELATED LINKS</span></span>

[<span data-ttu-id="4e861-184">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e861-184">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="4e861-185">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e861-185">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="4e861-186">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4e861-186">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
