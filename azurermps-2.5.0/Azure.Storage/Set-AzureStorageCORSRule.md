---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragecorsrule
schema: 2.0.0
ms.openlocfilehash: b60e13c9d491fddb867dd5d6884cffaa13798c70
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848360"
---
# <span data-ttu-id="169de-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="169de-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="169de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="169de-102">SYNOPSIS</span></span>
<span data-ttu-id="169de-103">Legt die CORS-Regeln für einen Typ von Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="169de-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="169de-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="169de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="169de-105">DESCRIPTION</span></span>
<span data-ttu-id="169de-106">Das Cmdlet " **Set-AzureStorageCORSRule** " legt die Richtlinien für die Cross-Origin-Ressourcenfreigabe (CORS) für einen Typ von Azure-Speicherdienst fest.</span><span class="sxs-lookup"><span data-stu-id="169de-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="169de-107">Die Typen von Speicherdiensten für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="169de-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="169de-108">Mit diesem Cmdlet werden die vorhandenen Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="169de-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="169de-109">Verwenden Sie das Cmdlet Get-AzureStorageCORSRule, um die aktuellen Regeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="169de-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="169de-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="169de-110">EXAMPLES</span></span>

### <span data-ttu-id="169de-111">Beispiel 1: Zuweisen von CORS-Regeln zum BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="169de-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="169de-112">Der erste Befehl weist der $CorsRules Variablen ein Array von Regeln zu.</span><span class="sxs-lookup"><span data-stu-id="169de-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="169de-113">Dieser Befehl verwendet die Standarderweiterung über mehrere Zeilen in diesem Codeblock.</span><span class="sxs-lookup"><span data-stu-id="169de-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="169de-114">Der zweite Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="169de-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="169de-115">Beispiel 2: Ändern der Eigenschaften einer CORS-Regel für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="169de-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="169de-116">Der erste Befehl ruft die aktuellen CORS-Regeln für den BLOB-Typ mit dem Cmdlet **Get-AzureStorageCORSRule** ab.</span><span class="sxs-lookup"><span data-stu-id="169de-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="169de-117">Der Befehl speichert die Regeln in der $CorsRules-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="169de-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="169de-118">Mit dem zweiten und dritten Befehl wird die erste Regel in $CorsRules geändert.</span><span class="sxs-lookup"><span data-stu-id="169de-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="169de-119">Der endgültige Befehl weist die Regeln in $CorsRules dem BLOB-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="169de-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="169de-120">Durch die überarbeiteten Regeln werden die aktuellen CORS-Regeln überschrieben.</span><span class="sxs-lookup"><span data-stu-id="169de-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="169de-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="169de-121">PARAMETERS</span></span>

### <span data-ttu-id="169de-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="169de-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="169de-123">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="169de-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="169de-124">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="169de-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="169de-125">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="169de-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="169de-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="169de-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="169de-127">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="169de-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="169de-128">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="169de-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="169de-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="169de-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="169de-130">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="169de-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="169de-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="169de-131">The default value is 10.</span></span>

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

### <span data-ttu-id="169de-132">-Context</span><span class="sxs-lookup"><span data-stu-id="169de-132">-Context</span></span>
<span data-ttu-id="169de-133">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="169de-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="169de-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169de-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="169de-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="169de-135">-CorsRules</span></span>
<span data-ttu-id="169de-136">Gibt ein Array von CORS-Regeln an.</span><span class="sxs-lookup"><span data-stu-id="169de-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="169de-137">Sie können die vorhandenen Regeln mithilfe des Get-AzureStorageCORSRule-Cmdlets abrufen.</span><span class="sxs-lookup"><span data-stu-id="169de-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="169de-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169de-138">-DefaultProfile</span></span>
<span data-ttu-id="169de-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="169de-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169de-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="169de-140">-PassThru</span></span>
<span data-ttu-id="169de-141">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="169de-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="169de-142">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="169de-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="169de-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="169de-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="169de-144">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="169de-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="169de-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="169de-145">-ServiceType</span></span>
<span data-ttu-id="169de-146">Gibt den Typ des Azure-Speicher Diensts an, für den dieses Cmdlet Regeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="169de-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="169de-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="169de-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="169de-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="169de-148">Blob</span></span> 
- <span data-ttu-id="169de-149">Tabelle</span><span class="sxs-lookup"><span data-stu-id="169de-149">Table</span></span> 
- <span data-ttu-id="169de-150">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="169de-150">Queue</span></span> 
- <span data-ttu-id="169de-151">Datei</span><span class="sxs-lookup"><span data-stu-id="169de-151">File</span></span>

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

### <span data-ttu-id="169de-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169de-152">CommonParameters</span></span>
<span data-ttu-id="169de-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169de-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169de-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169de-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169de-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="169de-155">INPUTS</span></span>

### <span data-ttu-id="169de-156">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="169de-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="169de-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="169de-157">OUTPUTS</span></span>

### <span data-ttu-id="169de-158">Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="169de-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="169de-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="169de-159">NOTES</span></span>

## <span data-ttu-id="169de-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="169de-160">RELATED LINKS</span></span>

[<span data-ttu-id="169de-161">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="169de-161">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="169de-162">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="169de-162">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="169de-163">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="169de-163">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


