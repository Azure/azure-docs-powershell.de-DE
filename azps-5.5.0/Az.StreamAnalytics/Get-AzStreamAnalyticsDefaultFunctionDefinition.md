---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150284"
---
# <span data-ttu-id="880c5-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="880c5-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="880c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="880c5-102">SYNOPSIS</span></span>
<span data-ttu-id="880c5-103">Ruft die Standarddefinition einer Funktion in Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="880c5-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="880c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="880c5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="880c5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="880c5-105">DESCRIPTION</span></span>
<span data-ttu-id="880c5-106">Das **Cmdlet "Get-AzStreamAnalyticsDefaultFunctionDefinition"** ruft die Standarddefinition einer Funktion in Azure Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="880c5-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="880c5-107">Sie können die Standarddefinition und das New-AzStreamAnalyticsFunction zum Erstellen einer Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="880c5-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="880c5-108">Sie können die Standarddefinition ändern, bevor Sie eine Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="880c5-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="880c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="880c5-109">EXAMPLES</span></span>

### <span data-ttu-id="880c5-110">Beispiel 1: Erhalten der Standarddefinition einer Stream analytics-Funktion</span><span class="sxs-lookup"><span data-stu-id="880c5-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="880c5-111">Dieser Befehl ruft die Standarddefinition der Funktion "ScoreTweet" mit den Parametern ab, die in der Datei RetrieveDefaultDefinitionRequest.jssind.</span><span class="sxs-lookup"><span data-stu-id="880c5-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="880c5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="880c5-112">PARAMETERS</span></span>

### <span data-ttu-id="880c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880c5-113">-DefaultProfile</span></span>
<span data-ttu-id="880c5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="880c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="880c5-115">-File</span><span class="sxs-lookup"><span data-stu-id="880c5-115">-File</span></span>
<span data-ttu-id="880c5-116">Gibt den Pfad einer JSON-Datei an, die die JavaScript Object Notation (JSON)-Darstellung des Anforderungstexts für die Anforderung der Standardfunktionsdefinitionsanforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="880c5-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c5-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="880c5-117">-JobName</span></span>
<span data-ttu-id="880c5-118">Gibt den Namen des Datenstromanalyseauftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="880c5-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="880c5-119">Dieses Cmdlet ruft die Standarddefinition für eine Funktion in dem Auftrag ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="880c5-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="880c5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="880c5-120">-Name</span></span>
<span data-ttu-id="880c5-121">Gibt den Namen der Stream Analytics-Funktion an, für die dieses Cmdlet die Standarddefinition erhält.</span><span class="sxs-lookup"><span data-stu-id="880c5-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="880c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="880c5-123">Gibt den Namen der Ressourcengruppe an, zu der Stream Analytics-Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="880c5-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="880c5-124">Dieses Cmdlet ruft eine Funktionsdefinition für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="880c5-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="880c5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880c5-125">CommonParameters</span></span>
<span data-ttu-id="880c5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="880c5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880c5-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880c5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880c5-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="880c5-128">INPUTS</span></span>

### <span data-ttu-id="880c5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="880c5-129">System.String</span></span>

## <span data-ttu-id="880c5-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="880c5-130">OUTPUTS</span></span>

### <span data-ttu-id="880c5-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="880c5-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="880c5-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="880c5-132">NOTES</span></span>

## <span data-ttu-id="880c5-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="880c5-133">RELATED LINKS</span></span>

[<span data-ttu-id="880c5-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="880c5-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


