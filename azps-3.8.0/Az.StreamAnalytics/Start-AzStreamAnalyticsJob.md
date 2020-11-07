---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: c733c071bb0c7c2bc1c0c2d1fe1c2142d89e8590
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846367"
---
# <span data-ttu-id="dfa6a-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfa6a-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="dfa6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfa6a-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa6a-103">Startet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="dfa6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa6a-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfa6a-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa6a-106">Mit dem Cmdlet " **Start-AzStreamAnalyticsJob** " wird ein Datenstrom Analyse Auftrag in Azure asynchron bereitgestellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="dfa6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfa6a-107">EXAMPLES</span></span>

### <span data-ttu-id="dfa6a-108">Beispiel 1: Starten eines Datenstrom Analyse Auftrags</span><span class="sxs-lookup"><span data-stu-id="dfa6a-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="dfa6a-109">Dieser Befehl startet den Job-StreamingJob und gibt an, dass der ausgabeereignis Datenstrom bei Timestamp 2014-07-03T01:00Z beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="dfa6a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfa6a-110">PARAMETERS</span></span>

### <span data-ttu-id="dfa6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa6a-111">-DefaultProfile</span></span>
<span data-ttu-id="dfa6a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfa6a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dfa6a-113">-Name</span></span>
<span data-ttu-id="dfa6a-114">Gibt den Namen des zu startenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="dfa6a-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="dfa6a-115">-OutputStartMode</span></span>
<span data-ttu-id="dfa6a-116">Gibt den Startmodus für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="dfa6a-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="dfa6a-117">Valid values are:</span></span> 
- <span data-ttu-id="dfa6a-118">JobStartTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms beginnen soll, wenn der Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="dfa6a-119">Benutzerdefiniertes Zeit-dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms zu einem im *OutputStartTime* -Parameter angegebenen benutzerdefinierten Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="dfa6a-120">LastOutputEventTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms ab dem letzten Ereignisausgabe Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="dfa6a-121">Wenn die Eigenschaft nicht vorhanden ist, lautet der Standardwert JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa6a-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="dfa6a-122">-OutputStartTime</span></span>
<span data-ttu-id="dfa6a-123">Gibt die Startzeit der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-123">Specifies the output start time.</span></span>
<span data-ttu-id="dfa6a-124">Dieser Wert ist entweder ein ISO-8601-formatierter Zeitstempel, der den Anfangspunkt des ausgabeereignis Datenstroms angibt, oder $NULL, um anzugeben, dass der ausgabeereignis Datenstrom beim Starten des Streaming-Auftrags gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="dfa6a-125">Diese Eigenschaft muss einen Wert haben, wenn *OutputStartMode* auf "Benutzerdefiniert" eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfa6a-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="dfa6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa6a-128">CommonParameters</span></span>
<span data-ttu-id="dfa6a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa6a-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa6a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa6a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfa6a-131">INPUTS</span></span>

### <span data-ttu-id="dfa6a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dfa6a-132">System.String</span></span>

### <span data-ttu-id="dfa6a-133">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dfa6a-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dfa6a-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfa6a-134">OUTPUTS</span></span>

### <span data-ttu-id="dfa6a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dfa6a-135">System.Boolean</span></span>

## <span data-ttu-id="dfa6a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfa6a-136">NOTES</span></span>

## <span data-ttu-id="dfa6a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfa6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="dfa6a-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfa6a-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="dfa6a-139">Neu – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfa6a-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="dfa6a-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfa6a-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="dfa6a-141">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfa6a-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


