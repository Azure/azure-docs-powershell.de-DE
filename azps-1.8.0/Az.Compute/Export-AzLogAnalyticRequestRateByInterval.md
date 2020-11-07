---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: f6bef7bc90f63ec5a421c0b78a87ea5ec8618053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661571"
---
# <span data-ttu-id="2cc6c-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="2cc6c-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="2cc6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc6c-103">Exportieren von Protokollen, die API-Anforderungen dieses Abonnements im angegebenen Zeitfenster anzeigen, um Drosselungs Aktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="2cc6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cc6c-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cc6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cc6c-105">DESCRIPTION</span></span>
<span data-ttu-id="2cc6c-106">Exportiert statistische Daten über die Anrufe des Abonnements in die Microsoft. Compute-API nach Erfolg, Fehler oder gedrosselten Status in vordefinierten Zeitintervallen.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="2cc6c-107">Die Protokolle können weiter nach drei Parametern gruppiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="2cc6c-108">Beachten Sie, dass dieses Cmdlet nur Protokolle des Compute-Ressourcenanbieters sammelt; Darüber hinaus sind Daten zu den Datenträger-und Snapshot-Ressourcentypen noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="2cc6c-109">Eine Übersicht über die API-Drosselung des Compute-Ressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="2cc6c-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="2cc6c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cc6c-110">EXAMPLES</span></span>

### <span data-ttu-id="2cc6c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cc6c-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="2cc6c-112">Dieser Befehl speichert die aggregierten Nummern von Microsoft. Compute-API-aufrufen, die durch Erfolg, Fehler oder gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 in dem angegebenen SAS-URI, aggregiert nach dem Vorgangsnamen, getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="2cc6c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc6c-113">PARAMETERS</span></span>

### <span data-ttu-id="2cc6c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cc6c-114">-AsJob</span></span>
<span data-ttu-id="2cc6c-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2cc6c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cc6c-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="2cc6c-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="2cc6c-117">SAS-URI des Protokollierungs-BLOB-Containers, in den Ausgabeprotokolle von der LogAnalytics-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="2cc6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc6c-118">-DefaultProfile</span></span>
<span data-ttu-id="2cc6c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc6c-120">-Ab-und-ab</span><span class="sxs-lookup"><span data-stu-id="2cc6c-120">-FromTime</span></span>
<span data-ttu-id="2cc6c-121">Ab Uhrzeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="2cc6c-121">From time of the query</span></span>

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

### <span data-ttu-id="2cc6c-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="2cc6c-122">-GroupByOperationName</span></span>
<span data-ttu-id="2cc6c-123">Ergebnis der Gruppenabfrage nach Vorgangs Name</span><span class="sxs-lookup"><span data-stu-id="2cc6c-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="2cc6c-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="2cc6c-124">-GroupByResourceName</span></span>
<span data-ttu-id="2cc6c-125">Ergebnis der Gruppenabfrage nach Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="2cc6c-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="2cc6c-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="2cc6c-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="2cc6c-127">Gruppenabfrage Ergebnis nach angewendeter Drosselungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2cc6c-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="2cc6c-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="2cc6c-128">-IntervalLength</span></span>
<span data-ttu-id="2cc6c-129">Intervallwert in Minuten, der zum Erstellen von LogAnalytics-Anruf Änderungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

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

### <span data-ttu-id="2cc6c-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="2cc6c-130">-Location</span></span>
<span data-ttu-id="2cc6c-131">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-131">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="2cc6c-132">-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="2cc6c-132">-ToTime</span></span>
<span data-ttu-id="2cc6c-133">Zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="2cc6c-133">To time of the query</span></span>

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

### <span data-ttu-id="2cc6c-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cc6c-134">-Confirm</span></span>
<span data-ttu-id="2cc6c-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cc6c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cc6c-136">-WhatIf</span></span>
<span data-ttu-id="2cc6c-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cc6c-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cc6c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc6c-139">CommonParameters</span></span>
<span data-ttu-id="2cc6c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc6c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc6c-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc6c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc6c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cc6c-142">INPUTS</span></span>

### <span data-ttu-id="2cc6c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2cc6c-143">System.String</span></span>

## <span data-ttu-id="2cc6c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cc6c-144">OUTPUTS</span></span>

### <span data-ttu-id="2cc6c-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="2cc6c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="2cc6c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cc6c-146">NOTES</span></span>

## <span data-ttu-id="2cc6c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cc6c-147">RELATED LINKS</span></span>
