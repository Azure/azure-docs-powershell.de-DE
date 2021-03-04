---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: c900973947418ebfb1eba3b503fc40a9f81a68ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929600"
---
# <span data-ttu-id="f5069-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="f5069-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="f5069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5069-102">SYNOPSIS</span></span>
<span data-ttu-id="f5069-103">Ruft die Standarddefinition einer Funktion in Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="f5069-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="f5069-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5069-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5069-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5069-105">DESCRIPTION</span></span>
<span data-ttu-id="f5069-106">Das **Get-AzStreamAnalyticsDefaultFunctionDefinition-Cmdlet** ruft die Standarddefinition einer Funktion in Azure Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="f5069-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="f5069-107">Sie können die Standarddefinition und das New-AzStreamAnalyticsFunction-Cmdlet verwenden, um eine Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5069-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="f5069-108">Sie können die Standarddefinition ändern, bevor Sie eine Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5069-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="f5069-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5069-109">EXAMPLES</span></span>

### <span data-ttu-id="f5069-110">Beispiel 1: Erhalten der Standarddefinition einer Stream Analytics-Funktion</span><span class="sxs-lookup"><span data-stu-id="f5069-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="f5069-111">Dieser Befehl ruft die Standarddefinition der Funktion mit dem Namen ScoreTweet ab, indem die in der Datei RetrieveDefaultDefinitionRequest.jsangegebenen Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5069-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="f5069-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f5069-112">PARAMETERS</span></span>

### <span data-ttu-id="f5069-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5069-113">-DefaultProfile</span></span>
<span data-ttu-id="f5069-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5069-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5069-115">-Datei</span><span class="sxs-lookup"><span data-stu-id="f5069-115">-File</span></span>
<span data-ttu-id="f5069-116">Gibt den Pfad einer JSON-Datei an, die die JavaScript-Objekt-Notation (JSON)-Darstellung des Anforderungstexts für die Standardfunktionsdefinitionsanforderung zum Abrufen enthält.</span><span class="sxs-lookup"><span data-stu-id="f5069-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="f5069-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="f5069-117">-JobName</span></span>
<span data-ttu-id="f5069-118">Gibt den Namen des Stream Analytics-Auftrags an, zu dem die Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="f5069-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="f5069-119">Dieses Cmdlet ruft die Standarddefinition für eine Funktion in dem Auftrag ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="f5069-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5069-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f5069-120">-Name</span></span>
<span data-ttu-id="f5069-121">Gibt den Namen der Stream Analytics-Funktion an, für die dieses Cmdlet die Standarddefinition erhält.</span><span class="sxs-lookup"><span data-stu-id="f5069-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="f5069-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5069-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5069-123">Gibt den Namen der Ressourcengruppe an, zu der Stream Analytics-Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="f5069-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="f5069-124">Dieses Cmdlet ruft eine Funktionsdefinition für die Gruppe ab, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5069-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5069-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5069-125">CommonParameters</span></span>
<span data-ttu-id="f5069-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5069-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5069-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5069-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5069-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5069-128">INPUTS</span></span>

### <span data-ttu-id="f5069-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f5069-129">System.String</span></span>

## <span data-ttu-id="f5069-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5069-130">OUTPUTS</span></span>

### <span data-ttu-id="f5069-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="f5069-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="f5069-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f5069-132">NOTES</span></span>

## <span data-ttu-id="f5069-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f5069-133">RELATED LINKS</span></span>

[<span data-ttu-id="f5069-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="f5069-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


