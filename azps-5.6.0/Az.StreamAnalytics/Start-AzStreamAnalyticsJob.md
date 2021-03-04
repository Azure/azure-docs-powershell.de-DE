---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: cd7d6aaa9a295f888d8e765d12b4088525eff1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939835"
---
# <span data-ttu-id="f4e0a-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4e0a-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="f4e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e0a-103">Startet einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="f4e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4e0a-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e0a-106">Das **Cmdlet Start-AzStreamAnalyticsJob** stellt asynchron bereit und startet einen Stream Analytics-Auftrag in Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="f4e0a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4e0a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e0a-108">Beispiel 1: Starten eines Datenstromanalyseauftrags</span><span class="sxs-lookup"><span data-stu-id="f4e0a-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="f4e0a-109">Dieser Befehl startet den Auftrag StreamingJob und gibt an, dass der Ausgabeereignisdatenstrom zum Zeitstempel 2014-07-03T01:00Z gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="f4e0a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4e0a-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e0a-111">-DefaultProfile</span></span>
<span data-ttu-id="f4e0a-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e0a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f4e0a-113">-Name</span></span>
<span data-ttu-id="f4e0a-114">Gibt den Namen des zu startenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="f4e0a-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="f4e0a-115">-OutputStartMode</span></span>
<span data-ttu-id="f4e0a-116">Gibt den Startmodus für den Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="f4e0a-117">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f4e0a-117">Valid values are:</span></span> 
- <span data-ttu-id="f4e0a-118">JobStartTime – Dieser Wert gibt an, dass der Startpunkt des Ausgabeereignisdatenstroms beginnen soll, wenn der Auftrag gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="f4e0a-119">CustomTime – Dieser Wert gibt an, dass der Startpunkt des Ausgabeereignisdatenstroms zu einem benutzerdefinierten Zeitpunkt beginnen soll, der im *Parameter OutputStartTime angegeben* ist.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="f4e0a-120">LastOutputEventTime – Dieser Wert gibt an, dass der Startpunkt des Ausgabeereignisdatenstroms ab der letzten Ereignisausgabezeit beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="f4e0a-121">Wenn die -Eigenschaft nicht vorhanden ist, ist die Standardeinstellung JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="f4e0a-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="f4e0a-122">-OutputStartTime</span></span>
<span data-ttu-id="f4e0a-123">Gibt die Startzeit der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-123">Specifies the output start time.</span></span>
<span data-ttu-id="f4e0a-124">Dieser Wert ist entweder ein ISO-8601-formatierter Zeitstempel, der den Ausgangspunkt des Ausgabeereignisdatenstroms angibt, oder $Null, um anzugeben, dass der Ausgabeereignisdatenstrom beim Starten des Streamingauftrags gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="f4e0a-125">Diese Eigenschaft muss einen Wert haben, wenn *OutputStartMode* auf CustomTime festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="f4e0a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e0a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f4e0a-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="f4e0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e0a-128">CommonParameters</span></span>
<span data-ttu-id="f4e0a-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e0a-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e0a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e0a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e0a-131">INPUTS</span></span>

### <span data-ttu-id="f4e0a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f4e0a-132">System.String</span></span>

### <span data-ttu-id="f4e0a-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4e0a-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f4e0a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4e0a-134">OUTPUTS</span></span>

### <span data-ttu-id="f4e0a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4e0a-135">System.Boolean</span></span>

## <span data-ttu-id="f4e0a-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4e0a-136">NOTES</span></span>

## <span data-ttu-id="f4e0a-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4e0a-137">RELATED LINKS</span></span>

[<span data-ttu-id="f4e0a-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4e0a-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f4e0a-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4e0a-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f4e0a-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4e0a-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="f4e0a-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f4e0a-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


