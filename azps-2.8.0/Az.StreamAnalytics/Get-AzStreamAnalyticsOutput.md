---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: bf4a8734304ce92dac1bc329d6ae0ffa0f30c09c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823076"
---
# <span data-ttu-id="0d676-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0d676-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0d676-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d676-102">SYNOPSIS</span></span>
<span data-ttu-id="0d676-103">Ruft die Ausgaben ab, die in einem angegebenen Datenstrom Analyse Auftrag oder einer angegebenen Ausgabe definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0d676-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="0d676-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d676-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d676-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d676-105">DESCRIPTION</span></span>
<span data-ttu-id="0d676-106">Das Cmdlet " **Get-AzStreamAnalyticsOutput** " listet alle Ausgaben auf, die in einem angegebenen Datenstrom Analyse Auftrag definiert sind, oder ruft Informationen zu einer bestimmten Ausgabe ab.</span><span class="sxs-lookup"><span data-stu-id="0d676-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="0d676-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d676-107">EXAMPLES</span></span>

### <span data-ttu-id="0d676-108">Beispiel 1: Abrufen von Informationen zu Auftrags Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d676-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="0d676-109">Dieser Befehl gibt Informationen zu den für den Job-StreamingJob definierten Ausgaben zurück.</span><span class="sxs-lookup"><span data-stu-id="0d676-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="0d676-110">Beispiel 2: Abrufen von Informationen zu einer bestimmten Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="0d676-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0d676-111">Dieser Befehl gibt Informationen zur Ausgabe mit dem Namen Output zurück, die für den Job-StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0d676-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="0d676-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d676-112">PARAMETERS</span></span>

### <span data-ttu-id="0d676-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d676-113">-DefaultProfile</span></span>
<span data-ttu-id="0d676-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d676-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d676-115">-Jobname</span><span class="sxs-lookup"><span data-stu-id="0d676-115">-JobName</span></span>
<span data-ttu-id="0d676-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="0d676-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0d676-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d676-117">-Name</span></span>
<span data-ttu-id="0d676-118">Gibt den Namen der auszurufenden Azure-Stream-Analyseausgabe an.</span><span class="sxs-lookup"><span data-stu-id="0d676-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="0d676-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d676-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d676-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="0d676-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0d676-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d676-121">CommonParameters</span></span>
<span data-ttu-id="0d676-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d676-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d676-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d676-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d676-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d676-124">INPUTS</span></span>

### <span data-ttu-id="0d676-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0d676-125">System.String</span></span>

## <span data-ttu-id="0d676-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d676-126">OUTPUTS</span></span>

### <span data-ttu-id="0d676-127">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="0d676-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="0d676-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d676-128">NOTES</span></span>

## <span data-ttu-id="0d676-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d676-129">RELATED LINKS</span></span>

[<span data-ttu-id="0d676-130">Neu – AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0d676-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0d676-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0d676-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0d676-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0d676-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


