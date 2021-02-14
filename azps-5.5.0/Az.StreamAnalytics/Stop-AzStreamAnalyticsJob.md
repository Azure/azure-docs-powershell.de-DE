---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150145"
---
# <span data-ttu-id="ab115-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ab115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab115-102">SYNOPSIS</span></span>
<span data-ttu-id="ab115-103">Beendet einen Streamanalyseauftrag.</span><span class="sxs-lookup"><span data-stu-id="ab115-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="ab115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab115-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab115-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab115-105">DESCRIPTION</span></span>
<span data-ttu-id="ab115-106">Das **Cmdlet "Stop-AzStreamAnalyticsJob"** beendet asynchron die Ausführung eines Stream Analytics-Auftrags in Azure und verteilt Ressourcen, die verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ab115-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="ab115-107">Die Auftragsdefinition und Metadaten bleiben in Ihrem Abonnement über die Azure Portal- und Verwaltungs-APIs verfügbar, damit der Auftrag bearbeitet und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab115-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="ab115-108">Ihnen wird keine Aufgabe im Status "Beendet" in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="ab115-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="ab115-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab115-109">EXAMPLES</span></span>

### <span data-ttu-id="ab115-110">Beispiel 1: Beenden eines ausgeführten Auftrags</span><span class="sxs-lookup"><span data-stu-id="ab115-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="ab115-111">Dieser Befehl beendet den Auftrag "StreamingJob".</span><span class="sxs-lookup"><span data-stu-id="ab115-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="ab115-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab115-112">PARAMETERS</span></span>

### <span data-ttu-id="ab115-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab115-113">-DefaultProfile</span></span>
<span data-ttu-id="ab115-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab115-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab115-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ab115-115">-Name</span></span>
<span data-ttu-id="ab115-116">Gibt den Namen des zu beendenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="ab115-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="ab115-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab115-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab115-118">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="ab115-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="ab115-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab115-119">CommonParameters</span></span>
<span data-ttu-id="ab115-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab115-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab115-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab115-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab115-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab115-122">INPUTS</span></span>

### <span data-ttu-id="ab115-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ab115-123">System.String</span></span>

## <span data-ttu-id="ab115-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab115-124">OUTPUTS</span></span>

### <span data-ttu-id="ab115-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab115-125">System.Boolean</span></span>

## <span data-ttu-id="ab115-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab115-126">NOTES</span></span>

## <span data-ttu-id="ab115-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab115-127">RELATED LINKS</span></span>

[<span data-ttu-id="ab115-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ab115-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ab115-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ab115-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ab115-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ab115-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


