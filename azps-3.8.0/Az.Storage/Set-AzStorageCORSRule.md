---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003261"
---
# <span data-ttu-id="e7791-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e7791-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="e7791-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7791-102">SYNOPSIS</span></span>
<span data-ttu-id="e7791-103">Legt die CORS-Regeln für einen Typ von Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="e7791-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="e7791-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7791-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e7791-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7791-105">DESCRIPTION</span></span>
<span data-ttu-id="e7791-106">Das Cmdlet " **Set-AzStorageCORSRule** " legt die Richtlinien für die Cross-Origin-Ressourcenfreigabe (CORS) für einen Typ von Azure-Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="e7791-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="e7791-107">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="e7791-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="e7791-108">Mit diesem Cmdlet werden die vorhandenen Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7791-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="e7791-109">Verwenden Sie das Cmdlet Get-AzStorageCORSRule, um die aktuellen Regeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7791-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="e7791-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7791-110">EXAMPLES</span></span>

### <span data-ttu-id="e7791-111">Beispiel 1: Zuweisen von CORS-Regeln zum BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="e7791-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e7791-112">Der erste Befehl weist der $CorsRules Variablen ein Array von Regeln zu.</span><span class="sxs-lookup"><span data-stu-id="e7791-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="e7791-113">Dieser Befehl verwendet die Standarderweiterung über mehrere Zeilen in diesem Codeblock.</span><span class="sxs-lookup"><span data-stu-id="e7791-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="e7791-114">Der zweite Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="e7791-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="e7791-115">Beispiel 2: Ändern der Eigenschaften einer CORS-Regel für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="e7791-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e7791-116">Der erste Befehl ruft die aktuellen CORS-Regeln für den BLOB-Typ mit dem Cmdlet **Get-AzStorageCORSRule** ab.</span><span class="sxs-lookup"><span data-stu-id="e7791-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="e7791-117">Der Befehl speichert die Regeln in der $CorsRules-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="e7791-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="e7791-118">Mit dem zweiten und dritten Befehl wird die erste Regel in $CorsRules geändert.</span><span class="sxs-lookup"><span data-stu-id="e7791-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="e7791-119">Der endgültige Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="e7791-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="e7791-120">Durch die überarbeiteten Regeln werden die aktuellen CORS-Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7791-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="e7791-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7791-121">PARAMETERS</span></span>

### <span data-ttu-id="e7791-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7791-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e7791-123">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="e7791-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e7791-124">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="e7791-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e7791-125">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e7791-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e7791-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e7791-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e7791-127">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="e7791-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e7791-128">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="e7791-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e7791-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e7791-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e7791-130">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e7791-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e7791-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="e7791-131">The default value is 10.</span></span>

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

### <span data-ttu-id="e7791-132">-Context</span><span class="sxs-lookup"><span data-stu-id="e7791-132">-Context</span></span>
<span data-ttu-id="e7791-133">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="e7791-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e7791-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7791-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e7791-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="e7791-135">-CorsRules</span></span>
<span data-ttu-id="e7791-136">Gibt ein Array von CORS-Regeln an.</span><span class="sxs-lookup"><span data-stu-id="e7791-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="e7791-137">Sie können die vorhandenen Regeln mithilfe des Get-AzStorageCORSRule-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="e7791-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7791-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7791-138">-DefaultProfile</span></span>
<span data-ttu-id="e7791-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7791-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7791-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7791-140">-PassThru</span></span>
<span data-ttu-id="e7791-141">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="e7791-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="e7791-142">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e7791-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e7791-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e7791-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e7791-144">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="e7791-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e7791-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e7791-145">-ServiceType</span></span>
<span data-ttu-id="e7791-146">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="e7791-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="e7791-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e7791-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7791-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="e7791-148">Blob</span></span> 
- <span data-ttu-id="e7791-149">Tabelle</span><span class="sxs-lookup"><span data-stu-id="e7791-149">Table</span></span> 
- <span data-ttu-id="e7791-150">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e7791-150">Queue</span></span> 
- <span data-ttu-id="e7791-151">Datei</span><span class="sxs-lookup"><span data-stu-id="e7791-151">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7791-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7791-152">CommonParameters</span></span>
<span data-ttu-id="e7791-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7791-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7791-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7791-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7791-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7791-155">INPUTS</span></span>

### <span data-ttu-id="e7791-156">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e7791-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e7791-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7791-157">OUTPUTS</span></span>

### <span data-ttu-id="e7791-158">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="e7791-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="e7791-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7791-159">NOTES</span></span>

## <span data-ttu-id="e7791-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7791-160">RELATED LINKS</span></span>

[<span data-ttu-id="e7791-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e7791-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="e7791-162">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e7791-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e7791-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e7791-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


