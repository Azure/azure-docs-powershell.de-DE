---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: 24313884b92a9a4c738425d64463c695ff689c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479842"
---
# <span data-ttu-id="9d3f3-101">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9d3f3-101">Get-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="9d3f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3f3-103">Ruft Informationen zu einer Datenstrom Analyse-Auftrags Transformation ab.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-103">Gets information about a Stream Analytics job transformation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d3f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d3f3-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d3f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="9d3f3-106">Das Cmdlet " **Get-AzureRmStreamAnalyticsTransformation** " Ruft Informationen zu einer Transformation ab, die für einen Datenstrom Analyse Auftrag definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-106">The **Get-AzureRmStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="9d3f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="9d3f3-108">Beispiel 1: Abrufen von Informationen zu einer Datenstrom Analyse-Transformation</span><span class="sxs-lookup"><span data-stu-id="9d3f3-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="9d3f3-109">Dieser Befehl gibt Informationen zur Transformation namens StreamingJob für den Auftrag mit dem Namen StreamingJob zurück.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="9d3f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="9d3f3-111">-Jobname</span><span class="sxs-lookup"><span data-stu-id="9d3f3-111">-JobName</span></span>
<span data-ttu-id="9d3f3-112">Gibt den Namen des Azure Stream Analytics-Auftrags an, zu dem die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="9d3f3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9d3f3-113">-Name</span></span>
<span data-ttu-id="9d3f3-114">Gibt den Namen der Azure Stream Analytics-Transformation an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-114">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="9d3f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d3f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d3f3-116">Gibt den Namen der Ressourcengruppe an, zu der die Azure Stream Analytics-Transformation gehört.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-116">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="9d3f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3f3-117">-DefaultProfile</span></span>
<span data-ttu-id="9d3f3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3f3-119">CommonParameters</span></span>
<span data-ttu-id="9d3f3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3f3-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d3f3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3f3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d3f3-122">INPUTS</span></span>

## <span data-ttu-id="9d3f3-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d3f3-123">OUTPUTS</span></span>

### <span data-ttu-id="9d3f3-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="9d3f3-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="9d3f3-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d3f3-125">NOTES</span></span>

## <span data-ttu-id="9d3f3-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d3f3-126">RELATED LINKS</span></span>

[<span data-ttu-id="9d3f3-127">Neu – AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="9d3f3-127">New-AzureRmStreamAnalyticsTransformation</span></span>](./New-AzureRmStreamAnalyticsTransformation.md)


