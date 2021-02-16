---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145100"
---
# <span data-ttu-id="7adcb-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7adcb-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="7adcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adcb-102">SYNOPSIS</span></span>
<span data-ttu-id="7adcb-103">Erstellt eine Bedingung für Lieferregel.</span><span class="sxs-lookup"><span data-stu-id="7adcb-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="7adcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7adcb-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7adcb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7adcb-105">DESCRIPTION</span></span>
<span data-ttu-id="7adcb-106">Das **Cmdlet "New-AzCdnDeliveryRule"** erstellt eine Zustellungsregel für die Erstellung des CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="7adcb-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="7adcb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7adcb-107">EXAMPLES</span></span>

### <span data-ttu-id="7adcb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7adcb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="7adcb-109">Erstellen Sie eine einfache Bedingung.</span><span class="sxs-lookup"><span data-stu-id="7adcb-109">Create a simple condition.</span></span>

## <span data-ttu-id="7adcb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7adcb-110">PARAMETERS</span></span>

### <span data-ttu-id="7adcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adcb-111">-DefaultProfile</span></span>
<span data-ttu-id="7adcb-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7adcb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adcb-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="7adcb-113">-MatchValue</span></span>
<span data-ttu-id="7adcb-114">Liste der möglichen Übereinstimmungswerte.</span><span class="sxs-lookup"><span data-stu-id="7adcb-114">List of possible match values.</span></span>

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

### <span data-ttu-id="7adcb-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="7adcb-115">-MatchVariable</span></span>
<span data-ttu-id="7adcb-116">Die Variable der Bedingung muss übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7adcb-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="7adcb-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="7adcb-117">-NegateCondition</span></span>
<span data-ttu-id="7adcb-118">Beschreibt, ob das Ergebnis dieser Bedingung negiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="7adcb-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="7adcb-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="7adcb-119">-Operator</span></span>
<span data-ttu-id="7adcb-120">Beschreibt den zu matching-Operator</span><span class="sxs-lookup"><span data-stu-id="7adcb-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="7adcb-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="7adcb-121">-Selector</span></span>
<span data-ttu-id="7adcb-122">Name der Auswahl, die übereinstimmen soll</span><span class="sxs-lookup"><span data-stu-id="7adcb-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="7adcb-123">-Transformieren</span><span class="sxs-lookup"><span data-stu-id="7adcb-123">-Transform</span></span>
<span data-ttu-id="7adcb-124">Transformation, die vor dem Abgleich angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7adcb-124">Transform to apply before matching.</span></span>
<span data-ttu-id="7adcb-125">Mögliche Werte sind "Kleinbuchstaben" und "Großbuchstaben".</span><span class="sxs-lookup"><span data-stu-id="7adcb-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="7adcb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adcb-126">CommonParameters</span></span>
<span data-ttu-id="7adcb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7adcb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adcb-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7adcb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adcb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7adcb-129">INPUTS</span></span>

### <span data-ttu-id="7adcb-130">Keine</span><span class="sxs-lookup"><span data-stu-id="7adcb-130">None</span></span>

## <span data-ttu-id="7adcb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7adcb-131">OUTPUTS</span></span>

### <span data-ttu-id="7adcb-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="7adcb-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="7adcb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7adcb-133">NOTES</span></span>

## <span data-ttu-id="7adcb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7adcb-134">RELATED LINKS</span></span>
