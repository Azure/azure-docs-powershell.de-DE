---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 79bf599b22796181c2f433f186e0e4bde8094773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470928"
---
# <span data-ttu-id="5e134-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5e134-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="5e134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e134-102">SYNOPSIS</span></span>
<span data-ttu-id="5e134-103">Exportprotokolle, die im angegebenen Zeitfenster gedrosselte Gesamtanforderungen für dieses Abonnement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5e134-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="5e134-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e134-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e134-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e134-105">DESCRIPTION</span></span>
<span data-ttu-id="5e134-106">Dadurch wird die Gesamtzahl der gedrosselten Microsoft.Compute-API-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="5e134-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="5e134-107">Die Protokolle können durch drei Optionen weiter aggregiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="5e134-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="5e134-108">Beachten Sie, dass dieses Cmdlet nur #A0 sammelt.</span><span class="sxs-lookup"><span data-stu-id="5e134-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="5e134-109">Eine Übersicht über die API-Einschränkung des Rechenressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="5e134-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="5e134-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e134-110">EXAMPLES</span></span>

### <span data-ttu-id="5e134-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e134-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="5e134-112">Dieser Befehl speichert die gedrosselten Microsoft.Compute-API-Aufrufe zwischen dem 2018-02-20T17:54:14 und dem 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="5e134-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="5e134-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e134-113">PARAMETERS</span></span>

### <span data-ttu-id="5e134-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e134-114">-AsJob</span></span>
<span data-ttu-id="5e134-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5e134-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e134-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5e134-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="5e134-117">SAS-URI des Protokollierungs-BLOB-Containers, in den die LogAnalytics-API Ausgabeprotokolle schreibt.</span><span class="sxs-lookup"><span data-stu-id="5e134-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="5e134-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e134-118">-DefaultProfile</span></span>
<span data-ttu-id="5e134-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e134-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e134-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="5e134-120">-FromTime</span></span>
<span data-ttu-id="5e134-121">Ab dem Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="5e134-121">From time of the query</span></span>

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

### <span data-ttu-id="5e134-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="5e134-122">-GroupByOperationName</span></span>
<span data-ttu-id="5e134-123">Gruppieren Sie das Abfrageergebnis nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="5e134-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="5e134-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="5e134-124">-GroupByResourceName</span></span>
<span data-ttu-id="5e134-125">Gruppenabfrageergebnis nach Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5e134-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="5e134-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="5e134-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="5e134-127">Gruppenabfrageergebnis nach angewendeter Einschränkungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5e134-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="5e134-128">-Location</span><span class="sxs-lookup"><span data-stu-id="5e134-128">-Location</span></span>
<span data-ttu-id="5e134-129">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="5e134-129">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="5e134-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5e134-130">-NoWait</span></span>
<span data-ttu-id="5e134-131">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="5e134-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5e134-132">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5e134-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5e134-133">-ToTime</span><span class="sxs-lookup"><span data-stu-id="5e134-133">-ToTime</span></span>
<span data-ttu-id="5e134-134">Bis zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="5e134-134">To time of the query</span></span>

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

### <span data-ttu-id="5e134-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e134-135">-Confirm</span></span>
<span data-ttu-id="5e134-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e134-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e134-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5e134-137">-WhatIf</span></span>
<span data-ttu-id="5e134-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e134-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e134-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e134-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e134-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e134-140">CommonParameters</span></span>
<span data-ttu-id="5e134-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e134-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e134-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e134-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e134-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e134-143">INPUTS</span></span>

### <span data-ttu-id="5e134-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5e134-144">System.String</span></span>

## <span data-ttu-id="5e134-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e134-145">OUTPUTS</span></span>

### <span data-ttu-id="5e134-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="5e134-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="5e134-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5e134-147">NOTES</span></span>

## <span data-ttu-id="5e134-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5e134-148">RELATED LINKS</span></span>
