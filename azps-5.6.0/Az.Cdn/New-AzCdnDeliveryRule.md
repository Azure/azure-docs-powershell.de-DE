---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944273"
---
# <span data-ttu-id="3bb64-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="3bb64-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="3bb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb64-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb64-103">Erstellt eine Zustellungsregel.</span><span class="sxs-lookup"><span data-stu-id="3bb64-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="3bb64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bb64-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bb64-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bb64-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb64-106">Das **Cmdlet New-AzCdnDeliveryRule** erstellt eine Übermittlungsregel für die Erstellung von CDN-Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="3bb64-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="3bb64-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bb64-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3bb64-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="3bb64-109">Erstellen Sie eine einfache Regel.</span><span class="sxs-lookup"><span data-stu-id="3bb64-109">Create a simple rule.</span></span>

## <span data-ttu-id="3bb64-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bb64-110">PARAMETERS</span></span>

### <span data-ttu-id="3bb64-111">-Aktion</span><span class="sxs-lookup"><span data-stu-id="3bb64-111">-Action</span></span>
<span data-ttu-id="3bb64-112">Eine Liste der Aktionen, die ausgeführt werden, wenn alle Bedingungen einer Regel erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="3bb64-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb64-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="3bb64-113">-Condition</span></span>
<span data-ttu-id="3bb64-114">Eine Liste der Bedingungen, die für die Ausführung der Aktionen übereinstimmen müssen.</span><span class="sxs-lookup"><span data-stu-id="3bb64-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb64-115">-DefaultProfile</span></span>
<span data-ttu-id="3bb64-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bb64-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb64-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3bb64-117">-Name</span></span>
<span data-ttu-id="3bb64-118">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="3bb64-118">Name of the rule</span></span>

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

### <span data-ttu-id="3bb64-119">-Bestellung</span><span class="sxs-lookup"><span data-stu-id="3bb64-119">-Order</span></span>
<span data-ttu-id="3bb64-120">Reihenfolge der Regel</span><span class="sxs-lookup"><span data-stu-id="3bb64-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb64-121">CommonParameters</span></span>
<span data-ttu-id="3bb64-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb64-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb64-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb64-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bb64-124">INPUTS</span></span>

### <span data-ttu-id="3bb64-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3bb64-125">None</span></span>

## <span data-ttu-id="3bb64-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bb64-126">OUTPUTS</span></span>

### <span data-ttu-id="3bb64-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="3bb64-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="3bb64-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3bb64-128">NOTES</span></span>

## <span data-ttu-id="3bb64-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3bb64-129">RELATED LINKS</span></span>
