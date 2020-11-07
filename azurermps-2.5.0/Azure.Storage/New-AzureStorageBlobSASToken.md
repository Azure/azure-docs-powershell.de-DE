---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
ms.openlocfilehash: a85f9a741848824554bb3df49075fad49bfe4015
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849832"
---
# <span data-ttu-id="25afc-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="25afc-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="25afc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25afc-102">SYNOPSIS</span></span>
<span data-ttu-id="25afc-103">Generiert ein SAS-Token für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="25afc-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25afc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25afc-104">SYNTAX</span></span>

### <span data-ttu-id="25afc-105">BlobNameWithPermission (Standard)</span><span class="sxs-lookup"><span data-stu-id="25afc-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25afc-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="25afc-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25afc-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="25afc-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25afc-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="25afc-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25afc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25afc-109">DESCRIPTION</span></span>
<span data-ttu-id="25afc-110">Das Cmdlet **New-AzureStorageBlobSASToken** generiert ein SAS-Token (Shared Access Signature) für ein Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="25afc-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="25afc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25afc-111">EXAMPLES</span></span>

### <span data-ttu-id="25afc-112">Beispiel 1: Generieren eines BLOB-SAS-Tokens mit vollständiger BLOB-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="25afc-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="25afc-113">In diesem Beispiel wird ein BLOB-SAS-Token mit vollständiger BLOB-Berechtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="25afc-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="25afc-114">Beispiel 2: Generieren eines BLOB-SAS-Tokens mit Lebensdauer</span><span class="sxs-lookup"><span data-stu-id="25afc-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="25afc-115">In diesem Beispiel wird ein BLOB-SAS-Token mit Lebensdauer generiert.</span><span class="sxs-lookup"><span data-stu-id="25afc-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="25afc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="25afc-116">PARAMETERS</span></span>

### <span data-ttu-id="25afc-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="25afc-117">-Blob</span></span>
<span data-ttu-id="25afc-118">Gibt den Speicher-BLOB-Namen an.</span><span class="sxs-lookup"><span data-stu-id="25afc-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="25afc-119">-CloudBlob</span></span>
<span data-ttu-id="25afc-120">Gibt das **CloudBlob** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="25afc-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="25afc-121">Verwenden Sie das Cmdlet [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) , um ein **CloudBlob** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="25afc-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-122">-Container</span><span class="sxs-lookup"><span data-stu-id="25afc-122">-Container</span></span>
<span data-ttu-id="25afc-123">Gibt den Namen des Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="25afc-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-124">-Context</span><span class="sxs-lookup"><span data-stu-id="25afc-124">-Context</span></span>
<span data-ttu-id="25afc-125">Gibt den Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="25afc-125">Specifies the storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25afc-126">-DefaultProfile</span></span>
<span data-ttu-id="25afc-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25afc-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25afc-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="25afc-128">-ExpiryTime</span></span>
<span data-ttu-id="25afc-129">Gibt an, wann die freigegebene zugriffssignatur abläuft.</span><span class="sxs-lookup"><span data-stu-id="25afc-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="25afc-130">-FullUri</span></span>
<span data-ttu-id="25afc-131">Gibt an, dass dieses Cmdlet den vollständigen BLOB-URI und das Shared Access-Signaturtoken zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="25afc-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="25afc-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="25afc-132">-IPAddressOrRange</span></span>
<span data-ttu-id="25afc-133">Gibt die IP-Adresse oder den Bereich von IP-Adressen an, aus denen Anforderungen wie 168.1.5.65 oder 168.1.5.60-168.1.5.70 akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="25afc-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="25afc-134">Der Bereich ist inklusive.</span><span class="sxs-lookup"><span data-stu-id="25afc-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="25afc-135">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="25afc-135">-Permission</span></span>
<span data-ttu-id="25afc-136">Gibt die Berechtigungen für ein Speicher-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="25afc-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="25afc-137">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` (für lesen, schreiben und löschen) handelt.</span><span class="sxs-lookup"><span data-stu-id="25afc-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-138">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="25afc-138">-Policy</span></span>
<span data-ttu-id="25afc-139">Gibt eine Azure stored Access-Richtlinie an.</span><span class="sxs-lookup"><span data-stu-id="25afc-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-140">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="25afc-140">-Protocol</span></span>
<span data-ttu-id="25afc-141">Gibt das für eine Anforderung zugelassene Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="25afc-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="25afc-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25afc-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="25afc-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="25afc-143">HttpsOnly</span></span>
* <span data-ttu-id="25afc-144">HttpsOrHttp der Standardwert ist HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="25afc-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-145">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="25afc-145">-StartTime</span></span>
<span data-ttu-id="25afc-146">Gibt den Zeitpunkt an, zu dem die freigegebene zugriffssignatur gültig wird.</span><span class="sxs-lookup"><span data-stu-id="25afc-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25afc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25afc-147">CommonParameters</span></span>
<span data-ttu-id="25afc-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25afc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25afc-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25afc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25afc-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25afc-150">INPUTS</span></span>

### <span data-ttu-id="25afc-151">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="25afc-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="25afc-152">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="25afc-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="25afc-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25afc-153">OUTPUTS</span></span>

### <span data-ttu-id="25afc-154">System. String</span><span class="sxs-lookup"><span data-stu-id="25afc-154">System.String</span></span>

## <span data-ttu-id="25afc-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="25afc-155">NOTES</span></span>

## <span data-ttu-id="25afc-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25afc-156">RELATED LINKS</span></span>

[<span data-ttu-id="25afc-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="25afc-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="25afc-158">Neu – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="25afc-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
