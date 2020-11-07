---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824579"
---
# <span data-ttu-id="3180d-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3180d-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="3180d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3180d-102">SYNOPSIS</span></span>
<span data-ttu-id="3180d-103">Ruft Informationen zu einer Datenstrom Analyse-Auftrags Transformation ab.</span><span class="sxs-lookup"><span data-stu-id="3180d-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="3180d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3180d-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3180d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3180d-105">DESCRIPTION</span></span>
<span data-ttu-id="3180d-106">Das Cmdlet " **Get-AzStreamAnalyticsTransformation** " Ruft Informationen zu einer Transformation ab, die für einen Datenstrom Analyse Auftrag definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3180d-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="3180d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3180d-107">EXAMPLES</span></span>

### <span data-ttu-id="3180d-108">Beispiel 1: Abrufen von Informationen zu einer Datenstrom Analyse-Transformation</span><span class="sxs-lookup"><span data-stu-id="3180d-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="3180d-109">Dieser Befehl gibt Informationen zur Transformation namens StreamingJob für den Auftrag mit dem Namen StreamingJob zurück.</span><span class="sxs-lookup"><span data-stu-id="3180d-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="3180d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3180d-110">PARAMETERS</span></span>

### <span data-ttu-id="3180d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3180d-111">-DefaultProfile</span></span>
<span data-ttu-id="3180d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3180d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3180d-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="3180d-113">-JobName</span></span>
<span data-ttu-id="3180d-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="3180d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="3180d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3180d-115">-Name</span></span>
<span data-ttu-id="3180d-116">Gibt den Namen der Azure Stream Analytics-Transformation an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3180d-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="3180d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3180d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3180d-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="3180d-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="3180d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3180d-119">CommonParameters</span></span>
<span data-ttu-id="3180d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3180d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3180d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3180d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3180d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3180d-122">INPUTS</span></span>

### <span data-ttu-id="3180d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3180d-123">System.String</span></span>

## <span data-ttu-id="3180d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3180d-124">OUTPUTS</span></span>

### <span data-ttu-id="3180d-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="3180d-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="3180d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3180d-126">NOTES</span></span>

## <span data-ttu-id="3180d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3180d-127">RELATED LINKS</span></span>

[<span data-ttu-id="3180d-128">Neu – AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="3180d-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


