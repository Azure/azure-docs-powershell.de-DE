---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826924"
---
# <span data-ttu-id="212e3-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="212e3-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="212e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="212e3-102">SYNOPSIS</span></span>
<span data-ttu-id="212e3-103">Ermitteln Sie die Plan Metriken.</span><span class="sxs-lookup"><span data-stu-id="212e3-103">Get the plan metrics.</span></span>

## <span data-ttu-id="212e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="212e3-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="212e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="212e3-105">DESCRIPTION</span></span>
<span data-ttu-id="212e3-106">Ermitteln Sie die Plan Metriken.</span><span class="sxs-lookup"><span data-stu-id="212e3-106">Get the plan metrics.</span></span>

## <span data-ttu-id="212e3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="212e3-107">EXAMPLES</span></span>

### <span data-ttu-id="212e3-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="212e3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="212e3-109">Besorgen Sie sich die Metriken eines Plans.</span><span class="sxs-lookup"><span data-stu-id="212e3-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="212e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="212e3-110">PARAMETERS</span></span>

### <span data-ttu-id="212e3-111">-Planname</span><span class="sxs-lookup"><span data-stu-id="212e3-111">-PlanName</span></span>
<span data-ttu-id="212e3-112">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="212e3-112">Name of the plan.</span></span>

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

### <span data-ttu-id="212e3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212e3-113">-ResourceGroupName</span></span>
<span data-ttu-id="212e3-114">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="212e3-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="212e3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212e3-115">CommonParameters</span></span>
<span data-ttu-id="212e3-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212e3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212e3-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="212e3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212e3-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="212e3-118">INPUTS</span></span>

## <span data-ttu-id="212e3-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="212e3-119">OUTPUTS</span></span>

### <span data-ttu-id="212e3-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="212e3-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="212e3-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="212e3-121">NOTES</span></span>

## <span data-ttu-id="212e3-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="212e3-122">RELATED LINKS</span></span>

