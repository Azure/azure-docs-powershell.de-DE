---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 072e9b16bec9709808cd3da7c90d60a6055f0363
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496742"
---
# <span data-ttu-id="57172-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57172-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="57172-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57172-102">SYNOPSIS</span></span>
<span data-ttu-id="57172-103">Erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="57172-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57172-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57172-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="57172-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57172-105">DESCRIPTION</span></span>
<span data-ttu-id="57172-106">Das Cmdlet **New-AzureStorageContainerStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für einen Azure-Speichercontainer.</span><span class="sxs-lookup"><span data-stu-id="57172-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="57172-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57172-107">EXAMPLES</span></span>

### <span data-ttu-id="57172-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einem Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="57172-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="57172-109">Dieser Befehl erstellt eine Access-Richtlinie mit dem Namen Policy01 im Speichercontainer mit dem Namen MyContainer.</span><span class="sxs-lookup"><span data-stu-id="57172-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="57172-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="57172-110">PARAMETERS</span></span>

### <span data-ttu-id="57172-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57172-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="57172-112">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="57172-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="57172-113">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="57172-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="57172-114">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="57172-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57172-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="57172-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="57172-116">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="57172-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="57172-117">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="57172-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="57172-118">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="57172-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="57172-119">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="57172-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="57172-120">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="57172-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57172-121">-Container</span><span class="sxs-lookup"><span data-stu-id="57172-121">-Container</span></span>
<span data-ttu-id="57172-122">Gibt den Namen des Azure-Speichercontainers an.</span><span class="sxs-lookup"><span data-stu-id="57172-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57172-123">-Context</span><span class="sxs-lookup"><span data-stu-id="57172-123">-Context</span></span>
<span data-ttu-id="57172-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="57172-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="57172-125">Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57172-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="57172-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="57172-126">-ExpiryTime</span></span>
<span data-ttu-id="57172-127">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="57172-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="57172-128">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="57172-128">-Permission</span></span>
<span data-ttu-id="57172-129">Gibt Berechtigungen in der gespeicherten Zugriffsrichtlinie an, um auf den Container zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="57172-129">Specifies permissions in the stored access policy to access the container.</span></span>

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

### <span data-ttu-id="57172-130">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="57172-130">-Policy</span></span>
<span data-ttu-id="57172-131">Gibt eine gespeicherte Zugriffsrichtlinie an, die die Berechtigungen für dieses SAS-Token umfasst.</span><span class="sxs-lookup"><span data-stu-id="57172-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57172-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="57172-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="57172-133">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="57172-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="57172-134">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="57172-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="57172-135">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="57172-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57172-136">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="57172-136">-StartTime</span></span>
<span data-ttu-id="57172-137">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="57172-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="57172-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57172-138">CommonParameters</span></span>
<span data-ttu-id="57172-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57172-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57172-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57172-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57172-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57172-141">INPUTS</span></span>

### <span data-ttu-id="57172-142">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57172-142">String</span></span>

<span data-ttu-id="57172-143">Der Parameter "Container" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="57172-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="57172-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57172-144">IStorageContext</span></span>

<span data-ttu-id="57172-145">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="57172-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="57172-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57172-146">OUTPUTS</span></span>

### <span data-ttu-id="57172-147">System. String</span><span class="sxs-lookup"><span data-stu-id="57172-147">System.String</span></span>

## <span data-ttu-id="57172-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="57172-148">NOTES</span></span>

## <span data-ttu-id="57172-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57172-149">RELATED LINKS</span></span>

[<span data-ttu-id="57172-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57172-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="57172-151">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="57172-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="57172-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57172-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="57172-153">Satz-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57172-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


