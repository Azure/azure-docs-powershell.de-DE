---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66e8e58b84c0ea1ca0e71999dad56bcf464d6a0f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007216"
---
# <span data-ttu-id="9cb4b-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="9cb4b-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="9cb4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cb4b-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb4b-103">Rufen Sie die Liste der Angebote für den angegebenen Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="9cb4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cb4b-104">SYNTAX</span></span>

### <span data-ttu-id="9cb4b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cb4b-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9cb4b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9cb4b-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -OfferName <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cb4b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cb4b-107">DESCRIPTION</span></span>
<span data-ttu-id="9cb4b-108">Rufen Sie die Liste der Angebote für den angegebenen Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="9cb4b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cb4b-109">EXAMPLES</span></span>

### <span data-ttu-id="9cb4b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cb4b-110">EXAMPLE 1</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="9cb4b-111">Rufen Sie die Liste der Angebote für den angegebenen Delegierten Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="9cb4b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cb4b-112">PARAMETERS</span></span>

### <span data-ttu-id="9cb4b-113">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="9cb4b-113">-OfferName</span></span>
<span data-ttu-id="9cb4b-114">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-114">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb4b-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="9cb4b-115">-DelegatedProviderId</span></span>
<span data-ttu-id="9cb4b-116">Die ID des Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-116">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb4b-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="9cb4b-117">-Skip</span></span>
<span data-ttu-id="9cb4b-118">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb4b-119">-Top</span><span class="sxs-lookup"><span data-stu-id="9cb4b-119">-Top</span></span>
<span data-ttu-id="9cb4b-120">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9cb4b-121">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb4b-122">CommonParameters</span></span>
<span data-ttu-id="9cb4b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb4b-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb4b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb4b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cb4b-125">INPUTS</span></span>

## <span data-ttu-id="9cb4b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cb4b-126">OUTPUTS</span></span>

### <span data-ttu-id="9cb4b-127">Microsoft. AzureStack. Management. Subscription. Models. offer</span><span class="sxs-lookup"><span data-stu-id="9cb4b-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="9cb4b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cb4b-128">NOTES</span></span>

## <span data-ttu-id="9cb4b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cb4b-129">RELATED LINKS</span></span>
