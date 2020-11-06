---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
ms.openlocfilehash: 635b8e1524f6123aa6ddde4ed7a64768d6c3d791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475789"
---
# <span data-ttu-id="9d704-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9d704-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="9d704-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d704-102">SYNOPSIS</span></span>
<span data-ttu-id="9d704-103">Legt die CORS-Regeln für einen Typ von Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="9d704-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="9d704-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d704-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9d704-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d704-105">DESCRIPTION</span></span>
<span data-ttu-id="9d704-106">Das Cmdlet " **Set-AzureStorageCORSRule** " legt die Richtlinien für die Cross-Origin-Ressourcenfreigabe (CORS) für einen Typ von Azure-Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="9d704-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="9d704-107">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="9d704-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="9d704-108">Mit diesem Cmdlet werden die vorhandenen Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d704-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="9d704-109">Verwenden Sie das Cmdlet Get-AzureStorageCORSRule, um die aktuellen Regeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9d704-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="9d704-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d704-110">EXAMPLES</span></span>

### <span data-ttu-id="9d704-111">Beispiel 1: Zuweisen von CORS-Regeln zum BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="9d704-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="9d704-112">Der erste Befehl weist der $CorsRules Variablen ein Array von Regeln zu.</span><span class="sxs-lookup"><span data-stu-id="9d704-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="9d704-113">Dieser Befehl verwendet die Standarderweiterung über mehrere Zeilen in diesem Codeblock.</span><span class="sxs-lookup"><span data-stu-id="9d704-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="9d704-114">Der zweite Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="9d704-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="9d704-115">Beispiel 2: Ändern der Eigenschaften einer CORS-Regel für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="9d704-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="9d704-116">Der erste Befehl ruft die aktuellen CORS-Regeln für den BLOB-Typ mit dem Cmdlet **Get-AzureStorageCORSRule** ab.</span><span class="sxs-lookup"><span data-stu-id="9d704-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="9d704-117">Der Befehl speichert die Regeln in der $CorsRules-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="9d704-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="9d704-118">Mit dem zweiten und dritten Befehl wird die erste Regel in $CorsRules geändert.</span><span class="sxs-lookup"><span data-stu-id="9d704-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="9d704-119">Der endgültige Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="9d704-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="9d704-120">Durch die überarbeiteten Regeln werden die aktuellen CORS-Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d704-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="9d704-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d704-121">PARAMETERS</span></span>

### <span data-ttu-id="9d704-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9d704-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9d704-123">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="9d704-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9d704-124">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="9d704-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9d704-125">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9d704-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9d704-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9d704-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9d704-127">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="9d704-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9d704-128">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="9d704-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9d704-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9d704-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9d704-130">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="9d704-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9d704-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9d704-131">The default value is 10.</span></span>

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

### <span data-ttu-id="9d704-132">-Context</span><span class="sxs-lookup"><span data-stu-id="9d704-132">-Context</span></span>
<span data-ttu-id="9d704-133">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9d704-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9d704-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d704-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9d704-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="9d704-135">-CorsRules</span></span>
<span data-ttu-id="9d704-136">Gibt ein Array von CORS-Regeln an.</span><span class="sxs-lookup"><span data-stu-id="9d704-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="9d704-137">Sie können die vorhandenen Regeln mithilfe des Get-AzureStorageCORSRule-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="9d704-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="9d704-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d704-138">-PassThru</span></span>
<span data-ttu-id="9d704-139">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="9d704-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="9d704-140">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d704-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9d704-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9d704-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9d704-142">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9d704-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9d704-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9d704-143">-ServiceType</span></span>
<span data-ttu-id="9d704-144">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="9d704-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="9d704-145">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9d704-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d704-146">BLOB</span><span class="sxs-lookup"><span data-stu-id="9d704-146">Blob</span></span> 
- <span data-ttu-id="9d704-147">Tabelle</span><span class="sxs-lookup"><span data-stu-id="9d704-147">Table</span></span> 
- <span data-ttu-id="9d704-148">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="9d704-148">Queue</span></span> 
- <span data-ttu-id="9d704-149">Datei</span><span class="sxs-lookup"><span data-stu-id="9d704-149">File</span></span>

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

### <span data-ttu-id="9d704-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d704-150">CommonParameters</span></span>
<span data-ttu-id="9d704-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d704-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d704-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d704-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d704-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d704-153">INPUTS</span></span>

## <span data-ttu-id="9d704-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d704-154">OUTPUTS</span></span>

## <span data-ttu-id="9d704-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d704-155">NOTES</span></span>

## <span data-ttu-id="9d704-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d704-156">RELATED LINKS</span></span>

[<span data-ttu-id="9d704-157">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9d704-157">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="9d704-158">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9d704-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="9d704-159">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="9d704-159">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


