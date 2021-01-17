---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: a2f20aa2c372261fe8f36599884c516563170293
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471677"
---
# <span data-ttu-id="c8445-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c8445-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c8445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8445-102">SYNOPSIS</span></span>
<span data-ttu-id="c8445-103">Ruft die in einem angegebenen Stream Analytics-Auftrag oder einer bestimmten Ausgabe definierten Ausgaben ab.</span><span class="sxs-lookup"><span data-stu-id="c8445-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="c8445-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8445-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8445-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8445-105">DESCRIPTION</span></span>
<span data-ttu-id="c8445-106">Das **Cmdlet "Get-AzStreamAnalyticsOutput"** listet alle Ausgaben auf, die in einem angegebenen Stream Analytics-Auftrag definiert sind oder Informationen zu einer bestimmten Ausgabe erhalten.</span><span class="sxs-lookup"><span data-stu-id="c8445-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="c8445-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c8445-107">EXAMPLES</span></span>

### <span data-ttu-id="c8445-108">Beispiel 1: Informationen zu Auftragsausgabedaten</span><span class="sxs-lookup"><span data-stu-id="c8445-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="c8445-109">Dieser Befehl gibt Informationen zu den Im Auftrag von StreamingJob definierten Ausgaben zurück.</span><span class="sxs-lookup"><span data-stu-id="c8445-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="c8445-110">Beispiel 2: Erhalten von Informationen zu einer bestimmten Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="c8445-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c8445-111">Dieser Befehl gibt Informationen über die Ausgabe mit dem Namen "Ausgabe" zurück, die im Auftrag von StreamingJob definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c8445-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="c8445-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8445-112">PARAMETERS</span></span>

### <span data-ttu-id="c8445-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8445-113">-DefaultProfile</span></span>
<span data-ttu-id="c8445-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8445-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8445-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="c8445-115">-JobName</span></span>
<span data-ttu-id="c8445-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="c8445-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c8445-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8445-117">-Name</span></span>
<span data-ttu-id="c8445-118">Gibt den Namen der Azure Stream Analytics-Ausgabe an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8445-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="c8445-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8445-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8445-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="c8445-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c8445-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8445-121">CommonParameters</span></span>
<span data-ttu-id="c8445-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8445-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8445-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8445-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8445-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c8445-124">INPUTS</span></span>

### <span data-ttu-id="c8445-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c8445-125">System.String</span></span>

## <span data-ttu-id="c8445-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c8445-126">OUTPUTS</span></span>

### <span data-ttu-id="c8445-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="c8445-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="c8445-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c8445-128">NOTES</span></span>

## <span data-ttu-id="c8445-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c8445-129">RELATED LINKS</span></span>

[<span data-ttu-id="c8445-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c8445-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c8445-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c8445-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="c8445-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c8445-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


