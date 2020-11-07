---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
ms.openlocfilehash: 3d2fd2ae65ff343bbe5faeece41194c768bec8c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850968"
---
# <span data-ttu-id="27297-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="27297-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="27297-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27297-102">SYNOPSIS</span></span>
<span data-ttu-id="27297-103">Legt die Speicherkapazität für eine Freigabe fest.</span><span class="sxs-lookup"><span data-stu-id="27297-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27297-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27297-104">SYNTAX</span></span>

### <span data-ttu-id="27297-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="27297-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="27297-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="27297-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="27297-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27297-107">DESCRIPTION</span></span>
<span data-ttu-id="27297-108">Das Cmdlet " **Set-AzureStorageShareQuota** " legt die Speicherkapazität für eine angegebene Freigabe fest.</span><span class="sxs-lookup"><span data-stu-id="27297-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="27297-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27297-109">EXAMPLES</span></span>

### <span data-ttu-id="27297-110">Beispiel 1: Einrichten der Speicherkapazität einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="27297-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="27297-111">Mit diesem Befehl wird die Speicherkapazität für eine Freigabe mit dem Namen ContosoShare01 auf 1024 GB festgelegt.</span><span class="sxs-lookup"><span data-stu-id="27297-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="27297-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27297-112">PARAMETERS</span></span>

### <span data-ttu-id="27297-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="27297-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="27297-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="27297-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="27297-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="27297-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="27297-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="27297-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27297-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="27297-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="27297-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="27297-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="27297-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="27297-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="27297-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="27297-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="27297-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="27297-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="27297-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="27297-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27297-123">-Context</span><span class="sxs-lookup"><span data-stu-id="27297-123">-Context</span></span>
<span data-ttu-id="27297-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="27297-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="27297-125">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="27297-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27297-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27297-126">-DefaultProfile</span></span>
<span data-ttu-id="27297-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27297-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27297-128">-Kontingent</span><span class="sxs-lookup"><span data-stu-id="27297-128">-Quota</span></span>
<span data-ttu-id="27297-129">Gibt den Kontingentwert in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="27297-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="27297-130">Sehen Sie sich die Kontingentbeschränkung in an https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="27297-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27297-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="27297-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="27297-132">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="27297-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27297-133">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="27297-133">-Share</span></span>
<span data-ttu-id="27297-134">Gibt ein **CloudFileShare** -Objekt an, das die Freigabe darstellt, für die diese Cmdlets ein Kontingent festlegen.</span><span class="sxs-lookup"><span data-stu-id="27297-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="27297-135">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="27297-135">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27297-136">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="27297-136">-ShareName</span></span>
<span data-ttu-id="27297-137">Gibt den Namen der Dateifreigabe an, für die ein Kontingent festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27297-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27297-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27297-138">CommonParameters</span></span>
<span data-ttu-id="27297-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27297-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27297-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27297-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27297-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27297-141">INPUTS</span></span>

### <span data-ttu-id="27297-142">System. String</span><span class="sxs-lookup"><span data-stu-id="27297-142">System.String</span></span>

### <span data-ttu-id="27297-143">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="27297-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="27297-144">Parameter: freigeben (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27297-144">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="27297-145">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27297-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="27297-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27297-146">OUTPUTS</span></span>

### <span data-ttu-id="27297-147">Microsoft. WindowsAzure. Storage. File. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="27297-147">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="27297-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="27297-148">NOTES</span></span>

## <span data-ttu-id="27297-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27297-149">RELATED LINKS</span></span>

[<span data-ttu-id="27297-150">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="27297-150">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="27297-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="27297-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="27297-152">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="27297-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
