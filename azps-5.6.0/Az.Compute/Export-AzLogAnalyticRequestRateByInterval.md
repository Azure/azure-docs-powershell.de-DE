---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: feae2282f6b989b8d595b2a51cd147975e689174
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927320"
---
# <span data-ttu-id="4ea1d-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="4ea1d-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="4ea1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea1d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea1d-103">Exportieren Sie Protokolle, die api-Anforderungen anzeigen, die von diesem Abonnement im angegebenen Zeitfenster ausgeführt werden, um Einschränkungsaktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="4ea1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ea1d-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ea1d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ea1d-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea1d-106">Exportiert statistische Daten zu den Aufrufen des Abonnements an die Microsoft.Compute-API nach Erfolgs-, Fehler- oder Einschränkungsstatus in vordefinierten Zeitintervallen.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="4ea1d-107">Die Protokolle können nach fünf Parametern weiter gruppieren: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent oder GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-107">The logs can be further grouped by five parameters: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="4ea1d-108">Beachten Sie, dass dieses Cmdlet nur Protokolle des Ressourcenanbieters berechnen sammelt. Darüber hinaus stehen noch keine Daten zu den Ressourcentypen Datenträger und Momentaufnahme zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="4ea1d-109">Eine Übersicht über die API-Einschränkung des Computeressourcenanbieters finden Sie unter https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="4ea1d-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="4ea1d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ea1d-110">EXAMPLES</span></span>

### <span data-ttu-id="4ea1d-111">Beispiel 1: Exportieren von Nach Vorgangsnamen aggregierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="4ea1d-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             operationName   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <operationName> 10            10                 0
2/21/2018  7:30:00 PM <operationName> 8             8                  0
2/21/2018  9:00:00 PM <operationName> 9             9                  0

```

<span data-ttu-id="4ea1d-112">Mit diesem Befehl werden die aggregierten Nummern von Microsoft.Compute-API-Aufrufen, getrennt durch Erfolg, Fehler oder Gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname, speichert.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="4ea1d-113">Beispiel 2: Exportieren von Datensätzen, aggregiert nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="4ea1d-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId

This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             clientApplicationId   TotalRequests SuccessfulRequests ThrottledRequests
---------             -------------------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <clientApplicationId> 10            10                 0
2/21/2018  7:30:00 PM <clientApplicationId> 8             8                  0
2/21/2018  9:00:00 PM <clientApplicationId> 9             9                  0

```

<span data-ttu-id="4ea1d-114">Mit diesem Befehl werden die aggregierten Nummern von Microsoft.Compute-API-Aufrufen, getrennt durch Erfolg, Fehler oder Gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Anwendungs-ID, speichert.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="4ea1d-115">Beispiel 3: Exportieren von nach Benutzermitarbeitern aggregierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="4ea1d-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
This command downloads a .csv file to the provided container. The format of the file is:

TIMESTAMP             userAgent   TotalRequests SuccessfulRequests ThrottledRequests
---------             ---------   ------------- ------------------ -----------------
2/21/2018  7:00:00 PM <userAgent> 10            10                 0
2/21/2018  7:30:00 PM <userAgent> 8             8                  0
2/21/2018  9:00:00 PM <userAgent> 9             9                  0

```

<span data-ttu-id="4ea1d-116">Dieser Befehl speichert die aggregierten Nummern von Microsoft.Compute-API-Aufrufen, getrennt durch Erfolg, Fehler oder Gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert vom Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="4ea1d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4ea1d-117">PARAMETERS</span></span>

### <span data-ttu-id="4ea1d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ea1d-118">-AsJob</span></span>
<span data-ttu-id="4ea1d-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4ea1d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ea1d-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="4ea1d-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="4ea1d-121">SAS Uri des Protokollierungsblobcontainers, in den die LogAnalytics-Api Ausgabeprotokolle schreibt.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea1d-122">-DefaultProfile</span></span>
<span data-ttu-id="4ea1d-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="4ea1d-124">-FromTime</span></span>
<span data-ttu-id="4ea1d-125">Ab dem Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="4ea1d-125">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="4ea1d-126">-GroupByApplicationId</span></span>
<span data-ttu-id="4ea1d-127">Gruppieren des Abfrageergebnisses nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="4ea1d-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="4ea1d-128">-GroupByOperationName</span></span>
<span data-ttu-id="4ea1d-129">Gruppieren des Abfrageergebnisses nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="4ea1d-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="4ea1d-130">-GroupByResourceName</span></span>
<span data-ttu-id="4ea1d-131">Gruppieren des Abfrageergebnisses nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="4ea1d-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="4ea1d-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="4ea1d-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="4ea1d-133">Gruppieren des Abfrageergebnisses nach angewendeter Einschränkungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="4ea1d-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="4ea1d-134">-GroupByUserAgent</span></span>
<span data-ttu-id="4ea1d-135">Gruppieren des Abfrageergebnisses nach UserAgent.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="4ea1d-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="4ea1d-136">-IntervalLength</span></span>
<span data-ttu-id="4ea1d-137">Intervallwert in Minuten, die zum Erstellen von LogAnalytics-Anruffrequenzprotokollen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-138">-Location</span><span class="sxs-lookup"><span data-stu-id="4ea1d-138">-Location</span></span>
<span data-ttu-id="4ea1d-139">Der Speicherort, an dem die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-139">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ea1d-140">-NoWait</span></span>
<span data-ttu-id="4ea1d-141">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="4ea1d-142">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="4ea1d-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="4ea1d-143">-ToTime</span></span>
<span data-ttu-id="4ea1d-144">Bis zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="4ea1d-144">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4ea1d-145">-Confirm</span></span>
<span data-ttu-id="4ea1d-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ea1d-147">-WhatIf</span></span>
<span data-ttu-id="4ea1d-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ea1d-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ea1d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea1d-150">CommonParameters</span></span>
<span data-ttu-id="4ea1d-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea1d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea1d-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ea1d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea1d-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ea1d-153">INPUTS</span></span>

### <span data-ttu-id="4ea1d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4ea1d-154">System.String</span></span>

## <span data-ttu-id="4ea1d-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ea1d-155">OUTPUTS</span></span>

### <span data-ttu-id="4ea1d-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="4ea1d-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="4ea1d-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4ea1d-157">NOTES</span></span>

## <span data-ttu-id="4ea1d-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4ea1d-158">RELATED LINKS</span></span>
