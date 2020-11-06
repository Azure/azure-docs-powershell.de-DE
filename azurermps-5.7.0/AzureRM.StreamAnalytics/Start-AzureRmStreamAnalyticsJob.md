---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476445"
---
# <span data-ttu-id="347e8-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="347e8-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="347e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="347e8-102">SYNOPSIS</span></span>
<span data-ttu-id="347e8-103">Startet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="347e8-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="347e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="347e8-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="347e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="347e8-105">DESCRIPTION</span></span>
<span data-ttu-id="347e8-106">Mit dem Cmdlet " **Start-AzureRmStreamAnalyticsJob** " wird ein Datenstrom Analyse Auftrag in Azure asynchron bereitgestellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="347e8-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="347e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="347e8-107">EXAMPLES</span></span>

### <span data-ttu-id="347e8-108">Beispiel 1: Starten eines Datenstrom Analyse Auftrags</span><span class="sxs-lookup"><span data-stu-id="347e8-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="347e8-109">Dieser Befehl startet den Job-StreamingJob und gibt an, dass der ausgabeereignis Datenstrom bei Timestamp 2014-07-03T01:00Z beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="347e8-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="347e8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="347e8-110">PARAMETERS</span></span>

### <span data-ttu-id="347e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347e8-111">-DefaultProfile</span></span>
<span data-ttu-id="347e8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="347e8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="347e8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="347e8-113">-Name</span></span>
<span data-ttu-id="347e8-114">Gibt den Namen des zu startenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="347e8-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="347e8-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="347e8-115">-OutputStartMode</span></span>
<span data-ttu-id="347e8-116">Gibt den Startmodus für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="347e8-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="347e8-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="347e8-117">Valid values are:</span></span> 

- <span data-ttu-id="347e8-118">JobStartTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms beginnen soll, wenn der Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="347e8-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="347e8-119">Benutzerdefiniertes Zeit-dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms zu einem im *OutputStartTime* -Parameter angegebenen benutzerdefinierten Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="347e8-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="347e8-120">--LastOutputEventTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms ab dem letzten Ereignisausgabe Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="347e8-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="347e8-121">Wenn die Eigenschaft nicht vorhanden ist, lautet der Standardwert JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="347e8-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347e8-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="347e8-122">-OutputStartTime</span></span>
<span data-ttu-id="347e8-123">Gibt die Startzeit der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="347e8-123">Specifies the output start time.</span></span>
<span data-ttu-id="347e8-124">Dieser Wert ist entweder ein ISO-8601-formatierter Zeitstempel, der den Anfangspunkt des ausgabeereignis Datenstroms angibt, oder $NULL, um anzugeben, dass der ausgabeereignis Datenstrom beim Starten des Streaming-Auftrags gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="347e8-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="347e8-125">Diese Eigenschaft muss einen Wert haben, wenn *OutputStartMode* auf "Benutzerdefiniert" eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="347e8-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="347e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="347e8-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="347e8-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347e8-128">CommonParameters</span></span>
<span data-ttu-id="347e8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="347e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347e8-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="347e8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347e8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="347e8-131">INPUTS</span></span>

### <span data-ttu-id="347e8-132">Keine</span><span class="sxs-lookup"><span data-stu-id="347e8-132">None</span></span>
<span data-ttu-id="347e8-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="347e8-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="347e8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="347e8-134">OUTPUTS</span></span>

### <span data-ttu-id="347e8-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="347e8-135">System.Object</span></span>

## <span data-ttu-id="347e8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="347e8-136">NOTES</span></span>

## <span data-ttu-id="347e8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="347e8-137">RELATED LINKS</span></span>

[<span data-ttu-id="347e8-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="347e8-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="347e8-139">Neu – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="347e8-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="347e8-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="347e8-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="347e8-141">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="347e8-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


