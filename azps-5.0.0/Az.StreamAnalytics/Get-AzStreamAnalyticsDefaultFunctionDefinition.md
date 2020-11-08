---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178187"
---
# <span data-ttu-id="fdf73-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="fdf73-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="fdf73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdf73-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf73-103">Ruft die Standard Definition einer Funktion in der Datenstrom Analyse ab.</span><span class="sxs-lookup"><span data-stu-id="fdf73-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="fdf73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf73-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf73-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdf73-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf73-106">Das Cmdlet " **Get-AzStreamAnalyticsDefaultFunctionDefinition** " Ruft die Standard Definition einer Funktion in Azure Stream Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="fdf73-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="fdf73-107">Sie können die Standard Definition und das New-AzStreamAnalyticsFunction-Cmdlet verwenden, um eine Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fdf73-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="fdf73-108">Sie können die Standard Definition ändern, bevor Sie eine Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="fdf73-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="fdf73-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdf73-109">EXAMPLES</span></span>

### <span data-ttu-id="fdf73-110">Beispiel 1: Abrufen der Standard Definition einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="fdf73-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="fdf73-111">Dieser Befehl ruft die Standard Definition der Funktion mit dem Namen ScoreTweet mithilfe der Parameter ab, die in der Datei RetrieveDefaultDefinitionRequest.jsangegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fdf73-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="fdf73-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf73-112">PARAMETERS</span></span>

### <span data-ttu-id="fdf73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf73-113">-DefaultProfile</span></span>
<span data-ttu-id="fdf73-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fdf73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf73-115">-Datei</span><span class="sxs-lookup"><span data-stu-id="fdf73-115">-File</span></span>
<span data-ttu-id="fdf73-116">Gibt den Pfad einer JSON-Datei an, die die JSON-Darstellung (JavaScript Object Notation) des Anforderungstexts für die Abruffunktion der Standard Funktions Definitions Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="fdf73-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="fdf73-117">-Jobname</span><span class="sxs-lookup"><span data-stu-id="fdf73-117">-JobName</span></span>
<span data-ttu-id="fdf73-118">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem Funktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="fdf73-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="fdf73-119">Dieses Cmdlet ruft die Standard Definition für eine Funktion in dem Auftrag ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fdf73-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdf73-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fdf73-120">-Name</span></span>
<span data-ttu-id="fdf73-121">Gibt den Namen der Datenstrom Analysefunktion an, für die dieses Cmdlet die Standard Definition abruft.</span><span class="sxs-lookup"><span data-stu-id="fdf73-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="fdf73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf73-122">-ResourceGroupName</span></span>
<span data-ttu-id="fdf73-123">Gibt den Namen der Ressourcengruppe an, zu der Datenstrom Analysefunktionen gehören.</span><span class="sxs-lookup"><span data-stu-id="fdf73-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="fdf73-124">Dieses Cmdlet ruft eine Funktionsdefinition für die Gruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fdf73-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdf73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf73-125">CommonParameters</span></span>
<span data-ttu-id="fdf73-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf73-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf73-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf73-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdf73-128">INPUTS</span></span>

### <span data-ttu-id="fdf73-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf73-129">System.String</span></span>

## <span data-ttu-id="fdf73-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdf73-130">OUTPUTS</span></span>

### <span data-ttu-id="fdf73-131">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="fdf73-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="fdf73-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdf73-132">NOTES</span></span>

## <span data-ttu-id="fdf73-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdf73-133">RELATED LINKS</span></span>

[<span data-ttu-id="fdf73-134">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="fdf73-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


