---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150228"
---
# <span data-ttu-id="53acf-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="53acf-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="53acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53acf-102">SYNOPSIS</span></span>
<span data-ttu-id="53acf-103">Ruft Informationen zu einer Stream Analytics-Auftragstransformation ab.</span><span class="sxs-lookup"><span data-stu-id="53acf-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="53acf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53acf-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53acf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53acf-105">DESCRIPTION</span></span>
<span data-ttu-id="53acf-106">Das **Cmdlet "Get-AzStreamAnalyticsTransformation"** ruft Informationen zu einer Transformation ab, die in einem Stream Analytics-Auftrag definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53acf-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="53acf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53acf-107">EXAMPLES</span></span>

### <span data-ttu-id="53acf-108">BEISPIEL 1: Informationen zu einer Datenstromanalysetransformation</span><span class="sxs-lookup"><span data-stu-id="53acf-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="53acf-109">Dieser Befehl gibt Informationen zur Transformation "StreamingJob" für den Auftrag "StreamingJob" zurück.</span><span class="sxs-lookup"><span data-stu-id="53acf-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="53acf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53acf-110">PARAMETERS</span></span>

### <span data-ttu-id="53acf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53acf-111">-DefaultProfile</span></span>
<span data-ttu-id="53acf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53acf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53acf-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="53acf-113">-JobName</span></span>
<span data-ttu-id="53acf-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="53acf-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="53acf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="53acf-115">-Name</span></span>
<span data-ttu-id="53acf-116">Gibt den Namen der Azure Stream Analytics-Transformation an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="53acf-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="53acf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53acf-117">-ResourceGroupName</span></span>
<span data-ttu-id="53acf-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="53acf-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="53acf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53acf-119">CommonParameters</span></span>
<span data-ttu-id="53acf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53acf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53acf-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53acf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53acf-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53acf-122">INPUTS</span></span>

### <span data-ttu-id="53acf-123">System.String</span><span class="sxs-lookup"><span data-stu-id="53acf-123">System.String</span></span>

## <span data-ttu-id="53acf-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53acf-124">OUTPUTS</span></span>

### <span data-ttu-id="53acf-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="53acf-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="53acf-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53acf-126">NOTES</span></span>

## <span data-ttu-id="53acf-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53acf-127">RELATED LINKS</span></span>

[<span data-ttu-id="53acf-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="53acf-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


