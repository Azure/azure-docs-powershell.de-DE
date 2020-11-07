---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: bdbd590f2c6c158759d439e473274c8b4508863d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824628"
---
# <span data-ttu-id="f614c-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f614c-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="f614c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f614c-102">SYNOPSIS</span></span>
<span data-ttu-id="f614c-103">Startet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="f614c-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="f614c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f614c-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f614c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f614c-105">DESCRIPTION</span></span>
<span data-ttu-id="f614c-106">Mit dem Cmdlet " **Start-AzStreamAnalyticsJob** " wird ein Datenstrom Analyse Auftrag in Azure asynchron bereitgestellt und gestartet.</span><span class="sxs-lookup"><span data-stu-id="f614c-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f614c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f614c-107">EXAMPLES</span></span>

### <span data-ttu-id="f614c-108">Beispiel 1: Starten eines Datenstrom Analyse Auftrags</span><span class="sxs-lookup"><span data-stu-id="f614c-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="f614c-109">Dieser Befehl startet den Job-StreamingJob und gibt an, dass der ausgabeereignis Datenstrom bei Timestamp 2014-07-03T01:00Z beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="f614c-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="f614c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f614c-110">PARAMETERS</span></span>

### <span data-ttu-id="f614c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f614c-111">-DefaultProfile</span></span>
<span data-ttu-id="f614c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f614c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f614c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f614c-113">-Name</span></span>
<span data-ttu-id="f614c-114">Gibt den Namen des zu startenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f614c-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="f614c-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="f614c-115">-OutputStartMode</span></span>
<span data-ttu-id="f614c-116">Gibt den Startmodus für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f614c-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="f614c-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f614c-117">Valid values are:</span></span> 
- <span data-ttu-id="f614c-118">JobStartTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms beginnen soll, wenn der Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f614c-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="f614c-119">Benutzerdefiniertes Zeit-dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms zu einem im *OutputStartTime* -Parameter angegebenen benutzerdefinierten Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="f614c-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="f614c-120">LastOutputEventTime – dieser Wert gibt an, dass der Ausgangspunkt des ausgabeereignis Datenstroms ab dem letzten Ereignisausgabe Zeitpunkt beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="f614c-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="f614c-121">Wenn die Eigenschaft nicht vorhanden ist, lautet der Standardwert JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="f614c-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="f614c-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="f614c-122">-OutputStartTime</span></span>
<span data-ttu-id="f614c-123">Gibt die Startzeit der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="f614c-123">Specifies the output start time.</span></span>
<span data-ttu-id="f614c-124">Dieser Wert ist entweder ein ISO-8601-formatierter Zeitstempel, der den Anfangspunkt des ausgabeereignis Datenstroms angibt, oder $NULL, um anzugeben, dass der ausgabeereignis Datenstrom beim Starten des Streaming-Auftrags gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f614c-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="f614c-125">Diese Eigenschaft muss einen Wert haben, wenn *OutputStartMode* auf "Benutzerdefiniert" eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="f614c-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="f614c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f614c-126">-ResourceGroupName</span></span>
<span data-ttu-id="f614c-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="f614c-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="f614c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f614c-128">CommonParameters</span></span>
<span data-ttu-id="f614c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f614c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f614c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f614c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f614c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f614c-131">INPUTS</span></span>

### <span data-ttu-id="f614c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f614c-132">System.String</span></span>

### <span data-ttu-id="f614c-133">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f614c-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f614c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f614c-134">OUTPUTS</span></span>

### <span data-ttu-id="f614c-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f614c-135">System.Boolean</span></span>

## <span data-ttu-id="f614c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f614c-136">NOTES</span></span>

## <span data-ttu-id="f614c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f614c-137">RELATED LINKS</span></span>

[<span data-ttu-id="f614c-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f614c-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f614c-139">Neu – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f614c-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f614c-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f614c-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f614c-141">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f614c-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


