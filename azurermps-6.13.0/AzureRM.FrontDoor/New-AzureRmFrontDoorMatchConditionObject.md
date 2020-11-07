---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663135"
---
# <span data-ttu-id="80988-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="80988-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="80988-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80988-102">SYNOPSIS</span></span>
<span data-ttu-id="80988-103">Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="80988-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80988-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80988-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80988-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80988-105">DESCRIPTION</span></span>
<span data-ttu-id="80988-106">Erstellen eines MatchCondition-Objekts für die WAF-Richtlinienerstellung</span><span class="sxs-lookup"><span data-stu-id="80988-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="80988-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80988-107">EXAMPLES</span></span>

### <span data-ttu-id="80988-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="80988-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="80988-109">Erstellen eines MatchCondition-Objekts</span><span class="sxs-lookup"><span data-stu-id="80988-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="80988-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80988-110">PARAMETERS</span></span>

### <span data-ttu-id="80988-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80988-111">-DefaultProfile</span></span>
<span data-ttu-id="80988-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80988-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80988-113">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="80988-113">-MatchValue</span></span>
<span data-ttu-id="80988-114">Übereinstimmungs Wert.</span><span class="sxs-lookup"><span data-stu-id="80988-114">Match value.</span></span>

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

### <span data-ttu-id="80988-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="80988-115">-MatchVariable</span></span>
<span data-ttu-id="80988-116">Variable vergleichen.</span><span class="sxs-lookup"><span data-stu-id="80988-116">Match Variable.</span></span>
<span data-ttu-id="80988-117">Mögliche Werte sind: ' RemoteAddr ', ' RequestMethod ', ' QueryString ', ' postargs ', ' RequestUri ', ' RequestHeader ', ' RequestBody '</span><span class="sxs-lookup"><span data-stu-id="80988-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80988-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="80988-118">-NegateCondition</span></span>
<span data-ttu-id="80988-119">Beschreibt, ob es sich um eine Negations Bedingung handelt oder ob der Standardwert falsch ist.</span><span class="sxs-lookup"><span data-stu-id="80988-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="80988-120">-Operatorproperty</span><span class="sxs-lookup"><span data-stu-id="80988-120">-OperatorProperty</span></span>
<span data-ttu-id="80988-121">Beschreibt den Operator, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="80988-121">Describes operator to be matched.</span></span>
<span data-ttu-id="80988-122">Mögliche Werte sind: "Any", "IPMatch", "geomatch", "gleich", "Contains", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "beginntmitder", "endsWith" "</span><span class="sxs-lookup"><span data-stu-id="80988-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80988-123">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="80988-123">-Selector</span></span>
<span data-ttu-id="80988-124">Der Name des Selektors in RequestHeader oder RequestBody, der zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="80988-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="80988-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80988-125">CommonParameters</span></span>
<span data-ttu-id="80988-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80988-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80988-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80988-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80988-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80988-128">INPUTS</span></span>

### <span data-ttu-id="80988-129">Keine</span><span class="sxs-lookup"><span data-stu-id="80988-129">None</span></span>

## <span data-ttu-id="80988-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80988-130">OUTPUTS</span></span>

### <span data-ttu-id="80988-131">Microsoft. Azure. Commands. Haustür. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="80988-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="80988-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="80988-132">NOTES</span></span>

## <span data-ttu-id="80988-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80988-133">RELATED LINKS</span></span>

[<span data-ttu-id="80988-134">Neu – AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="80988-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
