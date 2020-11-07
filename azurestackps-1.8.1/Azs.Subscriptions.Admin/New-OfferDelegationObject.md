---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828135"
---
# <span data-ttu-id="a06e7-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="a06e7-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="a06e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a06e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a06e7-103">Delegation anbieten.</span><span class="sxs-lookup"><span data-stu-id="a06e7-103">Offer delegation.</span></span>

## <span data-ttu-id="a06e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a06e7-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a06e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a06e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a06e7-106">Delegation anbieten.</span><span class="sxs-lookup"><span data-stu-id="a06e7-106">Offer delegation.</span></span>

## <span data-ttu-id="a06e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a06e7-107">EXAMPLES</span></span>

### <span data-ttu-id="a06e7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a06e7-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="a06e7-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="a06e7-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="a06e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a06e7-110">PARAMETERS</span></span>

### <span data-ttu-id="a06e7-111">-ID</span><span class="sxs-lookup"><span data-stu-id="a06e7-111">-Id</span></span>
<span data-ttu-id="a06e7-112">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a06e7-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="a06e7-113">-Location</span></span>
<span data-ttu-id="a06e7-114">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a06e7-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a06e7-115">-Name</span></span>
<span data-ttu-id="a06e7-116">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a06e7-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a06e7-117">-SubscriptionId</span></span>
<span data-ttu-id="a06e7-118">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="a06e7-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="a06e7-119">-Tags</span></span>
<span data-ttu-id="a06e7-120">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="a06e7-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="a06e7-121">-Type</span></span>
<span data-ttu-id="a06e7-122">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a06e7-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06e7-123">CommonParameters</span></span>
<span data-ttu-id="a06e7-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06e7-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06e7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06e7-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a06e7-126">INPUTS</span></span>

## <span data-ttu-id="a06e7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a06e7-127">OUTPUTS</span></span>

## <span data-ttu-id="a06e7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="a06e7-128">NOTES</span></span>

## <span data-ttu-id="a06e7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a06e7-129">RELATED LINKS</span></span>

