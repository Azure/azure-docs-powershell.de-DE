---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 7b1b3af4a311b923880253573019c62ee399571c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846364"
---
# <span data-ttu-id="c0295-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="c0295-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0295-102">SYNOPSIS</span></span>
<span data-ttu-id="c0295-103">Beendet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c0295-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="c0295-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0295-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0295-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0295-105">DESCRIPTION</span></span>
<span data-ttu-id="c0295-106">Das Cmdlet **Stop-AzStreamAnalyticsJob** verhindert, dass ein Stream-Analyse Auftrag in Azure ausgeführt wird, und reserviert Ressourcen, die verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c0295-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="c0295-107">Die Auftragsdefinition und die Metadaten bleiben innerhalb Ihres Abonnements über das Azure-Portal und die Verwaltungs-APIs verfügbar, sodass der Auftrag bearbeitet und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0295-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="c0295-108">Sie werden für einen Auftrag im Status "beendet" nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="c0295-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="c0295-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0295-109">EXAMPLES</span></span>

### <span data-ttu-id="c0295-110">Beispiel 1: Beenden eines ausgeführten Auftrags</span><span class="sxs-lookup"><span data-stu-id="c0295-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="c0295-111">Dieser Befehl beendet den Job-StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c0295-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="c0295-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0295-112">PARAMETERS</span></span>

### <span data-ttu-id="c0295-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0295-113">-DefaultProfile</span></span>
<span data-ttu-id="c0295-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0295-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0295-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c0295-115">-Name</span></span>
<span data-ttu-id="c0295-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0295-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="c0295-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0295-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0295-118">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="c0295-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="c0295-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0295-119">CommonParameters</span></span>
<span data-ttu-id="c0295-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0295-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0295-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0295-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0295-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0295-122">INPUTS</span></span>

### <span data-ttu-id="c0295-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c0295-123">System.String</span></span>

## <span data-ttu-id="c0295-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0295-124">OUTPUTS</span></span>

### <span data-ttu-id="c0295-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0295-125">System.Boolean</span></span>

## <span data-ttu-id="c0295-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0295-126">NOTES</span></span>

## <span data-ttu-id="c0295-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0295-127">RELATED LINKS</span></span>

[<span data-ttu-id="c0295-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c0295-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c0295-130">Neu – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c0295-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c0295-132">Anfang-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c0295-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


