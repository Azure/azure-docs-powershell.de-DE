---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847483"
---
# <span data-ttu-id="8e091-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8e091-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="8e091-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e091-102">SYNOPSIS</span></span>
<span data-ttu-id="8e091-103">Ruft Informationen zu einer Datenstrom Analyse-Auftrags Transformation ab.</span><span class="sxs-lookup"><span data-stu-id="8e091-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="8e091-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e091-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e091-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e091-105">DESCRIPTION</span></span>
<span data-ttu-id="8e091-106">Das Cmdlet " **Get-AzStreamAnalyticsTransformation** " Ruft Informationen zu einer Transformation ab, die für einen Datenstrom Analyse Auftrag definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8e091-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="8e091-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e091-107">EXAMPLES</span></span>

### <span data-ttu-id="8e091-108">Beispiel 1: Abrufen von Informationen zu einer Datenstrom Analyse-Transformation</span><span class="sxs-lookup"><span data-stu-id="8e091-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="8e091-109">Dieser Befehl gibt Informationen zur Transformation namens StreamingJob für den Auftrag mit dem Namen StreamingJob zurück.</span><span class="sxs-lookup"><span data-stu-id="8e091-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="8e091-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e091-110">PARAMETERS</span></span>

### <span data-ttu-id="8e091-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e091-111">-DefaultProfile</span></span>
<span data-ttu-id="8e091-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e091-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e091-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8e091-113">-JobName</span></span>
<span data-ttu-id="8e091-114">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="8e091-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="8e091-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8e091-115">-Name</span></span>
<span data-ttu-id="8e091-116">Gibt den Namen der Azure Stream Analytics-Transformation an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e091-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="8e091-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e091-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e091-118">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="8e091-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="8e091-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e091-119">CommonParameters</span></span>
<span data-ttu-id="8e091-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e091-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e091-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e091-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e091-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e091-122">INPUTS</span></span>

### <span data-ttu-id="8e091-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8e091-123">System.String</span></span>

## <span data-ttu-id="8e091-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e091-124">OUTPUTS</span></span>

### <span data-ttu-id="8e091-125">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="8e091-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="8e091-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e091-126">NOTES</span></span>

## <span data-ttu-id="8e091-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e091-127">RELATED LINKS</span></span>

[<span data-ttu-id="8e091-128">Neu – AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="8e091-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


