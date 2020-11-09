---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300376"
---
# <span data-ttu-id="89fe2-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="89fe2-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="89fe2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="89fe2-103">Erstellt eine Zustellungs Regelbedingung.</span><span class="sxs-lookup"><span data-stu-id="89fe2-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="89fe2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89fe2-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89fe2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="89fe2-106">Das Cmdlet **New-AzCdnDeliveryRule** erstellt eine Übermittlungs Regel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="89fe2-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="89fe2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89fe2-107">EXAMPLES</span></span>

### <span data-ttu-id="89fe2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89fe2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="89fe2-109">Erstellen Sie eine einfache Bedingung.</span><span class="sxs-lookup"><span data-stu-id="89fe2-109">Create a simple condition.</span></span>

## <span data-ttu-id="89fe2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="89fe2-110">PARAMETERS</span></span>

### <span data-ttu-id="89fe2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fe2-111">-DefaultProfile</span></span>
<span data-ttu-id="89fe2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89fe2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89fe2-113">-Matchwert</span><span class="sxs-lookup"><span data-stu-id="89fe2-113">-MatchValue</span></span>
<span data-ttu-id="89fe2-114">Liste möglicher Übereinstimmungs Werte.</span><span class="sxs-lookup"><span data-stu-id="89fe2-114">List of possible match values.</span></span>

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

### <span data-ttu-id="89fe2-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="89fe2-115">-MatchVariable</span></span>
<span data-ttu-id="89fe2-116">Variable der Bedingung vergleichen.</span><span class="sxs-lookup"><span data-stu-id="89fe2-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="89fe2-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="89fe2-117">-NegateCondition</span></span>
<span data-ttu-id="89fe2-118">Beschreibt, ob das Ergebnis dieser Bedingung negiert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="89fe2-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="89fe2-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="89fe2-119">-Operator</span></span>
<span data-ttu-id="89fe2-120">Beschreibt den Operator, dem entsprochen werden soll</span><span class="sxs-lookup"><span data-stu-id="89fe2-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="89fe2-121">-Auswahl</span><span class="sxs-lookup"><span data-stu-id="89fe2-121">-Selector</span></span>
<span data-ttu-id="89fe2-122">Name der Auswahl, die abgeglichen werden soll</span><span class="sxs-lookup"><span data-stu-id="89fe2-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="89fe2-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="89fe2-123">-Transform</span></span>
<span data-ttu-id="89fe2-124">Transformation, die vor dem Abgleich angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="89fe2-124">Transform to apply before matching.</span></span>
<span data-ttu-id="89fe2-125">Mögliche Werte sind Kleinbuchstaben und Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="89fe2-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="89fe2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fe2-126">CommonParameters</span></span>
<span data-ttu-id="89fe2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fe2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fe2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89fe2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fe2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89fe2-129">INPUTS</span></span>

### <span data-ttu-id="89fe2-130">Keine</span><span class="sxs-lookup"><span data-stu-id="89fe2-130">None</span></span>

## <span data-ttu-id="89fe2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89fe2-131">OUTPUTS</span></span>

### <span data-ttu-id="89fe2-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="89fe2-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="89fe2-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="89fe2-133">NOTES</span></span>

## <span data-ttu-id="89fe2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89fe2-134">RELATED LINKS</span></span>
