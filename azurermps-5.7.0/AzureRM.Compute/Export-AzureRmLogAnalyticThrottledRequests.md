---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticthrottledrequests
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticThrottledRequests.md
ms.openlocfilehash: a8deadf4760950eebbec22626bca475439ab0b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496641"
---
# <span data-ttu-id="88d0b-101">Export-AzureRmLogAnalyticThrottledRequests</span><span class="sxs-lookup"><span data-stu-id="88d0b-101">Export-AzureRmLogAnalyticThrottledRequests</span></span>

## <span data-ttu-id="88d0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="88d0b-103">Exportieren von Protokollen, die insgesamt gedrosselte API-Anforderungen für dieses Abonnement im angegebenen Zeitfenster anzeigen.</span><span class="sxs-lookup"><span data-stu-id="88d0b-103">Export logs that show total throttled Api requests for this subscription in the given time window.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88d0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88d0b-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticThrottledRequests [-GroupByOperationName] [-FromTime] <DateTime>
 [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String> [-GroupByResourceName] [-ToTime] <DateTime>
 [-Location] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88d0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="88d0b-106">Dadurch wird die Gesamtzahl der gedrosselten Microsoft. Compute-API-Aufrufe exportiert.</span><span class="sxs-lookup"><span data-stu-id="88d0b-106">This exports the total number of throttled Microsoft.Compute API calls.</span></span>
<span data-ttu-id="88d0b-107">Die Protokolle können durch drei Optionen weiter aggregiert werden: GroupByOperationName, GroupByThrottlePolicy oder GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="88d0b-107">The logs can be further aggregated by three options: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="88d0b-108">Beachten Sie, dass dieses Cmdlet nur CRP-Protokolle sammelt.</span><span class="sxs-lookup"><span data-stu-id="88d0b-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="88d0b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88d0b-109">EXAMPLES</span></span>

### <span data-ttu-id="88d0b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88d0b-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticThrottledRequests -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -GroupByOperationName
```

<span data-ttu-id="88d0b-111">Dieser Befehl speichert die insgesamt gedrosselten Microsoft. Compute-API-Aufrufe zwischen 2018-02-20T17:54:14 und 2018-02-22T17:54:17 im angegebenen SAS-URI, aggregiert nach Vorgangsname.</span><span class="sxs-lookup"><span data-stu-id="88d0b-111">This command stores the total throttled Microsoft.Compute API calls between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="88d0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="88d0b-112">PARAMETERS</span></span>

### <span data-ttu-id="88d0b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88d0b-113">-AsJob</span></span>
<span data-ttu-id="88d0b-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="88d0b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88d0b-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="88d0b-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="88d0b-116">SAS-URI des Protokollierungs-BLOB-Containers, in den Ausgabeprotokolle von der LogAnalytics-API geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="88d0b-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

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

### <span data-ttu-id="88d0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d0b-117">-DefaultProfile</span></span>
<span data-ttu-id="88d0b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88d0b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88d0b-119">-Ab-und-ab</span><span class="sxs-lookup"><span data-stu-id="88d0b-119">-FromTime</span></span>
<span data-ttu-id="88d0b-120">Ab Uhrzeit der Abfrage</span><span class="sxs-lookup"><span data-stu-id="88d0b-120">From time of the query</span></span>

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

### <span data-ttu-id="88d0b-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="88d0b-121">-GroupByOperationName</span></span>
<span data-ttu-id="88d0b-122">Ergebnis der Gruppenabfrage nach Vorgangs Name</span><span class="sxs-lookup"><span data-stu-id="88d0b-122">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="88d0b-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="88d0b-123">-GroupByResourceName</span></span>
<span data-ttu-id="88d0b-124">Ergebnis der Gruppenabfrage nach Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="88d0b-124">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="88d0b-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="88d0b-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="88d0b-126">Gruppenabfrage Ergebnis nach angewendeter Drosselungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="88d0b-126">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="88d0b-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="88d0b-127">-Location</span></span>
<span data-ttu-id="88d0b-128">Die Position, an der die Protokollanalyse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="88d0b-128">The location upon which log analytic is queried.</span></span>

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

### <span data-ttu-id="88d0b-129">-Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="88d0b-129">-ToTime</span></span>
<span data-ttu-id="88d0b-130">Zum Zeitpunkt der Abfrage</span><span class="sxs-lookup"><span data-stu-id="88d0b-130">To time of the query</span></span>

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

### <span data-ttu-id="88d0b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88d0b-131">-Confirm</span></span>
<span data-ttu-id="88d0b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88d0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d0b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d0b-133">-WhatIf</span></span>
<span data-ttu-id="88d0b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88d0b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d0b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88d0b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d0b-136">CommonParameters</span></span>
<span data-ttu-id="88d0b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d0b-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d0b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d0b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88d0b-139">INPUTS</span></span>

### <span data-ttu-id="88d0b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="88d0b-140">System.String</span></span>

## <span data-ttu-id="88d0b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88d0b-141">OUTPUTS</span></span>

### <span data-ttu-id="88d0b-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="88d0b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="88d0b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="88d0b-143">NOTES</span></span>

## <span data-ttu-id="88d0b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88d0b-144">RELATED LINKS</span></span>
