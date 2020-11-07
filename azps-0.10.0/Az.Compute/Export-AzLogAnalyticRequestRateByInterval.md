---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: bbf275b08421265130da898b670b46c95b15c34c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844679"
---
# <span data-ttu-id="94650-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="94650-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="94650-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94650-102">SYNOPSIS</span></span>
<span data-ttu-id="94650-103">Exportieren von Protokollen, die API-Anforderungen dieses Abonnements im angegebenen Zeitfenster anzeigen, um Drosselungs Aktivitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="94650-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="94650-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94650-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval  [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins>
 [-GroupByOperationName] [-GroupByThrottlePolicy] [-GroupByResourceName] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94650-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94650-105">DESCRIPTION</span></span>
<span data-ttu-id="94650-106">Damit werden aggregierte Zahlen von Microsoft. Compute-API-aufrufen getrennt nach Erfolg, Fehler oder Drosselung in Zeitintervallen exportiert.</span><span class="sxs-lookup"><span data-stu-id="94650-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="94650-107">Die Protokolle können weiter nach drei Parametern gruppiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="94650-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="94650-108">Beachten Sie, dass dieses Cmdlet nur CRP-Protokolle sammelt.</span><span class="sxs-lookup"><span data-stu-id="94650-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="94650-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94650-109">EXAMPLES</span></span>

### <span data-ttu-id="94650-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="94650-110">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="94650-111">Dieser Befehl speichert die aggregierten Nummern von Microsoft. Compute-API-aufrufen, die durch Erfolg, Fehler oder gedrosselt zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 in dem angegebenen SAS-URI, aggregiert nach dem Vorgangsnamen, getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="94650-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="94650-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="94650-112">PARAMETERS</span></span>

### <span data-ttu-id="94650-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94650-113">-AsJob</span></span>
<span data-ttu-id="94650-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="94650-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94650-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="94650-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="94650-116">SAS-URI des Protokollierungs-BLOB-Containers, in den Ausgabeprotokolle von der LogAnalytics-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="94650-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94650-117">-DefaultProfile</span></span>
<span data-ttu-id="94650-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94650-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-119">-Ab-und-ab</span><span class="sxs-lookup"><span data-stu-id="94650-119">-FromTime</span></span>
<span data-ttu-id="94650-120">Ab Uhrzeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="94650-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="94650-121">-GroupByOperationName</span></span>
<span data-ttu-id="94650-122">Ergebnis der Gruppenabfrage nach Vorgangs Name</span><span class="sxs-lookup"><span data-stu-id="94650-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="94650-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="94650-123">-GroupByResourceName</span></span>
<span data-ttu-id="94650-124">Ergebnis der Gruppenabfrage nach Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="94650-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="94650-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="94650-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="94650-126">Gruppenabfrage Ergebnis nach angewendeter Drosselungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="94650-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="94650-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="94650-127">-IntervalLength</span></span>
<span data-ttu-id="94650-128">Intervallwert in Minuten, der zum Erstellen von LogAnalytics-Anruf Änderungsprotokollen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="94650-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases: 
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="94650-129">-Location</span></span>
<span data-ttu-id="94650-130">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="94650-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94650-131">-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="94650-131">-ToTime</span></span>
<span data-ttu-id="94650-132">Zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="94650-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94650-133">-Confirm</span></span>
<span data-ttu-id="94650-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94650-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94650-135">-WhatIf</span></span>
<span data-ttu-id="94650-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94650-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94650-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94650-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94650-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94650-138">CommonParameters</span></span>
<span data-ttu-id="94650-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94650-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94650-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94650-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94650-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94650-141">INPUTS</span></span>

### <span data-ttu-id="94650-142">System. String</span><span class="sxs-lookup"><span data-stu-id="94650-142">System.String</span></span>

## <span data-ttu-id="94650-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94650-143">OUTPUTS</span></span>

### <span data-ttu-id="94650-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="94650-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="94650-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="94650-145">NOTES</span></span>

## <span data-ttu-id="94650-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94650-146">RELATED LINKS</span></span>

