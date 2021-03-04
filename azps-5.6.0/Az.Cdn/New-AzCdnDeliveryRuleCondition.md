---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947224"
---
# <span data-ttu-id="d67c8-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d67c8-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="d67c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d67c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d67c8-103">Erstellt eine Bedingung für die Zustellungsregel.</span><span class="sxs-lookup"><span data-stu-id="d67c8-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="d67c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d67c8-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d67c8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d67c8-105">DESCRIPTION</span></span>
<span data-ttu-id="d67c8-106">Das **Cmdlet New-AzCdnDeliveryRule** erstellt eine Übermittlungsregel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="d67c8-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d67c8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d67c8-107">EXAMPLES</span></span>

### <span data-ttu-id="d67c8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d67c8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="d67c8-109">Erstellen Sie eine einfache Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d67c8-109">Create a simple condition.</span></span>

## <span data-ttu-id="d67c8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d67c8-110">PARAMETERS</span></span>

### <span data-ttu-id="d67c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67c8-111">-DefaultProfile</span></span>
<span data-ttu-id="d67c8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d67c8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67c8-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d67c8-113">-MatchValue</span></span>
<span data-ttu-id="d67c8-114">Liste möglicher Übereinstimmungswerte.</span><span class="sxs-lookup"><span data-stu-id="d67c8-114">List of possible match values.</span></span>

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

### <span data-ttu-id="d67c8-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d67c8-115">-MatchVariable</span></span>
<span data-ttu-id="d67c8-116">Übereinstimmungsvariable der Bedingung.</span><span class="sxs-lookup"><span data-stu-id="d67c8-116">Match variable of the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67c8-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="d67c8-117">-NegateCondition</span></span>
<span data-ttu-id="d67c8-118">Beschreibt, ob das Ergebnis dieser Bedingung negiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d67c8-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67c8-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="d67c8-119">-Operator</span></span>
<span data-ttu-id="d67c8-120">Beschreibt den zu matching-Operator</span><span class="sxs-lookup"><span data-stu-id="d67c8-120">Describes operator to be matched</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67c8-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="d67c8-121">-Selector</span></span>
<span data-ttu-id="d67c8-122">Name der Auswahl, die übereinstimmen soll</span><span class="sxs-lookup"><span data-stu-id="d67c8-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="d67c8-123">-Transformieren</span><span class="sxs-lookup"><span data-stu-id="d67c8-123">-Transform</span></span>
<span data-ttu-id="d67c8-124">Transformieren, um vor dem Abgleich anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="d67c8-124">Transform to apply before matching.</span></span>
<span data-ttu-id="d67c8-125">Mögliche Werte sind Klein- und Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="d67c8-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="d67c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67c8-126">CommonParameters</span></span>
<span data-ttu-id="d67c8-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d67c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67c8-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d67c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67c8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d67c8-129">INPUTS</span></span>

### <span data-ttu-id="d67c8-130">Keine</span><span class="sxs-lookup"><span data-stu-id="d67c8-130">None</span></span>

## <span data-ttu-id="d67c8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d67c8-131">OUTPUTS</span></span>

### <span data-ttu-id="d67c8-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d67c8-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="d67c8-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d67c8-133">NOTES</span></span>

## <span data-ttu-id="d67c8-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d67c8-134">RELATED LINKS</span></span>
