---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007302"
---
# <span data-ttu-id="06d34-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="06d34-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="06d34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06d34-102">SYNOPSIS</span></span>
<span data-ttu-id="06d34-103">Ermitteln Sie die Plan Metriken.</span><span class="sxs-lookup"><span data-stu-id="06d34-103">Get the plan metrics.</span></span>

## <span data-ttu-id="06d34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06d34-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="06d34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06d34-105">DESCRIPTION</span></span>
<span data-ttu-id="06d34-106">Ermitteln Sie die Plan Metriken.</span><span class="sxs-lookup"><span data-stu-id="06d34-106">Get the plan metrics.</span></span>

## <span data-ttu-id="06d34-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06d34-107">EXAMPLES</span></span>

### <span data-ttu-id="06d34-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="06d34-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="06d34-109">Besorgen Sie sich die Metriken eines Plans.</span><span class="sxs-lookup"><span data-stu-id="06d34-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="06d34-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="06d34-110">PARAMETERS</span></span>

### <span data-ttu-id="06d34-111">-Planname</span><span class="sxs-lookup"><span data-stu-id="06d34-111">-PlanName</span></span>
<span data-ttu-id="06d34-112">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="06d34-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d34-113">-ResourceGroupName</span></span>
<span data-ttu-id="06d34-114">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="06d34-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d34-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d34-115">CommonParameters</span></span>
<span data-ttu-id="06d34-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d34-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d34-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d34-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d34-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06d34-118">INPUTS</span></span>

## <span data-ttu-id="06d34-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06d34-119">OUTPUTS</span></span>

### <span data-ttu-id="06d34-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="06d34-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="06d34-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="06d34-121">NOTES</span></span>

## <span data-ttu-id="06d34-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06d34-122">RELATED LINKS</span></span>

