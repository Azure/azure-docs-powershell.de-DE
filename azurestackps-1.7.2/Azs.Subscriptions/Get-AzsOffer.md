---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650330"
---
# <span data-ttu-id="fd985-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="fd985-101">Get-AzsOffer</span></span>

## <span data-ttu-id="fd985-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd985-102">SYNOPSIS</span></span>
<span data-ttu-id="fd985-103">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="fd985-103">Get the list of public offers.</span></span>

## <span data-ttu-id="fd985-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd985-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fd985-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd985-105">DESCRIPTION</span></span>
<span data-ttu-id="fd985-106">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="fd985-106">Get the list of public offers.</span></span>

## <span data-ttu-id="fd985-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd985-107">EXAMPLES</span></span>

### <span data-ttu-id="fd985-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fd985-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="fd985-109">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="fd985-109">Get the list of public offers.</span></span>

## <span data-ttu-id="fd985-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd985-110">PARAMETERS</span></span>

### <span data-ttu-id="fd985-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="fd985-111">-Skip</span></span>
<span data-ttu-id="fd985-112">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd985-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd985-113">-Top</span><span class="sxs-lookup"><span data-stu-id="fd985-113">-Top</span></span>
<span data-ttu-id="fd985-114">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="fd985-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fd985-115">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="fd985-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd985-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd985-116">CommonParameters</span></span>
<span data-ttu-id="fd985-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd985-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd985-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd985-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd985-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd985-119">INPUTS</span></span>

## <span data-ttu-id="fd985-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd985-120">OUTPUTS</span></span>

### <span data-ttu-id="fd985-121">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="fd985-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="fd985-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd985-122">NOTES</span></span>

## <span data-ttu-id="fd985-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd985-123">RELATED LINKS</span></span>

