---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007965"
---
# <span data-ttu-id="4dfe7-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4dfe7-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="4dfe7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfe7-103">Erstellen Sie ein PSRulesEngineMatchCondition-Objekt zum Erstellen einer Regelmodul Regel.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="4dfe7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dfe7-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dfe7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dfe7-105">DESCRIPTION</span></span>
<span data-ttu-id="4dfe7-106">Erstellen Sie ein PSRulesEngineMatchCondition-Objekt zum Erstellen einer Regelmodul Regel.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="4dfe7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dfe7-107">EXAMPLES</span></span>

### <span data-ttu-id="4dfe7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dfe7-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="4dfe7-109">Tolles ein neues PSRulesEngineMatchCondition-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="4dfe7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dfe7-110">PARAMETERS</span></span>

### <span data-ttu-id="4dfe7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfe7-111">-DefaultProfile</span></span>
<span data-ttu-id="4dfe7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfe7-113">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="4dfe7-113">-MatchValue</span></span>
<span data-ttu-id="4dfe7-114">Vergleichen Sie die Werte mit der Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-114">Match values to match against.</span></span>
<span data-ttu-id="4dfe7-115">Der Operator gilt für jeden Wert hier mit oder Semantik.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="4dfe7-116">Wenn einer der Variablen mit dem angegebenen Operator übereinstimmt, wird diese übereinstimmungsbedingung als Übereinstimmung angesehen.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="4dfe7-117">-MatchVariable</span></span>
<span data-ttu-id="4dfe7-118">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-118">Match Variable.</span></span>
<span data-ttu-id="4dfe7-119">Mögliche Werte sind IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="4dfe7-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="4dfe7-120">-NegateCondition</span></span>
<span data-ttu-id="4dfe7-121">Beschreibt, ob es sich um eine Negations Bedingung handelt.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="4dfe7-122">-Operator</span></span>
<span data-ttu-id="4dfe7-123">Beschreibt den Operator, der auf die übereinstimmungsbedingung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="4dfe7-124">Mögliche Werte sind any, IPMatch, geomatch, EQUAL, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, beginntmitder, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-125">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="4dfe7-125">-Selector</span></span>
<span data-ttu-id="4dfe7-126">Der Name des Selektors in RequestHeader oder RequestBody, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="4dfe7-127">-Transform</span></span>
<span data-ttu-id="4dfe7-128">Liste der Transformationen, die vor dem Abgleich angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="4dfe7-129">Mögliche einzelne Transformationswerte sind Kleinbuchstaben, Großbuchstaben, trimmen, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dfe7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfe7-130">CommonParameters</span></span>
<span data-ttu-id="4dfe7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfe7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfe7-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dfe7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfe7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dfe7-133">INPUTS</span></span>

### <span data-ttu-id="4dfe7-134">Keine</span><span class="sxs-lookup"><span data-stu-id="4dfe7-134">None</span></span>

## <span data-ttu-id="4dfe7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dfe7-135">OUTPUTS</span></span>

### <span data-ttu-id="4dfe7-136">Microsoft. Azure. Commands. Haustür. Models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="4dfe7-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="4dfe7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dfe7-137">NOTES</span></span>

## <span data-ttu-id="4dfe7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dfe7-138">RELATED LINKS</span></span>
