---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303315"
---
# <span data-ttu-id="fdfa5-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fdfa5-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="fdfa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdfa5-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfa5-103">Legt die REGELN des Typs "CORS" für einen Speicherdiensttyp fest.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="fdfa5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdfa5-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fdfa5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdfa5-105">DESCRIPTION</span></span>
<span data-ttu-id="fdfa5-106">Das **Cmdlet Set-AzStorageCORSRule** legt die REGELN für die cross origin-übergreifende Ressourcenfreigabe (CROSSS) für einen Typ von Azure Storage Service fest.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="fdfa5-107">Die Speicherdienste für dieses Cmdlet sind BLOB, Table, Queue und File.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="fdfa5-108">Dieses Cmdlet überschreibt die vorhandenen Regeln.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="fdfa5-109">Um die aktuellen Regeln zu sehen, verwenden Sie das Get-AzStorageCORSRule Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="fdfa5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdfa5-110">EXAMPLES</span></span>

### <span data-ttu-id="fdfa5-111">Beispiel 1: Zuweisen von KORS-Regeln zum BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="fdfa5-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="fdfa5-112">Der erste Befehl weist der Variablen ein Array von Regeln $CorsRules zu.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="fdfa5-113">Dieser Befehl verwendet einen Standard, der sich über mehrere Zeilen in diesem Codeblock erstreckt.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="fdfa5-114">Der zweite Befehl weist die Regeln in $CorsRules dem Blob-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="fdfa5-115">Beispiel 2: Ändern der Eigenschaften einer CORS-Regel für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="fdfa5-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="fdfa5-116">Der erste Befehl ruft mithilfe des Cmdlets **"Get-AzStorageCORSRule"** die aktuellen KORS-Regeln für den Blob-Typ ab.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="fdfa5-117">Der Befehl speichert die Regeln in der $CorsRules Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="fdfa5-118">Der zweite und dritte Befehl ändern die erste Regel in $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="fdfa5-119">Der letzte Befehl weist die Regeln in $CorsRules dem Blob-Diensttyp zu.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="fdfa5-120">Die überarbeiteten Regeln überschreiben die aktuellen KORS-Regeln.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="fdfa5-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdfa5-121">PARAMETERS</span></span>

### <span data-ttu-id="fdfa5-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdfa5-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fdfa5-123">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fdfa5-124">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fdfa5-125">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fdfa5-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fdfa5-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fdfa5-127">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fdfa5-128">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fdfa5-129">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fdfa5-130">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fdfa5-131">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-131">The default value is 10.</span></span>

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

### <span data-ttu-id="fdfa5-132">-Context</span><span class="sxs-lookup"><span data-stu-id="fdfa5-132">-Context</span></span>
<span data-ttu-id="fdfa5-133">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="fdfa5-134">Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fdfa5-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="fdfa5-135">-CorsRules</span></span>
<span data-ttu-id="fdfa5-136">Gibt ein Array von KORS-Regeln an.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="fdfa5-137">Sie können die vorhandenen Regeln mithilfe des cmdlets Get-AzStorageCORSRule abrufen.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="fdfa5-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfa5-138">-DefaultProfile</span></span>
<span data-ttu-id="fdfa5-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfa5-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdfa5-140">-PassThru</span></span>
<span data-ttu-id="fdfa5-141">Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="fdfa5-142">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fdfa5-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fdfa5-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fdfa5-144">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="fdfa5-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="fdfa5-145">-ServiceType</span></span>
<span data-ttu-id="fdfa5-146">Gibt den Azure Storage-Diensttyp an, dem dieses Cmdlet Regeln zugibt.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="fdfa5-147">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="fdfa5-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fdfa5-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="fdfa5-148">Blob</span></span> 
- <span data-ttu-id="fdfa5-149">Tabelle</span><span class="sxs-lookup"><span data-stu-id="fdfa5-149">Table</span></span> 
- <span data-ttu-id="fdfa5-150">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="fdfa5-150">Queue</span></span> 
- <span data-ttu-id="fdfa5-151">Datei</span><span class="sxs-lookup"><span data-stu-id="fdfa5-151">File</span></span>

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

### <span data-ttu-id="fdfa5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfa5-152">CommonParameters</span></span>
<span data-ttu-id="fdfa5-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdfa5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfa5-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdfa5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfa5-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdfa5-155">INPUTS</span></span>

### <span data-ttu-id="fdfa5-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdfa5-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fdfa5-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdfa5-157">OUTPUTS</span></span>

### <span data-ttu-id="fdfa5-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="fdfa5-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="fdfa5-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fdfa5-159">NOTES</span></span>

## <span data-ttu-id="fdfa5-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fdfa5-160">RELATED LINKS</span></span>

[<span data-ttu-id="fdfa5-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fdfa5-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="fdfa5-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fdfa5-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fdfa5-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="fdfa5-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


