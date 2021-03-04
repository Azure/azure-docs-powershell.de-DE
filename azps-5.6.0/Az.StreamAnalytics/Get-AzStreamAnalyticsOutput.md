---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929544"
---
# <span data-ttu-id="8f264-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8f264-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="8f264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f264-102">SYNOPSIS</span></span>
<span data-ttu-id="8f264-103">Ruft die in einem angegebenen Stream Analytics-Auftrag oder einer angegebenen Ausgabe definierten Ausgaben ab.</span><span class="sxs-lookup"><span data-stu-id="8f264-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="8f264-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f264-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f264-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f264-105">DESCRIPTION</span></span>
<span data-ttu-id="8f264-106">Im **Cmdlet Get-AzStreamAnalyticsOutput** werden alle Ausgaben aufgeführt, die in einem angegebenen Stream Analytics-Auftrag definiert sind oder Informationen zu einer bestimmten Ausgabe erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f264-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="8f264-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f264-107">EXAMPLES</span></span>

### <span data-ttu-id="8f264-108">Beispiel 1: Informationen zu Stellenausgängen</span><span class="sxs-lookup"><span data-stu-id="8f264-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="8f264-109">Dieser Befehl gibt Informationen zu den ausgaben zurück, die im Auftrag StreamingJob definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8f264-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="8f264-110">Beispiel 2: Informationen zu einer bestimmten Auftragsausgabe</span><span class="sxs-lookup"><span data-stu-id="8f264-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="8f264-111">Dieser Befehl gibt Informationen zur Ausgabe mit dem Namen Ausgabe zurück, die im Auftrag StreamingJob definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f264-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="8f264-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8f264-112">PARAMETERS</span></span>

### <span data-ttu-id="8f264-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f264-113">-DefaultProfile</span></span>
<span data-ttu-id="8f264-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f264-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f264-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="8f264-115">-JobName</span></span>
<span data-ttu-id="8f264-116">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="8f264-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="8f264-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f264-117">-Name</span></span>
<span data-ttu-id="8f264-118">Gibt den Namen der abzurufenden Azure Stream Analytics-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="8f264-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="8f264-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f264-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f264-120">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Ausgabe gehört.</span><span class="sxs-lookup"><span data-stu-id="8f264-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="8f264-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f264-121">CommonParameters</span></span>
<span data-ttu-id="8f264-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f264-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f264-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f264-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f264-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f264-124">INPUTS</span></span>

### <span data-ttu-id="8f264-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8f264-125">System.String</span></span>

## <span data-ttu-id="8f264-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f264-126">OUTPUTS</span></span>

### <span data-ttu-id="8f264-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="8f264-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="8f264-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8f264-128">NOTES</span></span>

## <span data-ttu-id="8f264-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8f264-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f264-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8f264-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8f264-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8f264-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8f264-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8f264-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


