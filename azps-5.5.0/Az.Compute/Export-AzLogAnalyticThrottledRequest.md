---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 97f921fab8e258d5fbde44a6c148f61da2730999
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171275"
---
# <span data-ttu-id="772c3-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="772c3-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="772c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="772c3-102">SYNOPSIS</span></span>
<span data-ttu-id="772c3-103">Exportprotokolle, die im angegebenen Zeitfenster gedrosselte Gesamtanforderungen für dieses Abonnement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="772c3-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="772c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="772c3-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="772c3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="772c3-105">DESCRIPTION</span></span>
<span data-ttu-id="772c3-106">Dadurch wird die Gesamtanzahl der gedrosselten Microsoft.Compute-API-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="772c3-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="772c3-107">Die Protokolle können durch drei Optionen weiter aggregiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="772c3-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="772c3-108">Beachten Sie, dass dieses Cmdlet nur #A0 sammelt.</span><span class="sxs-lookup"><span data-stu-id="772c3-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="772c3-109">Eine Übersicht über die API-Einschränkung des Rechenressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="772c3-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="772c3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="772c3-110">EXAMPLES</span></span>

### <span data-ttu-id="772c3-111">Beispiel 1: Exportieren von nach Vorgangsnamen zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="772c3-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="772c3-112">Dieser Befehl speichert die gedrosselten Microsoft.Compute-API-Aufrufe zwischen dem 2018-02-20T17:54:14 und dem 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="772c3-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="772c3-113">Beispiel 2: Exportieren von nach Anwendungs-ID zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="772c3-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="772c3-114">Dieser Befehl speichert die gedrosselten Microsoft.Compute-API-Aufrufe zwischen dem 2018-02-20T17:54:14 und dem 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="772c3-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="772c3-115">Beispiel 3: Exportieren von vom Benutzer-Agent zusammengefassten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="772c3-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="772c3-116">Dieser Befehl speichert die gedrosselten Microsoft.Compute-API-Aufrufe zwischen dem 2018-02-20T17:54:14 und dem 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert vom Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="772c3-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="772c3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="772c3-117">PARAMETERS</span></span>

### <span data-ttu-id="772c3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="772c3-118">-AsJob</span></span>
<span data-ttu-id="772c3-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="772c3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="772c3-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="772c3-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="772c3-121">SAS-URI des Protokollierungs-BLOB-Containers, in den die LogAnalytics-API Ausgabeprotokolle schreibt.</span><span class="sxs-lookup"><span data-stu-id="772c3-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="772c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="772c3-122">-DefaultProfile</span></span>
<span data-ttu-id="772c3-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="772c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="772c3-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="772c3-124">-FromTime</span></span>
<span data-ttu-id="772c3-125">Ab dem Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="772c3-125">From time of the query</span></span>

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

### <span data-ttu-id="772c3-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="772c3-126">-GroupByApplicationId</span></span>
<span data-ttu-id="772c3-127">Gruppieren Sie das Abfrageergebnis nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="772c3-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="772c3-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="772c3-128">-GroupByOperationName</span></span>
<span data-ttu-id="772c3-129">Gruppieren Sie das Abfrageergebnis nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="772c3-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="772c3-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="772c3-130">-GroupByResourceName</span></span>
<span data-ttu-id="772c3-131">Gruppenabfrageergebnis nach Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="772c3-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="772c3-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="772c3-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="772c3-133">Group query result by Throttle Policy applied.</span><span class="sxs-lookup"><span data-stu-id="772c3-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="772c3-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="772c3-134">-GroupByUserAgent</span></span>
<span data-ttu-id="772c3-135">Gruppieren Sie das Abfrageergebnis nach UserAgent.</span><span class="sxs-lookup"><span data-stu-id="772c3-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="772c3-136">-Location</span><span class="sxs-lookup"><span data-stu-id="772c3-136">-Location</span></span>
<span data-ttu-id="772c3-137">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="772c3-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="772c3-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="772c3-138">-NoWait</span></span>
<span data-ttu-id="772c3-139">Der Vorgang wird gestartet und unmittelbar vor Abschluss des Vorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="772c3-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="772c3-140">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="772c3-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="772c3-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="772c3-141">-ToTime</span></span>
<span data-ttu-id="772c3-142">Bis zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="772c3-142">To time of the query</span></span>

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

### <span data-ttu-id="772c3-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="772c3-143">-Confirm</span></span>
<span data-ttu-id="772c3-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="772c3-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="772c3-145">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="772c3-145">-WhatIf</span></span>
<span data-ttu-id="772c3-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="772c3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="772c3-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="772c3-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="772c3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="772c3-148">CommonParameters</span></span>
<span data-ttu-id="772c3-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="772c3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="772c3-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="772c3-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="772c3-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="772c3-151">INPUTS</span></span>

### <span data-ttu-id="772c3-152">System.String</span><span class="sxs-lookup"><span data-stu-id="772c3-152">System.String</span></span>

## <span data-ttu-id="772c3-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="772c3-153">OUTPUTS</span></span>

### <span data-ttu-id="772c3-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="772c3-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="772c3-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="772c3-155">NOTES</span></span>

## <span data-ttu-id="772c3-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="772c3-156">RELATED LINKS</span></span>
