---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827788"
---
# <span data-ttu-id="4ad21-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="4ad21-101">Get-AzsOffer</span></span>

## <span data-ttu-id="4ad21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ad21-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad21-103">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="4ad21-103">Get the list of public offers.</span></span>

## <span data-ttu-id="4ad21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ad21-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="4ad21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ad21-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad21-106">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="4ad21-106">Get the list of public offers.</span></span>

## <span data-ttu-id="4ad21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ad21-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad21-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ad21-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="4ad21-109">Holen Sie sich die Liste der öffentlichen Angebote.</span><span class="sxs-lookup"><span data-stu-id="4ad21-109">Get the list of public offers.</span></span>

## <span data-ttu-id="4ad21-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ad21-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad21-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="4ad21-111">-Skip</span></span>
<span data-ttu-id="4ad21-112">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ad21-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4ad21-113">-Top</span><span class="sxs-lookup"><span data-stu-id="4ad21-113">-Top</span></span>
<span data-ttu-id="4ad21-114">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="4ad21-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4ad21-115">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="4ad21-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4ad21-116">-Anbieter</span><span class="sxs-lookup"><span data-stu-id="4ad21-116">-Provider</span></span>
<span data-ttu-id="4ad21-117">Optionaler Parameter, um den Namen des Delegierten Anbieters anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4ad21-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="4ad21-118">Dieser Parameter wird nicht verwendet und wird in Zukunft veraltet sein.</span><span class="sxs-lookup"><span data-stu-id="4ad21-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad21-119">CommonParameters</span></span>
<span data-ttu-id="4ad21-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad21-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad21-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad21-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ad21-122">INPUTS</span></span>

## <span data-ttu-id="4ad21-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ad21-123">OUTPUTS</span></span>

### <span data-ttu-id="4ad21-124">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="4ad21-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="4ad21-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ad21-125">NOTES</span></span>

## <span data-ttu-id="4ad21-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ad21-126">RELATED LINKS</span></span>
