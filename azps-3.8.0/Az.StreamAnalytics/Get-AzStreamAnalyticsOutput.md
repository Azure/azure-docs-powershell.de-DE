---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 9f4b1af4de82be63990bdf8cc84a51866cecc1ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847487"
---
# <span data-ttu-id="9ad8f-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9ad8f-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="9ad8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ad8f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad8f-103">Ruft die Ausgaben ab, die in einem angegebenen Datenstrom Analyse Auftrag oder einer angegebenen Ausgabe definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="9ad8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad8f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad8f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ad8f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad8f-106">Das Cmdlet " **Get-AzStreamAnalyticsOutput** " listet alle Ausgaben auf, die in einem angegebenen Datenstrom Analyse Auftrag definiert sind, oder ruft Informationen zu einer bestimmten Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="9ad8f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ad8f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ad8f-108">Beispiel 1: Abrufen von Informationen zu Auftrags Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ad8f-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="9ad8f-109">Dieser Befehl gibt Informationen zu den für den Job-StreamingJob definierten Ausgaben zurück.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="9ad8f-110">Beispiel 2: Abrufen von Informationen zu einer bestimmten Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="9ad8f-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="9ad8f-111">Dieser Befehl gibt Informationen zur Ausgabe mit dem Namen Output zurück, die für den Job-StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="9ad8f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ad8f-112">PARAMETERS</span></span>

### <span data-ttu-id="9ad8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad8f-113">-DefaultProfile</span></span>
<span data-ttu-id="9ad8f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad8f-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="9ad8f-115">-JobName</span></span>
<span data-ttu-id="9ad8f-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9ad8f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ad8f-117">-Name</span></span>
<span data-ttu-id="9ad8f-118">Gibt den Namen der auszurufenden Azure-Stream-Analyseausgabe an.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="9ad8f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ad8f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ad8f-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9ad8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad8f-121">CommonParameters</span></span>
<span data-ttu-id="9ad8f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad8f-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad8f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad8f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ad8f-124">INPUTS</span></span>

### <span data-ttu-id="9ad8f-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9ad8f-125">System.String</span></span>

## <span data-ttu-id="9ad8f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ad8f-126">OUTPUTS</span></span>

### <span data-ttu-id="9ad8f-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="9ad8f-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="9ad8f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ad8f-128">NOTES</span></span>

## <span data-ttu-id="9ad8f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ad8f-129">RELATED LINKS</span></span>

[<span data-ttu-id="9ad8f-130">Neu – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9ad8f-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9ad8f-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9ad8f-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9ad8f-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9ad8f-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


