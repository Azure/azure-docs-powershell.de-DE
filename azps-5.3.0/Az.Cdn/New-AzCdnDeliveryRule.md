---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471008"
---
# <span data-ttu-id="d85b3-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="d85b3-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="d85b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d85b3-103">Erstellt eine Zustellungsregel.</span><span class="sxs-lookup"><span data-stu-id="d85b3-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="d85b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d85b3-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d85b3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d85b3-105">DESCRIPTION</span></span>
<span data-ttu-id="d85b3-106">Das **Cmdlet "New-AzCdnDeliveryRule"** erstellt eine Zustellungsregel für die Erstellung des CDN-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="d85b3-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d85b3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d85b3-107">EXAMPLES</span></span>

### <span data-ttu-id="d85b3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d85b3-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="d85b3-109">Erstellen Sie eine einfache Regel.</span><span class="sxs-lookup"><span data-stu-id="d85b3-109">Create a simple rule.</span></span>

## <span data-ttu-id="d85b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d85b3-110">PARAMETERS</span></span>

### <span data-ttu-id="d85b3-111">-Action</span><span class="sxs-lookup"><span data-stu-id="d85b3-111">-Action</span></span>
<span data-ttu-id="d85b3-112">Eine Liste der Aktionen, die ausgeführt werden, wenn alle Bedingungen einer Regel erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d85b3-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="d85b3-113">-Bedingung</span><span class="sxs-lookup"><span data-stu-id="d85b3-113">-Condition</span></span>
<span data-ttu-id="d85b3-114">Eine Liste der Bedingungen, die erfüllt werden müssen, damit die Aktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d85b3-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="d85b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85b3-115">-DefaultProfile</span></span>
<span data-ttu-id="d85b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d85b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85b3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d85b3-117">-Name</span></span>
<span data-ttu-id="d85b3-118">Name der Regel</span><span class="sxs-lookup"><span data-stu-id="d85b3-118">Name of the rule</span></span>

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

### <span data-ttu-id="d85b3-119">-Order</span><span class="sxs-lookup"><span data-stu-id="d85b3-119">-Order</span></span>
<span data-ttu-id="d85b3-120">Reihenfolge der Regel</span><span class="sxs-lookup"><span data-stu-id="d85b3-120">Order of the rule</span></span>

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

### <span data-ttu-id="d85b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85b3-121">CommonParameters</span></span>
<span data-ttu-id="d85b3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d85b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85b3-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d85b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85b3-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d85b3-124">INPUTS</span></span>

### <span data-ttu-id="d85b3-125">Keine</span><span class="sxs-lookup"><span data-stu-id="d85b3-125">None</span></span>

## <span data-ttu-id="d85b3-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d85b3-126">OUTPUTS</span></span>

### <span data-ttu-id="d85b3-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDEliveryRule</span><span class="sxs-lookup"><span data-stu-id="d85b3-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="d85b3-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d85b3-128">NOTES</span></span>

## <span data-ttu-id="d85b3-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d85b3-129">RELATED LINKS</span></span>
