---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004857"
---
# <span data-ttu-id="a635a-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="a635a-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="a635a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a635a-102">SYNOPSIS</span></span>
<span data-ttu-id="a635a-103">Exportieren von Protokollen, die API-Anforderungen dieses Abonnements im angegebenen Zeitfenster anzeigen, um Drosselungs Aktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a635a-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="a635a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a635a-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a635a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a635a-105">DESCRIPTION</span></span>
<span data-ttu-id="a635a-106">Exportiert statistische Daten über die Anrufe des Abonnements in die Microsoft. Compute-API nach Erfolg, Fehler oder gedrosselten Status in vordefinierten Zeitintervallen.</span><span class="sxs-lookup"><span data-stu-id="a635a-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="a635a-107">Die Protokolle können weiter nach drei Parametern gruppiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="a635a-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="a635a-108">Beachten Sie, dass dieses Cmdlet nur Protokolle des Compute-Ressourcenanbieters sammelt; Darüber hinaus sind Daten zu den Datenträger-und Snapshot-Ressourcentypen noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a635a-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="a635a-109">Eine Übersicht über die API-Drosselung des Compute-Ressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="a635a-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="a635a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a635a-110">EXAMPLES</span></span>

### <span data-ttu-id="a635a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a635a-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="a635a-112">Dieser Befehl speichert die aggregierten Nummern von Microsoft. Compute-API-aufrufen, die durch Erfolg, Fehler oder gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 in dem angegebenen SAS-URI, aggregiert nach dem Vorgangsnamen, getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="a635a-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="a635a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a635a-113">PARAMETERS</span></span>

### <span data-ttu-id="a635a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a635a-114">-AsJob</span></span>
<span data-ttu-id="a635a-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a635a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a635a-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a635a-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="a635a-117">SAS-URI des Protokollierungs-BLOB-Containers, in den Ausgabeprotokolle von der LogAnalytics-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a635a-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="a635a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a635a-118">-DefaultProfile</span></span>
<span data-ttu-id="a635a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a635a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a635a-120">-Ab-und-ab</span><span class="sxs-lookup"><span data-stu-id="a635a-120">-FromTime</span></span>
<span data-ttu-id="a635a-121">Ab Uhrzeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="a635a-121">From time of the query</span></span>

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

### <span data-ttu-id="a635a-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="a635a-122">-GroupByOperationName</span></span>
<span data-ttu-id="a635a-123">Ergebnis der Gruppenabfrage nach Vorgangs Name</span><span class="sxs-lookup"><span data-stu-id="a635a-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="a635a-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="a635a-124">-GroupByResourceName</span></span>
<span data-ttu-id="a635a-125">Ergebnis der Gruppenabfrage nach Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="a635a-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="a635a-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="a635a-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="a635a-127">Gruppenabfrage Ergebnis nach angewendeter Drosselungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="a635a-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="a635a-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="a635a-128">-IntervalLength</span></span>
<span data-ttu-id="a635a-129">Intervallwert in Minuten, der zum Erstellen von LogAnalytics-Anruf Änderungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a635a-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="a635a-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="a635a-130">-Location</span></span>
<span data-ttu-id="a635a-131">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="a635a-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="a635a-132">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a635a-132">-NoWait</span></span>
<span data-ttu-id="a635a-133">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="a635a-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a635a-134">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a635a-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a635a-135">-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="a635a-135">-ToTime</span></span>
<span data-ttu-id="a635a-136">Zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="a635a-136">To time of the query</span></span>

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

### <span data-ttu-id="a635a-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a635a-137">-Confirm</span></span>
<span data-ttu-id="a635a-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a635a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a635a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a635a-139">-WhatIf</span></span>
<span data-ttu-id="a635a-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a635a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a635a-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a635a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a635a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a635a-142">CommonParameters</span></span>
<span data-ttu-id="a635a-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a635a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a635a-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a635a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a635a-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a635a-145">INPUTS</span></span>

### <span data-ttu-id="a635a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a635a-146">System.String</span></span>

## <span data-ttu-id="a635a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a635a-147">OUTPUTS</span></span>

### <span data-ttu-id="a635a-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="a635a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="a635a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a635a-149">NOTES</span></span>

## <span data-ttu-id="a635a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a635a-150">RELATED LINKS</span></span>
