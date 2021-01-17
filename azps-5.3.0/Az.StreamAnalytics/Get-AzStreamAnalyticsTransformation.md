---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471674"
---
# <span data-ttu-id="d335d-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="d335d-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="d335d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d335d-102">SYNOPSIS</span></span>
<span data-ttu-id="d335d-103">Ruft Informationen zu einer Stream Analytics-Auftragstransformation ab.</span><span class="sxs-lookup"><span data-stu-id="d335d-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="d335d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d335d-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d335d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d335d-105">DESCRIPTION</span></span>
<span data-ttu-id="d335d-106">Das **Cmdlet "Get-AzStreamAnalyticsTransformation"** ruft Informationen zu einer Transformation ab, die in einem Stream Analytics-Auftrag definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d335d-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="d335d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d335d-107">EXAMPLES</span></span>

### <span data-ttu-id="d335d-108">BEISPIEL 1: Informationen zu einer Datenstromanalysetransformation</span><span class="sxs-lookup"><span data-stu-id="d335d-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="d335d-109">Dieser Befehl gibt Informationen zur Transformation "StreamingJob" für den Auftrag "StreamingJob" zurück.</span><span class="sxs-lookup"><span data-stu-id="d335d-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="d335d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d335d-110">PARAMETERS</span></span>

### <span data-ttu-id="d335d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d335d-111">-DefaultProfile</span></span>
<span data-ttu-id="d335d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d335d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d335d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d335d-113">-JobName</span></span>
<span data-ttu-id="d335d-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="d335d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="d335d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d335d-115">-Name</span></span>
<span data-ttu-id="d335d-116">Gibt den Namen der Azure Stream Analytics-Transformation an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d335d-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d335d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d335d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d335d-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="d335d-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="d335d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d335d-119">CommonParameters</span></span>
<span data-ttu-id="d335d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d335d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d335d-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d335d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d335d-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d335d-122">INPUTS</span></span>

### <span data-ttu-id="d335d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d335d-123">System.String</span></span>

## <span data-ttu-id="d335d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d335d-124">OUTPUTS</span></span>

### <span data-ttu-id="d335d-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="d335d-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="d335d-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d335d-126">NOTES</span></span>

## <span data-ttu-id="d335d-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d335d-127">RELATED LINKS</span></span>

[<span data-ttu-id="d335d-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="d335d-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


