---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 681782db0e1621e8d1126ca1f3425ce87e8e30d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929576"
---
# <span data-ttu-id="d325a-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d325a-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="d325a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d325a-102">SYNOPSIS</span></span>
<span data-ttu-id="d325a-103">Ruft Funktionen in einem Stream Analytics-Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="d325a-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="d325a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d325a-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d325a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d325a-105">DESCRIPTION</span></span>
<span data-ttu-id="d325a-106">Das **Get-AzStreamAnalyticsFunction-Cmdlet** ruft eine Liste der Funktionen ab, die in einem Azure Stream Analytics-Auftrag definiert sind, oder Informationen zu einer bestimmten Funktion.</span><span class="sxs-lookup"><span data-stu-id="d325a-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="d325a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d325a-107">EXAMPLES</span></span>

### <span data-ttu-id="d325a-108">Beispiel 1: Alle Stream Analytics-Funktionen erhalten</span><span class="sxs-lookup"><span data-stu-id="d325a-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="d325a-109">Dieser Befehl ruft die Funktionen ab, die für den Auftrag mit dem Namen StreamJob22 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d325a-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="d325a-110">Beispiel 2: Erhalten einer bestimmten Stream Analytics-Funktion</span><span class="sxs-lookup"><span data-stu-id="d325a-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="d325a-111">Dieser Befehl ruft Informationen zur Funktion mit dem Namen ScoreTweet ab, die für den Auftrag mit dem Namen StreamJob22 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d325a-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="d325a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d325a-112">PARAMETERS</span></span>

### <span data-ttu-id="d325a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d325a-113">-DefaultProfile</span></span>
<span data-ttu-id="d325a-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d325a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d325a-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="d325a-115">-JobName</span></span>
<span data-ttu-id="d325a-116">Gibt den Namen des Stream Analytics-Auftrags an, zu dem die Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="d325a-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="d325a-117">Dieses Cmdlet ruft Funktionen für den Auftrag ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d325a-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="d325a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d325a-118">-Name</span></span>
<span data-ttu-id="d325a-119">Gibt den Namen der Stream Analytics-Funktion an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d325a-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d325a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d325a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d325a-121">Gibt den Namen der Ressourcengruppe an, zu der Stream Analytics-Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="d325a-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="d325a-122">Dieses Cmdlet ruft Funktionen für die Gruppe ab, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d325a-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d325a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d325a-123">CommonParameters</span></span>
<span data-ttu-id="d325a-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d325a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d325a-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d325a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d325a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d325a-126">INPUTS</span></span>

### <span data-ttu-id="d325a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d325a-127">System.String</span></span>

## <span data-ttu-id="d325a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d325a-128">OUTPUTS</span></span>

### <span data-ttu-id="d325a-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="d325a-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="d325a-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d325a-130">NOTES</span></span>

## <span data-ttu-id="d325a-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d325a-131">RELATED LINKS</span></span>

[<span data-ttu-id="d325a-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d325a-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d325a-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d325a-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="d325a-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d325a-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


