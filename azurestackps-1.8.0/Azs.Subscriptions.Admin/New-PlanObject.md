---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827480"
---
# <span data-ttu-id="adde5-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="adde5-101">New-PlanObject</span></span>

## <span data-ttu-id="adde5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="adde5-102">SYNOPSIS</span></span>
<span data-ttu-id="adde5-103">Ein Plan steht für ein Paket von Kontingenten und Funktionen, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="adde5-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="adde5-104">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="adde5-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="adde5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="adde5-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="adde5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adde5-106">DESCRIPTION</span></span>
<span data-ttu-id="adde5-107">Ein Plan steht für ein Paket von Kontingenten und Funktionen, die Mandanten angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="adde5-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="adde5-108">Ein Mandant kann diesen Plan über ein Angebot erwerben, um seinen Zugriff auf die zugrunde liegenden Cloud-Services zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="adde5-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="adde5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="adde5-109">EXAMPLES</span></span>

### <span data-ttu-id="adde5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="adde5-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="adde5-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="adde5-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="adde5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="adde5-112">PARAMETERS</span></span>

### <span data-ttu-id="adde5-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="adde5-113">-Description</span></span>
<span data-ttu-id="adde5-114">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="adde5-114">Description of the plan.</span></span>

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

### <span data-ttu-id="adde5-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="adde5-115">-DisplayName</span></span>
<span data-ttu-id="adde5-116">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="adde5-116">Display name.</span></span>

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

### <span data-ttu-id="adde5-117">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="adde5-117">-ExternalReferenceId</span></span>
<span data-ttu-id="adde5-118">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="adde5-118">External reference identifier.</span></span>

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

### <span data-ttu-id="adde5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="adde5-119">-Id</span></span>
<span data-ttu-id="adde5-120">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="adde5-120">URI of the resource.</span></span>

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

### <span data-ttu-id="adde5-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="adde5-121">-Location</span></span>
<span data-ttu-id="adde5-122">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="adde5-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="adde5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="adde5-123">-Name</span></span>
<span data-ttu-id="adde5-124">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="adde5-124">Name of the resource.</span></span>

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

### <span data-ttu-id="adde5-125">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="adde5-125">-QuotaIds</span></span>
<span data-ttu-id="adde5-126">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="adde5-126">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="adde5-127">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="adde5-127">-SkuIds</span></span>
<span data-ttu-id="adde5-128">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="adde5-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="adde5-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="adde5-129">-SubscriptionCount</span></span>
<span data-ttu-id="adde5-130">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="adde5-130">Subscription count.</span></span>

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

### <span data-ttu-id="adde5-131">-Tags</span><span class="sxs-lookup"><span data-stu-id="adde5-131">-Tags</span></span>
<span data-ttu-id="adde5-132">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="adde5-132">List of key-value pairs.</span></span>

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

### <span data-ttu-id="adde5-133">-Typ</span><span class="sxs-lookup"><span data-stu-id="adde5-133">-Type</span></span>
<span data-ttu-id="adde5-134">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="adde5-134">Type of resource.</span></span>

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

### <span data-ttu-id="adde5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adde5-135">CommonParameters</span></span>
<span data-ttu-id="adde5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adde5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adde5-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adde5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adde5-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="adde5-138">INPUTS</span></span>

## <span data-ttu-id="adde5-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="adde5-139">OUTPUTS</span></span>

## <span data-ttu-id="adde5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="adde5-140">NOTES</span></span>

## <span data-ttu-id="adde5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="adde5-141">RELATED LINKS</span></span>

