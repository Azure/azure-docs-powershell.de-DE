---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 2719f875d4a21f47b05b55b7880e4654237baafd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171276"
---
# <span data-ttu-id="a2faa-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="a2faa-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="a2faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2faa-102">SYNOPSIS</span></span>
<span data-ttu-id="a2faa-103">Exportprotokolle, die im angegebenen Zeitfenster die von diesem Abonnement vorgenommenen Api-Anforderungen anzeigen, um Einschränkungsaktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2faa-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="a2faa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a2faa-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2faa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2faa-105">DESCRIPTION</span></span>
<span data-ttu-id="a2faa-106">Exportiert statistische Daten über die Aufrufe des Abonnements an die Microsoft.Compute-API nach Erfolg, Fehler oder Gedrosselungsstatus in vordefinierten Zeitintervallen.</span><span class="sxs-lookup"><span data-stu-id="a2faa-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="a2faa-107">Die Protokolle können nach drei Parametern weiter gruppieren: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a2faa-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a2faa-108">Beachten Sie, dass dieses Cmdlet nur Protokolle des Compute Resource Provider sammelt. darüber hinaus sind daten zu den Ressourcentypen "Datenträger" und "Momentaufnahme" noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a2faa-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="a2faa-109">Eine Übersicht über die API-Einschränkung des Rechenressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="a2faa-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="a2faa-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a2faa-110">EXAMPLES</span></span>

### <span data-ttu-id="a2faa-111">Beispiel 1: Exportieren von nach Vorgangsnamen zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="a2faa-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="a2faa-112">Dieser Befehl speichert die aggregierten Zahlen der Microsoft.Compute-API-Aufrufe getrennt durch Erfolg, Fehler oder Gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="a2faa-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="a2faa-113">Beispiel 2: Exportieren von nach Anwendungs-ID zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="a2faa-113">Example 2: Export records aggregated by application id</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByApplicationId
```

<span data-ttu-id="a2faa-114">Dieser Befehl speichert die aggregierten Zahlen der Microsoft.Compute-API-Aufrufe getrennt durch Erfolg, Fehler oder Gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="a2faa-114">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by application id.</span></span> 

### <span data-ttu-id="a2faa-115">Beispiel 3: Exportieren von vom Benutzer-Agent zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="a2faa-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByUserAgent
```

<span data-ttu-id="a2faa-116">Dieser Befehl speichert die aggregierten Zahlen der Microsoft.Compute-API-Aufrufe getrennt durch Erfolg, Fehler oder Gedrosselt zwischen dem 2018-02-20T17:54:14 und dem 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert vom Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="a2faa-116">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span> 

## <span data-ttu-id="a2faa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2faa-117">PARAMETERS</span></span>

### <span data-ttu-id="a2faa-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2faa-118">-AsJob</span></span>
<span data-ttu-id="a2faa-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a2faa-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2faa-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a2faa-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="a2faa-121">SAS-URI des Protokollierungs-BLOB-Containers, in den die LogAnalytics-API Ausgabeprotokolle schreibt.</span><span class="sxs-lookup"><span data-stu-id="a2faa-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="a2faa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2faa-122">-DefaultProfile</span></span>
<span data-ttu-id="a2faa-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2faa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2faa-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="a2faa-124">-FromTime</span></span>
<span data-ttu-id="a2faa-125">Ab dem Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="a2faa-125">From time of the query</span></span>

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

### <span data-ttu-id="a2faa-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="a2faa-126">-GroupByApplicationId</span></span>
<span data-ttu-id="a2faa-127">Gruppieren Sie das Abfrageergebnis nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="a2faa-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="a2faa-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a2faa-128">-GroupByOperationName</span></span>
<span data-ttu-id="a2faa-129">Gruppieren Sie das Abfrageergebnis nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="a2faa-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a2faa-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a2faa-130">-GroupByResourceName</span></span>
<span data-ttu-id="a2faa-131">Gruppenabfrageergebnis nach Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="a2faa-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a2faa-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a2faa-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a2faa-133">Group query result by Throttle Policy applied.</span><span class="sxs-lookup"><span data-stu-id="a2faa-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a2faa-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="a2faa-134">-GroupByUserAgent</span></span>
<span data-ttu-id="a2faa-135">Gruppieren Sie das Abfrageergebnis nach UserAgent.</span><span class="sxs-lookup"><span data-stu-id="a2faa-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="a2faa-136">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="a2faa-136">-IntervalLength</span></span>
<span data-ttu-id="a2faa-137">Intervallwert in Minuten, der zum Erstellen von Protokollen für die Anrufrate von LogAnalytics verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2faa-137">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="a2faa-138">-Location</span><span class="sxs-lookup"><span data-stu-id="a2faa-138">-Location</span></span>
<span data-ttu-id="a2faa-139">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a2faa-139">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="a2faa-140">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a2faa-140">-NoWait</span></span>
<span data-ttu-id="a2faa-141">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="a2faa-141">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a2faa-142">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a2faa-142">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a2faa-143">-ToTime</span><span class="sxs-lookup"><span data-stu-id="a2faa-143">-ToTime</span></span>
<span data-ttu-id="a2faa-144">Bis zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="a2faa-144">To time of the query</span></span>

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

### <span data-ttu-id="a2faa-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2faa-145">-Confirm</span></span>
<span data-ttu-id="a2faa-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2faa-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2faa-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a2faa-147">-WhatIf</span></span>
<span data-ttu-id="a2faa-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2faa-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2faa-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2faa-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2faa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2faa-150">CommonParameters</span></span>
<span data-ttu-id="a2faa-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2faa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2faa-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2faa-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2faa-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a2faa-153">INPUTS</span></span>

### <span data-ttu-id="a2faa-154">System.String</span><span class="sxs-lookup"><span data-stu-id="a2faa-154">System.String</span></span>

## <span data-ttu-id="a2faa-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a2faa-155">OUTPUTS</span></span>

### <span data-ttu-id="a2faa-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a2faa-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a2faa-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a2faa-157">NOTES</span></span>

## <span data-ttu-id="a2faa-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a2faa-158">RELATED LINKS</span></span>
