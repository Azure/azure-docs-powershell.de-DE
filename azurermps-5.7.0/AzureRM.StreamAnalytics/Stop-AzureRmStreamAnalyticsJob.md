---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476442"
---
# <span data-ttu-id="4e860-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="4e860-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e860-102">SYNOPSIS</span></span>
<span data-ttu-id="4e860-103">Beendet einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4e860-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e860-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e860-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e860-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e860-105">DESCRIPTION</span></span>
<span data-ttu-id="4e860-106">Das Cmdlet **Stop-AzureRmStreamAnalyticsJob** verhindert, dass ein Stream-Analyse Auftrag in Azure ausgeführt wird, und reserviert Ressourcen, die verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4e860-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="4e860-107">Die Auftragsdefinition und die Metadaten bleiben innerhalb Ihres Abonnements über das Azure-Portal und die Verwaltungs-APIs verfügbar, sodass der Auftrag bearbeitet und neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e860-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="4e860-108">Sie werden für einen Auftrag im Status "beendet" nicht in Rechnung gestellt.</span><span class="sxs-lookup"><span data-stu-id="4e860-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="4e860-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e860-109">EXAMPLES</span></span>

### <span data-ttu-id="4e860-110">Beispiel 1: Beenden eines ausgeführten Auftrags</span><span class="sxs-lookup"><span data-stu-id="4e860-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="4e860-111">Dieser Befehl beendet den Job-StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="4e860-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="4e860-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e860-112">PARAMETERS</span></span>

### <span data-ttu-id="4e860-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e860-113">-DefaultProfile</span></span>
<span data-ttu-id="4e860-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e860-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e860-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4e860-115">-Name</span></span>
<span data-ttu-id="4e860-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e860-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="4e860-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e860-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e860-118">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehört.</span><span class="sxs-lookup"><span data-stu-id="4e860-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="4e860-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e860-119">CommonParameters</span></span>
<span data-ttu-id="4e860-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e860-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e860-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e860-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e860-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e860-122">INPUTS</span></span>

### <span data-ttu-id="4e860-123">Keine</span><span class="sxs-lookup"><span data-stu-id="4e860-123">None</span></span>
<span data-ttu-id="4e860-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4e860-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e860-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e860-125">OUTPUTS</span></span>

### <span data-ttu-id="4e860-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e860-126">System.Object</span></span>

## <span data-ttu-id="4e860-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e860-127">NOTES</span></span>

## <span data-ttu-id="4e860-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e860-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e860-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4e860-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4e860-131">Neu – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4e860-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="4e860-133">Anfang-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="4e860-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


