---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: d75111b27b03317f757cbf0def4d9d66c43427c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663511"
---
# <span data-ttu-id="9c015-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="9c015-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="9c015-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c015-102">SYNOPSIS</span></span>
<span data-ttu-id="9c015-103">Generiert ein SAS-Token für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="9c015-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c015-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c015-104">SYNTAX</span></span>

### <span data-ttu-id="9c015-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="9c015-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="9c015-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9c015-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="9c015-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="9c015-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="9c015-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="9c015-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9c015-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c015-109">DESCRIPTION</span></span>
<span data-ttu-id="9c015-110">Das Cmdlet **New-AzureStorageBlobSASToken** generiert ein SAS-Token (Shared Access Signature) für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="9c015-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="9c015-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c015-111">EXAMPLES</span></span>

### <span data-ttu-id="9c015-112">Beispiel 1: Generieren eines BLOB-SAS-Tokens mit vollständiger BLOB-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="9c015-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="9c015-113">In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger BLOB-Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="9c015-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="9c015-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="9c015-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="9c015-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="9c015-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="9c015-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c015-116">PARAMETERS</span></span>

### <span data-ttu-id="9c015-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="9c015-117">-Blob</span></span>
<span data-ttu-id="9c015-118">Gibt den Speicher-BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="9c015-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="9c015-119">-CloudBlob</span></span>
<span data-ttu-id="9c015-120">Gibt das **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9c015-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="9c015-121">Verwenden Sie das Cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) , um ein **CloudBlob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c015-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-122">-Container</span><span class="sxs-lookup"><span data-stu-id="9c015-122">-Container</span></span>
<span data-ttu-id="9c015-123">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="9c015-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-124">-Context</span><span class="sxs-lookup"><span data-stu-id="9c015-124">-Context</span></span>
<span data-ttu-id="9c015-125">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9c015-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9c015-126">-ExpiryTime</span></span>
<span data-ttu-id="9c015-127">Gibt an, wann die freigegebene zugriffssignatur abläuft.</span><span class="sxs-lookup"><span data-stu-id="9c015-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9c015-128">-FullUri</span></span>
<span data-ttu-id="9c015-129">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9c015-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="9c015-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9c015-130">-IPAddressOrRange</span></span>
<span data-ttu-id="9c015-131">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="9c015-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9c015-132">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="9c015-132">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-133">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="9c015-133">-Permission</span></span>
<span data-ttu-id="9c015-134">Gibt die Berechtigungen für ein Speicher-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="9c015-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-135">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="9c015-135">-Policy</span></span>
<span data-ttu-id="9c015-136">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="9c015-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9c015-137">-Protocol</span></span>
<span data-ttu-id="9c015-138">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="9c015-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9c015-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c015-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9c015-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9c015-140">HttpsOnly</span></span>
* <span data-ttu-id="9c015-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="9c015-141">HttpsOrHttp</span></span>

<span data-ttu-id="9c015-142">Der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9c015-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-143">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="9c015-143">-StartTime</span></span>
<span data-ttu-id="9c015-144">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="9c015-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c015-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c015-145">CommonParameters</span></span>
<span data-ttu-id="9c015-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c015-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c015-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c015-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c015-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c015-148">INPUTS</span></span>

### <span data-ttu-id="9c015-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9c015-149">IStorageContext</span></span>

<span data-ttu-id="9c015-150">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9c015-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="9c015-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c015-151">OUTPUTS</span></span>

### <span data-ttu-id="9c015-152">System. String</span><span class="sxs-lookup"><span data-stu-id="9c015-152">System.String</span></span>

## <span data-ttu-id="9c015-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c015-153">NOTES</span></span>

## <span data-ttu-id="9c015-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c015-154">RELATED LINKS</span></span>

[<span data-ttu-id="9c015-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="9c015-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="9c015-156">Neu – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="9c015-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
