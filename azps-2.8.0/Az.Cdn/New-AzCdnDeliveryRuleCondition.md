---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652284"
---
# <span data-ttu-id="480ce-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="480ce-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="480ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="480ce-102">SYNOPSIS</span></span>
<span data-ttu-id="480ce-103">Erstellt eine Zustellungs Regelbedingung.</span><span class="sxs-lookup"><span data-stu-id="480ce-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="480ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="480ce-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="480ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="480ce-105">DESCRIPTION</span></span>
<span data-ttu-id="480ce-106">Das Cmdlet **New-AzCdnDeliveryRule** erstellt eine Übermittlungs Regel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="480ce-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="480ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="480ce-107">EXAMPLES</span></span>

### <span data-ttu-id="480ce-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="480ce-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="480ce-109">Erstellen Sie eine einfache Bedingung.</span><span class="sxs-lookup"><span data-stu-id="480ce-109">Create a simple condition.</span></span>

## <span data-ttu-id="480ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="480ce-110">PARAMETERS</span></span>

### <span data-ttu-id="480ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480ce-111">-DefaultProfile</span></span>
<span data-ttu-id="480ce-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="480ce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="480ce-113">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="480ce-113">-MatchValue</span></span>
<span data-ttu-id="480ce-114">Liste möglicher Übereinstimmungs Werte.</span><span class="sxs-lookup"><span data-stu-id="480ce-114">List of possible match values.</span></span>

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

### <span data-ttu-id="480ce-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="480ce-115">-MatchVariable</span></span>
<span data-ttu-id="480ce-116">Variable der Bedingung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="480ce-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="480ce-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="480ce-117">-NegateCondition</span></span>
<span data-ttu-id="480ce-118">Beschreibt, ob das Ergebnis dieser Bedingung negiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="480ce-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="480ce-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="480ce-119">-Operator</span></span>
<span data-ttu-id="480ce-120">Beschreibt den Operator, dem entsprochen werden soll</span><span class="sxs-lookup"><span data-stu-id="480ce-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="480ce-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="480ce-121">-Transform</span></span>
<span data-ttu-id="480ce-122">Transformation, die vor dem Abgleich angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="480ce-122">Transform to apply before matching.</span></span>
<span data-ttu-id="480ce-123">Mögliche Werte sind Kleinbuchstaben und Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="480ce-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="480ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480ce-124">CommonParameters</span></span>
<span data-ttu-id="480ce-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="480ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480ce-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="480ce-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480ce-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="480ce-127">INPUTS</span></span>

### <span data-ttu-id="480ce-128">Keine</span><span class="sxs-lookup"><span data-stu-id="480ce-128">None</span></span>

## <span data-ttu-id="480ce-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="480ce-129">OUTPUTS</span></span>

### <span data-ttu-id="480ce-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="480ce-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="480ce-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="480ce-131">NOTES</span></span>

## <span data-ttu-id="480ce-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="480ce-132">RELATED LINKS</span></span>
