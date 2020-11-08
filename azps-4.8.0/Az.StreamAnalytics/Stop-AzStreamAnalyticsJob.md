---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165440"
---
# <span data-ttu-id="ee9fb-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ee9fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9fb-103">Beendet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="ee9fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee9fb-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee9fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9fb-106">Das Cmdlet **Stop-AzStreamAnalyticsJob** verhindert, dass ein Stream-Analyse Auftrag in Azure ausgeführt wird, und reserviert Ressourcen, die verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="ee9fb-107">Die Auftragsdefinition und die Metadaten bleiben innerhalb Ihres Abonnements über das Azure-Portal und die Verwaltungs-APIs verfügbar, sodass der Auftrag bearbeitet und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="ee9fb-108">Sie werden für einen Auftrag im Status "beendet" nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="ee9fb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee9fb-109">EXAMPLES</span></span>

### <span data-ttu-id="ee9fb-110">Beispiel 1: Beenden eines ausgeführten Auftrags</span><span class="sxs-lookup"><span data-stu-id="ee9fb-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="ee9fb-111">Dieser Befehl beendet den Job-StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="ee9fb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9fb-112">PARAMETERS</span></span>

### <span data-ttu-id="ee9fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9fb-113">-DefaultProfile</span></span>
<span data-ttu-id="ee9fb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee9fb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ee9fb-115">-Name</span></span>
<span data-ttu-id="ee9fb-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="ee9fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee9fb-118">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="ee9fb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9fb-119">CommonParameters</span></span>
<span data-ttu-id="ee9fb-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9fb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9fb-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9fb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9fb-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee9fb-122">INPUTS</span></span>

### <span data-ttu-id="ee9fb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ee9fb-123">System.String</span></span>

## <span data-ttu-id="ee9fb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee9fb-124">OUTPUTS</span></span>

### <span data-ttu-id="ee9fb-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ee9fb-125">System.Boolean</span></span>

## <span data-ttu-id="ee9fb-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee9fb-126">NOTES</span></span>

## <span data-ttu-id="ee9fb-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee9fb-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee9fb-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ee9fb-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ee9fb-130">Neu – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ee9fb-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ee9fb-132">Anfang-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ee9fb-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


