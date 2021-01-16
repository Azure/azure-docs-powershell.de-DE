---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366455"
---
# <span data-ttu-id="54f5f-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="54f5f-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="54f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="54f5f-103">Ruft Funktionen in einem Streamanalyseauftrag ab.</span><span class="sxs-lookup"><span data-stu-id="54f5f-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="54f5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f5f-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f5f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="54f5f-106">Das **Cmdlet "Get-AzStreamAnalyticsFunction"** ruft eine Liste der Funktionen ab, die in einem Azure Stream Analytics-Auftrag definiert sind, oder Informationen zu einer bestimmten Funktion.</span><span class="sxs-lookup"><span data-stu-id="54f5f-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="54f5f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54f5f-107">EXAMPLES</span></span>

### <span data-ttu-id="54f5f-108">Beispiel 1: Alle Streamanalysefunktionen erhalten</span><span class="sxs-lookup"><span data-stu-id="54f5f-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="54f5f-109">Mit diesem Befehl werden die Funktionen für den Auftrag "StreamJob22" definiert.</span><span class="sxs-lookup"><span data-stu-id="54f5f-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="54f5f-110">Beispiel 2: Erhalten einer bestimmten Streamanalysefunktion</span><span class="sxs-lookup"><span data-stu-id="54f5f-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="54f5f-111">Dieser Befehl ruft Informationen über die Funktion mit dem Namen ScoreTweet ab, die für den Auftrag "StreamJob22" definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="54f5f-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="54f5f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54f5f-112">PARAMETERS</span></span>

### <span data-ttu-id="54f5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f5f-113">-DefaultProfile</span></span>
<span data-ttu-id="54f5f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54f5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f5f-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="54f5f-115">-JobName</span></span>
<span data-ttu-id="54f5f-116">Gibt den Namen des Datenstromanalyseauftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="54f5f-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="54f5f-117">Dieses Cmdlet ruft Funktionen für den Auftrag ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54f5f-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="54f5f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="54f5f-118">-Name</span></span>
<span data-ttu-id="54f5f-119">Gibt den Namen der Stream Analytics-Funktion an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="54f5f-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="54f5f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f5f-120">-ResourceGroupName</span></span>
<span data-ttu-id="54f5f-121">Gibt den Namen der Ressourcengruppe an, zu der Stream Analytics-Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="54f5f-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="54f5f-122">Dieses Cmdlet ruft Funktionen für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="54f5f-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="54f5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f5f-123">CommonParameters</span></span>
<span data-ttu-id="54f5f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f5f-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f5f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f5f-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54f5f-126">INPUTS</span></span>

### <span data-ttu-id="54f5f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="54f5f-127">System.String</span></span>

## <span data-ttu-id="54f5f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54f5f-128">OUTPUTS</span></span>

### <span data-ttu-id="54f5f-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="54f5f-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="54f5f-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54f5f-130">NOTES</span></span>

## <span data-ttu-id="54f5f-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54f5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="54f5f-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="54f5f-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="54f5f-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="54f5f-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="54f5f-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="54f5f-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


