---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828136"
---
# <span data-ttu-id="eb556-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="eb556-101">New-OfferObject</span></span>

## <span data-ttu-id="eb556-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb556-102">SYNOPSIS</span></span>
<span data-ttu-id="eb556-103">Stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb556-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="eb556-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb556-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="eb556-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb556-105">DESCRIPTION</span></span>
<span data-ttu-id="eb556-106">Stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb556-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="eb556-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb556-107">EXAMPLES</span></span>

### <span data-ttu-id="eb556-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eb556-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="eb556-109">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="eb556-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="eb556-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb556-110">PARAMETERS</span></span>

### <span data-ttu-id="eb556-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="eb556-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="eb556-112">Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="eb556-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb556-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="eb556-113">-BasePlanIds</span></span>
<span data-ttu-id="eb556-114">Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="eb556-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb556-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb556-115">-Description</span></span>
<span data-ttu-id="eb556-116">Angebotsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="eb556-116">Description of offer.</span></span>

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

### <span data-ttu-id="eb556-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb556-117">-DisplayName</span></span>
<span data-ttu-id="eb556-118">Anzeigename des Angebots.</span><span class="sxs-lookup"><span data-stu-id="eb556-118">Display name of offer.</span></span>

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

### <span data-ttu-id="eb556-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="eb556-119">-ExternalReferenceId</span></span>
<span data-ttu-id="eb556-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="eb556-120">External reference identifier.</span></span>

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

### <span data-ttu-id="eb556-121">-ID</span><span class="sxs-lookup"><span data-stu-id="eb556-121">-Id</span></span>
<span data-ttu-id="eb556-122">Der URI der Ressource.</span><span class="sxs-lookup"><span data-stu-id="eb556-122">URI of the resource.</span></span>

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

### <span data-ttu-id="eb556-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="eb556-123">-Location</span></span>
<span data-ttu-id="eb556-124">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="eb556-124">Location where resource is location.</span></span>

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

### <span data-ttu-id="eb556-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="eb556-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="eb556-126">Maximale Abonnements pro Konto.</span><span class="sxs-lookup"><span data-stu-id="eb556-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb556-127">-Name</span><span class="sxs-lookup"><span data-stu-id="eb556-127">-Name</span></span>
<span data-ttu-id="eb556-128">Der Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="eb556-128">Name of the resource.</span></span>

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

### <span data-ttu-id="eb556-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="eb556-129">-State</span></span>
<span data-ttu-id="eb556-130">Barrierefreien Status anbieten.</span><span class="sxs-lookup"><span data-stu-id="eb556-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="eb556-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="eb556-131">-SubscriptionCount</span></span>
<span data-ttu-id="eb556-132">Aktuelle Abonnementanzahl.</span><span class="sxs-lookup"><span data-stu-id="eb556-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb556-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="eb556-133">-Tags</span></span>
<span data-ttu-id="eb556-134">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="eb556-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb556-135">-Typ</span><span class="sxs-lookup"><span data-stu-id="eb556-135">-Type</span></span>
<span data-ttu-id="eb556-136">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="eb556-136">Type of resource.</span></span>

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

### <span data-ttu-id="eb556-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb556-137">CommonParameters</span></span>
<span data-ttu-id="eb556-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb556-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb556-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb556-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb556-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb556-140">INPUTS</span></span>

## <span data-ttu-id="eb556-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb556-141">OUTPUTS</span></span>

## <span data-ttu-id="eb556-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb556-142">NOTES</span></span>

## <span data-ttu-id="eb556-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb556-143">RELATED LINKS</span></span>

