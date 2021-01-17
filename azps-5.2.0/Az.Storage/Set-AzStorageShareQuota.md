---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303243"
---
# <span data-ttu-id="6013c-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6013c-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="6013c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6013c-102">SYNOPSIS</span></span>
<span data-ttu-id="6013c-103">Legt die Speicherkapazität für eine Freigabe fest.</span><span class="sxs-lookup"><span data-stu-id="6013c-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="6013c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6013c-104">SYNTAX</span></span>

### <span data-ttu-id="6013c-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6013c-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6013c-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="6013c-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="6013c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6013c-107">DESCRIPTION</span></span>
<span data-ttu-id="6013c-108">Das **Cmdlet "Set-AzStorageShareQuota"** legt die Speicherkapazität für eine angegebene Freigabe fest.</span><span class="sxs-lookup"><span data-stu-id="6013c-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="6013c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6013c-109">EXAMPLES</span></span>

### <span data-ttu-id="6013c-110">Beispiel 1: Festlegen der Speicherkapazität einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="6013c-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="6013c-111">Mit diesem Befehl wird die Speicherkapazität für eine Freigabe namens ContosoShare01 auf 1024 GB erhöht.</span><span class="sxs-lookup"><span data-stu-id="6013c-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="6013c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6013c-112">PARAMETERS</span></span>

### <span data-ttu-id="6013c-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6013c-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6013c-114">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="6013c-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6013c-115">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6013c-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6013c-116">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="6013c-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6013c-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6013c-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6013c-118">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="6013c-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6013c-119">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="6013c-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6013c-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="6013c-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6013c-121">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="6013c-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6013c-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="6013c-122">The default value is 10.</span></span>

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

### <span data-ttu-id="6013c-123">-Context</span><span class="sxs-lookup"><span data-stu-id="6013c-123">-Context</span></span>
<span data-ttu-id="6013c-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="6013c-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6013c-125">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="6013c-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6013c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6013c-126">-DefaultProfile</span></span>
<span data-ttu-id="6013c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6013c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6013c-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="6013c-128">-Quota</span></span>
<span data-ttu-id="6013c-129">Gibt den Kontingentwert in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="6013c-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="6013c-130">Sehen Sie sich die Kontingentbeschränkung in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits an.</span><span class="sxs-lookup"><span data-stu-id="6013c-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6013c-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6013c-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6013c-132">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="6013c-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6013c-133">-Teilen</span><span class="sxs-lookup"><span data-stu-id="6013c-133">-Share</span></span>
<span data-ttu-id="6013c-134">Gibt ein **CloudFileShare-Objekt** an, das die Freigabe repräsentiert, für die diese Cmdlets ein Kontingent festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="6013c-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="6013c-135">Verwenden Sie zum Abrufen **eines CloudFileShare-Objekts** das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6013c-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6013c-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6013c-136">-ShareName</span></span>
<span data-ttu-id="6013c-137">Gibt den Namen der Dateifreigabe an, für die ein Kontingent festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6013c-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="6013c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6013c-138">CommonParameters</span></span>
<span data-ttu-id="6013c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6013c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6013c-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6013c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6013c-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6013c-141">INPUTS</span></span>

### <span data-ttu-id="6013c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6013c-142">System.String</span></span>

### <span data-ttu-id="6013c-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6013c-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="6013c-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6013c-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6013c-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6013c-145">OUTPUTS</span></span>

### <span data-ttu-id="6013c-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="6013c-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="6013c-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6013c-147">NOTES</span></span>

## <span data-ttu-id="6013c-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6013c-148">RELATED LINKS</span></span>

[<span data-ttu-id="6013c-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6013c-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="6013c-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="6013c-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="6013c-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6013c-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
