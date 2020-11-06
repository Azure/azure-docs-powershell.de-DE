---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: 97f68475ab935df66b67f0cab92466e68732a735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480525"
---
# <span data-ttu-id="3f4b3-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="3f4b3-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="3f4b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4b3-103">Exportieren von Protokollen, die insgesamt gedrosselte API-Anforderungen für dieses Abonnement im angegebenen Zeitfenster anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f4b3-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f4b3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f4b3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f4b3-106">Dadurch wird die Gesamtzahl der gedrosselten Microsoft. Compute-API-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="3f4b3-107">Die Protokolle können durch drei Optionen weiter aggregiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="3f4b3-108">Beachten Sie, dass dieses Cmdlet nur CRP-Protokolle sammelt.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-108">Note that this cmdlet collects only CRP logs.</span></span>

<span data-ttu-id="3f4b3-109">Eine Übersicht über die API-Drosselung des Compute-Ressourcenanbieters finden Sie unter https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="3f4b3-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="3f4b3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f4b3-110">EXAMPLES</span></span>

### <span data-ttu-id="3f4b3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f4b3-111">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="3f4b3-112">Dieser Befehl speichert die insgesamt gedrosselten Microsoft. Compute-API-Aufrufe zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-112">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="3f4b3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f4b3-113">PARAMETERS</span></span>

### <span data-ttu-id="3f4b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f4b3-114">-AsJob</span></span>
<span data-ttu-id="3f4b3-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3f4b3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f4b3-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3f4b3-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="3f4b3-117">SAS-URI des Protokollierungs-BLOB-Containers, in den Ausgabeprotokolle von der LogAnalytics-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4b3-118">-DefaultProfile</span></span>
<span data-ttu-id="3f4b3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f4b3-120">-Ab-und-ab</span><span class="sxs-lookup"><span data-stu-id="3f4b3-120">-FromTime</span></span>
<span data-ttu-id="3f4b3-121">Ab Uhrzeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="3f4b3-121">From time of the query</span></span>

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

### <span data-ttu-id="3f4b3-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="3f4b3-122">-GroupByOperationName</span></span>
<span data-ttu-id="3f4b3-123">Ergebnis der Gruppenabfrage nach Vorgangs Name</span><span class="sxs-lookup"><span data-stu-id="3f4b3-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="3f4b3-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="3f4b3-124">-GroupByResourceName</span></span>
<span data-ttu-id="3f4b3-125">Ergebnis der Gruppenabfrage nach Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="3f4b3-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="3f4b3-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="3f4b3-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="3f4b3-127">Gruppenabfrage Ergebnis nach angewendeter Drosselungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="3f4b3-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="3f4b3-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="3f4b3-128">-Location</span></span>
<span data-ttu-id="3f4b3-129">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-129">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f4b3-130">-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="3f4b3-130">-ToTime</span></span>
<span data-ttu-id="3f4b3-131">Zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="3f4b3-131">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4b3-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f4b3-132">-Confirm</span></span>
<span data-ttu-id="3f4b3-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4b3-134">-WhatIf</span></span>
<span data-ttu-id="3f4b3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4b3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4b3-137">CommonParameters</span></span>
<span data-ttu-id="3f4b3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4b3-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4b3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4b3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f4b3-140">INPUTS</span></span>

### <span data-ttu-id="3f4b3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3f4b3-141">System.String</span></span>

## <span data-ttu-id="3f4b3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f4b3-142">OUTPUTS</span></span>

### <span data-ttu-id="3f4b3-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="3f4b3-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="3f4b3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f4b3-144">NOTES</span></span>

## <span data-ttu-id="3f4b3-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f4b3-145">RELATED LINKS</span></span>
