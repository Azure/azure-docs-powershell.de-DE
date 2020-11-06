---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503354"
---
# <span data-ttu-id="e5fe6-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e5fe6-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="e5fe6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="e5fe6-103">Legt die CORS-Regeln für einen Typ von Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5fe6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5fe6-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e5fe6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="e5fe6-106">Das Cmdlet " **Set-AzureStorageCORSRule** " legt die Richtlinien für die Cross-Origin-Ressourcenfreigabe (CORS) für einen Typ von Azure-Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="e5fe6-107">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="e5fe6-108">Mit diesem Cmdlet werden die vorhandenen Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="e5fe6-109">Verwenden Sie das Cmdlet Get-AzureStorageCORSRule, um die aktuellen Regeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="e5fe6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5fe6-110">EXAMPLES</span></span>

### <span data-ttu-id="e5fe6-111">Beispiel 1: Zuweisen von CORS-Regeln zum BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="e5fe6-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e5fe6-112">Der erste Befehl weist der $CorsRules Variablen ein Array von Regeln zu.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="e5fe6-113">Dieser Befehl verwendet die Standarderweiterung über mehrere Zeilen in diesem Codeblock.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="e5fe6-114">Der zweite Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="e5fe6-115">Beispiel 2: Ändern der Eigenschaften einer CORS-Regel für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="e5fe6-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e5fe6-116">Der erste Befehl ruft die aktuellen CORS-Regeln für den BLOB-Typ mit dem Cmdlet **Get-AzureStorageCORSRule** ab.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="e5fe6-117">Der Befehl speichert die Regeln in der $CorsRules-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="e5fe6-118">Mit dem zweiten und dritten Befehl wird die erste Regel in $CorsRules geändert.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="e5fe6-119">Der endgültige Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="e5fe6-120">Durch die überarbeiteten Regeln werden die aktuellen CORS-Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="e5fe6-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5fe6-121">PARAMETERS</span></span>

### <span data-ttu-id="e5fe6-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e5fe6-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e5fe6-123">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e5fe6-124">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e5fe6-125">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e5fe6-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e5fe6-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e5fe6-127">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e5fe6-128">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e5fe6-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e5fe6-130">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e5fe6-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-131">The default value is 10.</span></span>

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

### <span data-ttu-id="e5fe6-132">-Context</span><span class="sxs-lookup"><span data-stu-id="e5fe6-132">-Context</span></span>
<span data-ttu-id="e5fe6-133">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e5fe6-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e5fe6-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="e5fe6-135">-CorsRules</span></span>
<span data-ttu-id="e5fe6-136">Gibt ein Array von CORS-Regeln an.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="e5fe6-137">Sie können die vorhandenen Regeln mithilfe des Get-AzureStorageCORSRule-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe6-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5fe6-138">-PassThru</span></span>
<span data-ttu-id="e5fe6-139">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="e5fe6-140">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e5fe6-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e5fe6-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e5fe6-142">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e5fe6-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e5fe6-143">-ServiceType</span></span>
<span data-ttu-id="e5fe6-144">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="e5fe6-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e5fe6-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5fe6-146">BLOB</span><span class="sxs-lookup"><span data-stu-id="e5fe6-146">Blob</span></span> 
- <span data-ttu-id="e5fe6-147">Tabelle</span><span class="sxs-lookup"><span data-stu-id="e5fe6-147">Table</span></span> 
- <span data-ttu-id="e5fe6-148">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e5fe6-148">Queue</span></span> 
- <span data-ttu-id="e5fe6-149">Datei</span><span class="sxs-lookup"><span data-stu-id="e5fe6-149">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5fe6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5fe6-150">CommonParameters</span></span>
<span data-ttu-id="e5fe6-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5fe6-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5fe6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5fe6-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5fe6-153">INPUTS</span></span>

### <span data-ttu-id="e5fe6-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5fe6-154">IStorageContext</span></span>

<span data-ttu-id="e5fe6-155">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5fe6-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e5fe6-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5fe6-156">OUTPUTS</span></span>

### <span data-ttu-id="e5fe6-157">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="e5fe6-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="e5fe6-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5fe6-158">NOTES</span></span>

## <span data-ttu-id="e5fe6-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5fe6-159">RELATED LINKS</span></span>

[<span data-ttu-id="e5fe6-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e5fe6-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="e5fe6-161">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5fe6-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e5fe6-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e5fe6-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


