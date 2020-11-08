---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007370"
---
# <span data-ttu-id="492f7-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="492f7-101">New-PlanObject</span></span>

## <span data-ttu-id="492f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="492f7-102">SYNOPSIS</span></span>
<span data-ttu-id="492f7-103">Ein Plan steht für ein Paket von Kontingenten und Funktionen, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="492f7-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="492f7-104">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="492f7-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="492f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="492f7-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="492f7-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="492f7-106">DESCRIPTION</span></span>
<span data-ttu-id="492f7-107">Ein Plan steht für ein Paket von Kontingenten und Funktionen, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="492f7-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="492f7-108">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="492f7-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="492f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="492f7-109">EXAMPLES</span></span>

### <span data-ttu-id="492f7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="492f7-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="492f7-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="492f7-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="492f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="492f7-112">PARAMETERS</span></span>

### <span data-ttu-id="492f7-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="492f7-113">-Description</span></span>
<span data-ttu-id="492f7-114">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="492f7-114">Description of the plan.</span></span>

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

### <span data-ttu-id="492f7-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="492f7-115">-DisplayName</span></span>
<span data-ttu-id="492f7-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="492f7-116">Display name.</span></span>

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

### <span data-ttu-id="492f7-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="492f7-117">-ExternalReferenceId</span></span>
<span data-ttu-id="492f7-118">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="492f7-118">External reference identifier.</span></span>

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

### <span data-ttu-id="492f7-119">-ID</span><span class="sxs-lookup"><span data-stu-id="492f7-119">-Id</span></span>
<span data-ttu-id="492f7-120">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="492f7-120">URI of the resource.</span></span>

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

### <span data-ttu-id="492f7-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="492f7-121">-Location</span></span>
<span data-ttu-id="492f7-122">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="492f7-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="492f7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="492f7-123">-Name</span></span>
<span data-ttu-id="492f7-124">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="492f7-124">Name of the resource.</span></span>

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

### <span data-ttu-id="492f7-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="492f7-125">-QuotaIds</span></span>
<span data-ttu-id="492f7-126">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="492f7-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492f7-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="492f7-127">-SkuIds</span></span>
<span data-ttu-id="492f7-128">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="492f7-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492f7-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="492f7-129">-SubscriptionCount</span></span>
<span data-ttu-id="492f7-130">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="492f7-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492f7-131">-Tags</span><span class="sxs-lookup"><span data-stu-id="492f7-131">-Tags</span></span>
<span data-ttu-id="492f7-132">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="492f7-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="492f7-133">-Typ</span><span class="sxs-lookup"><span data-stu-id="492f7-133">-Type</span></span>
<span data-ttu-id="492f7-134">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="492f7-134">Type of resource.</span></span>

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

### <span data-ttu-id="492f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492f7-135">CommonParameters</span></span>
<span data-ttu-id="492f7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="492f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492f7-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="492f7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492f7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="492f7-138">INPUTS</span></span>

## <span data-ttu-id="492f7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="492f7-139">OUTPUTS</span></span>

## <span data-ttu-id="492f7-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="492f7-140">NOTES</span></span>

## <span data-ttu-id="492f7-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="492f7-141">RELATED LINKS</span></span>

