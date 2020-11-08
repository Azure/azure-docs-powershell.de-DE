---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007369"
---
# <span data-ttu-id="b7c6d-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="b7c6d-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="b7c6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c6d-103">Liste der unterstützten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="b7c6d-103">List of supported operations.</span></span>

## <span data-ttu-id="b7c6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c6d-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b7c6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c6d-106">Liste der unterstützten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="b7c6d-106">List of supported operations.</span></span>

## <span data-ttu-id="b7c6d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c6d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7c6d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b7c6d-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="b7c6d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b7c6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="b7c6d-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7c6d-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="b7c6d-112">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="b7c6d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7c6d-113">-DisplayName</span></span>
<span data-ttu-id="b7c6d-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-114">Subscription name.</span></span>

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

### <span data-ttu-id="b7c6d-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="b7c6d-115">-ExternalReferenceId</span></span>
<span data-ttu-id="b7c6d-116">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="b7c6d-117">-Id</span></span>
<span data-ttu-id="b7c6d-118">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c6d-119">-Name</span></span>
<span data-ttu-id="b7c6d-120">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-120">Name of the resource.</span></span>

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

### <span data-ttu-id="b7c6d-121">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="b7c6d-121">-OfferId</span></span>
<span data-ttu-id="b7c6d-122">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6d-123">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="b7c6d-123">-Owner</span></span>
<span data-ttu-id="b7c6d-124">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-124">Subscription owner.</span></span>

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

### <span data-ttu-id="b7c6d-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="b7c6d-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="b7c6d-126">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6d-127">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="b7c6d-127">-State</span></span>
<span data-ttu-id="b7c6d-128">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c6d-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b7c6d-129">-SubscriptionId</span></span>
<span data-ttu-id="b7c6d-130">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-130">Subscription identifier.</span></span>

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

### <span data-ttu-id="b7c6d-131">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="b7c6d-131">-TenantId</span></span>
<span data-ttu-id="b7c6d-132">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-132">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="b7c6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c6d-133">CommonParameters</span></span>
<span data-ttu-id="b7c6d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c6d-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c6d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c6d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7c6d-136">INPUTS</span></span>

## <span data-ttu-id="b7c6d-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7c6d-137">OUTPUTS</span></span>

## <span data-ttu-id="b7c6d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7c6d-138">NOTES</span></span>

## <span data-ttu-id="b7c6d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7c6d-139">RELATED LINKS</span></span>

