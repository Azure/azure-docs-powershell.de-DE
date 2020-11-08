---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007059"
---
# <span data-ttu-id="a2b92-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="a2b92-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="a2b92-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2b92-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b92-103">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="a2b92-103">Get the offer metrics.</span></span>

## <span data-ttu-id="a2b92-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2b92-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="a2b92-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b92-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b92-106">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="a2b92-106">Get the offer metrics.</span></span>

## <span data-ttu-id="a2b92-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2b92-107">EXAMPLES</span></span>

### <span data-ttu-id="a2b92-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a2b92-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="a2b92-109">Holen Sie sich die Angebots Metrik.</span><span class="sxs-lookup"><span data-stu-id="a2b92-109">Get the offer metrics.</span></span>

## <span data-ttu-id="a2b92-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b92-110">PARAMETERS</span></span>

### <span data-ttu-id="a2b92-111">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="a2b92-111">-OfferName</span></span>
<span data-ttu-id="a2b92-112">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="a2b92-112">Name of an offer.</span></span>

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

### <span data-ttu-id="a2b92-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b92-113">-ResourceGroupName</span></span>
<span data-ttu-id="a2b92-114">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="a2b92-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a2b92-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b92-115">CommonParameters</span></span>
<span data-ttu-id="a2b92-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b92-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b92-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b92-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b92-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2b92-118">INPUTS</span></span>

## <span data-ttu-id="a2b92-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2b92-119">OUTPUTS</span></span>

### <span data-ttu-id="a2b92-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="a2b92-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="a2b92-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2b92-121">NOTES</span></span>

## <span data-ttu-id="a2b92-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2b92-122">RELATED LINKS</span></span>

