---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/export-azloganalyticthrottledrequest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticThrottledRequest.md
ms.openlocfilehash: 02d78a36bcd2afc6eef037a0b043c5db89d37f0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927315"
---
# <span data-ttu-id="12f7f-101">Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="12f7f-101">Export-AzLogAnalyticThrottledRequest</span></span>

## <span data-ttu-id="12f7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="12f7f-103">Exportieren Sie Protokolle, die im angegebenen Zeitfenster gedrosselte Api-Anforderungen für dieses Abonnement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="12f7f-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

## <span data-ttu-id="12f7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12f7f-104">SYNTAX</span></span>

```
Export-AzLogAnalyticThrottledRequest [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-GroupByOperationName] [-GroupByResourceName] [-GroupByThrottlePolicy]
 [-GroupByApplicationId] [-GroupByUserAgent] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12f7f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="12f7f-106">Dadurch wird die Gesamtanzahl der gedrosselten Microsoft.Compute-API-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="12f7f-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="12f7f-107">Die Protokolle können durch fünf Optionen weiter aggregiert werden: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent oder GroupByApplicationId.</span><span class="sxs-lookup"><span data-stu-id="12f7f-107">The logs can be further aggregated by five options: GroupByOperationName, GroupByThrottlePolicy, GroupByResourceName, GroupByUserAgent, or GroupByApplicationId.</span></span>
<span data-ttu-id="12f7f-108">Beachten Sie, dass dieses Cmdlet nur #A0 sammelt.</span><span class="sxs-lookup"><span data-stu-id="12f7f-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="12f7f-109">Eine Übersicht über die API-Einschränkung des Computeressourcenanbieters finden Sie unter https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="12f7f-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="12f7f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12f7f-110">EXAMPLES</span></span>

### <span data-ttu-id="12f7f-111">Beispiel 1: Exportieren von Nach Vorgangsnamen aggregierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="12f7f-111">Example 1: Export records aggregated by operation name</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="12f7f-112">Dieser Befehl speichert die insgesamt gedrosselten Microsoft.Compute-API-Aufrufe zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="12f7f-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

### <span data-ttu-id="12f7f-113">Beispiel 2: Exportieren von Datensätzen, aggregiert nach Anwendungs-ID</span><span class="sxs-lookup"><span data-stu-id="12f7f-113">Example 2: Export records aggregated by applicaiton id</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByApplicationId
```

<span data-ttu-id="12f7f-114">Dieser Befehl speichert die insgesamt gedrosselten Microsoft.Compute-API-Aufrufe zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="12f7f-114">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by appliction id.</span></span>

### <span data-ttu-id="12f7f-115">Beispiel 3: Exportieren von nach Benutzermitarbeitern aggregierten Datensätzen</span><span class="sxs-lookup"><span data-stu-id="12f7f-115">Example 3: Export records aggregated by user agent</span></span>
```
PS C:\> Export-AzLogAnalyticThrottledRequest -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByUserAgent
```

<span data-ttu-id="12f7f-116">Dieser Befehl speichert die insgesamt gedrosselten Microsoft.Compute-API-Aufrufe zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert vom Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="12f7f-116">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by user agent.</span></span>

## <span data-ttu-id="12f7f-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12f7f-117">PARAMETERS</span></span>

### <span data-ttu-id="12f7f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12f7f-118">-AsJob</span></span>
<span data-ttu-id="12f7f-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12f7f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12f7f-120">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="12f7f-120">-BlobContainerSasUri</span></span>
<span data-ttu-id="12f7f-121">SAS Uri des Protokollierungsblobcontainers, in den die LogAnalytics-Api Ausgabeprotokolle schreibt.</span><span class="sxs-lookup"><span data-stu-id="12f7f-121">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="12f7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f7f-122">-DefaultProfile</span></span>
<span data-ttu-id="12f7f-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12f7f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f7f-124">-FromTime</span><span class="sxs-lookup"><span data-stu-id="12f7f-124">-FromTime</span></span>
<span data-ttu-id="12f7f-125">Ab dem Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="12f7f-125">From time of the query</span></span>

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

### <span data-ttu-id="12f7f-126">-GroupByApplicationId</span><span class="sxs-lookup"><span data-stu-id="12f7f-126">-GroupByApplicationId</span></span>
<span data-ttu-id="12f7f-127">Gruppieren des Abfrageergebnisses nach Anwendungs-ID.</span><span class="sxs-lookup"><span data-stu-id="12f7f-127">Group query result by Application Id.</span></span>

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

### <span data-ttu-id="12f7f-128">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="12f7f-128">-GroupByOperationName</span></span>
<span data-ttu-id="12f7f-129">Gruppieren des Abfrageergebnisses nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="12f7f-129">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="12f7f-130">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="12f7f-130">-GroupByResourceName</span></span>
<span data-ttu-id="12f7f-131">Gruppieren des Abfrageergebnisses nach Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="12f7f-131">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="12f7f-132">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="12f7f-132">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="12f7f-133">Gruppieren des Abfrageergebnisses nach angewendeter Einschränkungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="12f7f-133">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="12f7f-134">-GroupByUserAgent</span><span class="sxs-lookup"><span data-stu-id="12f7f-134">-GroupByUserAgent</span></span>
<span data-ttu-id="12f7f-135">Gruppieren des Abfrageergebnisses nach UserAgent.</span><span class="sxs-lookup"><span data-stu-id="12f7f-135">Group query result by UserAgent.</span></span>

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

### <span data-ttu-id="12f7f-136">-Location</span><span class="sxs-lookup"><span data-stu-id="12f7f-136">-Location</span></span>
<span data-ttu-id="12f7f-137">Der Speicherort, an dem die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="12f7f-137">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="12f7f-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12f7f-138">-NoWait</span></span>
<span data-ttu-id="12f7f-139">Startet den Vorgang und gibt sofort zurück, bevor der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="12f7f-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="12f7f-140">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="12f7f-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="12f7f-141">-ToTime</span><span class="sxs-lookup"><span data-stu-id="12f7f-141">-ToTime</span></span>
<span data-ttu-id="12f7f-142">Bis zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="12f7f-142">To time of the query</span></span>

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

### <span data-ttu-id="12f7f-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12f7f-143">-Confirm</span></span>
<span data-ttu-id="12f7f-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12f7f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f7f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f7f-145">-WhatIf</span></span>
<span data-ttu-id="12f7f-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12f7f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f7f-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12f7f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f7f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f7f-148">CommonParameters</span></span>
<span data-ttu-id="12f7f-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f7f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f7f-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f7f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f7f-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12f7f-151">INPUTS</span></span>

### <span data-ttu-id="12f7f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="12f7f-152">System.String</span></span>

## <span data-ttu-id="12f7f-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12f7f-153">OUTPUTS</span></span>

### <span data-ttu-id="12f7f-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="12f7f-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="12f7f-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12f7f-155">NOTES</span></span>

## <span data-ttu-id="12f7f-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12f7f-156">RELATED LINKS</span></span>
