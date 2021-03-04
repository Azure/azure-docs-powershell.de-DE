---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2a13466b792426cdf06b7c52a8067f3adf5b787d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939816"
---
# <span data-ttu-id="c488f-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="c488f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c488f-102">SYNOPSIS</span></span>
<span data-ttu-id="c488f-103">Beendet einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c488f-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="c488f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c488f-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c488f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c488f-105">DESCRIPTION</span></span>
<span data-ttu-id="c488f-106">Das **Cmdlet Stop-AzStreamAnalyticsJob** beendet asynchron die Ausführung eines Stream Analytics-Auftrags in Azure und verteilt Ressourcen, die verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c488f-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="c488f-107">Die Auftragsdefinition und Metadaten bleiben in Ihrem Abonnement über die Azure Portal- und Verwaltungs-APIs verfügbar, damit der Auftrag bearbeitet und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c488f-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="c488f-108">Sie erhalten keine Kosten für einen Auftrag im Status "Beendet".</span><span class="sxs-lookup"><span data-stu-id="c488f-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="c488f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c488f-109">EXAMPLES</span></span>

### <span data-ttu-id="c488f-110">Beispiel 1: Beenden eines ausgeführten Auftrags</span><span class="sxs-lookup"><span data-stu-id="c488f-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="c488f-111">Mit diesem Befehl wird der Auftrag StreamingJob beendet.</span><span class="sxs-lookup"><span data-stu-id="c488f-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="c488f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c488f-112">PARAMETERS</span></span>

### <span data-ttu-id="c488f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c488f-113">-DefaultProfile</span></span>
<span data-ttu-id="c488f-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c488f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c488f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c488f-115">-Name</span></span>
<span data-ttu-id="c488f-116">Gibt den Namen des zu beendenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="c488f-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="c488f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c488f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c488f-118">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="c488f-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="c488f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c488f-119">CommonParameters</span></span>
<span data-ttu-id="c488f-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c488f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c488f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c488f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c488f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c488f-122">INPUTS</span></span>

### <span data-ttu-id="c488f-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c488f-123">System.String</span></span>

## <span data-ttu-id="c488f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c488f-124">OUTPUTS</span></span>

### <span data-ttu-id="c488f-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c488f-125">System.Boolean</span></span>

## <span data-ttu-id="c488f-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c488f-126">NOTES</span></span>

## <span data-ttu-id="c488f-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c488f-127">RELATED LINKS</span></span>

[<span data-ttu-id="c488f-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c488f-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c488f-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c488f-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c488f-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c488f-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


