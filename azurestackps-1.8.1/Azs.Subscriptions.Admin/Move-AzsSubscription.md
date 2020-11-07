---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 987793101e89a7f628f575bf7353994756edaeae
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828167"
---
# <span data-ttu-id="0cc8f-101">Move-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="0cc8f-101">Move-AzsSubscription</span></span>

## <span data-ttu-id="0cc8f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cc8f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc8f-103">Verschieben von Abonnements zwischen Delegierten Anbieter angeboten</span><span class="sxs-lookup"><span data-stu-id="0cc8f-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="0cc8f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cc8f-104">SYNTAX</span></span>

```
Move-AzsSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="0cc8f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cc8f-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc8f-106">Verschieben von Abonnements zwischen Delegierten Anbieter angeboten</span><span class="sxs-lookup"><span data-stu-id="0cc8f-106">Move subscriptions between delegated provider offers.</span></span>
<span data-ttu-id="0cc8f-107">Dieser Vorgang führt nur zu einer Umbenennung, das zugrunde liegende Angebot, die Pläne, die Kontingente für die Abonnements werden nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-107">This process will only perform a rebranding, the underlying offer, plans, quotas for the subscriptions will not be altered.</span></span>

## <span data-ttu-id="0cc8f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cc8f-108">EXAMPLES</span></span>

### <span data-ttu-id="0cc8f-109">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cc8f-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Move user subscriptions to a delegated provider offer.
```

<span data-ttu-id="0cc8f-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-Resourcen-"/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="0cc8f-110">Move-AzsSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="0cc8f-111">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cc8f-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Move user subscriptions from a delegated provider to the Default Provider.
```

<span data-ttu-id="0cc8f-112">$resourceIds = Get-AzsUserSubscription-Filter "Offername EQ ' O1 '" | wobei {$ _. DelegatedProviderSubscriptionId-EQ "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | SELECT-expando-ID Move-AzsSubscription-resourcecode $resourceIds</span><span class="sxs-lookup"><span data-stu-id="0cc8f-112">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id Move-AzsSubscription -ResourceId $resourceIds</span></span>

## <span data-ttu-id="0cc8f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cc8f-113">PARAMETERS</span></span>

### <span data-ttu-id="0cc8f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cc8f-114">-AsJob</span></span>
<span data-ttu-id="0cc8f-115">Gibt an, ob der Verschiebevorgang als Job ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-115">Specifies whether the move operation is to be executed as a job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-116">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="0cc8f-116">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="0cc8f-117">Gibt das vollqualifizierte Anbieter Angebot für Delegierte an, in das dieses Cmdlet Abonnements verschiebt.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-117">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="0cc8f-118">NULL, wenn die Abonnements zurück zum Standardanbieter verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-118">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="0cc8f-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0cc8f-119">-ResourceId</span></span>
<span data-ttu-id="0cc8f-120">Gibt ein Array vollständig qualifizierter Abonnement Ressourcen-IDs an, die dieses Cmdlet verschiebt.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-120">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc8f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc8f-121">CommonParameters</span></span>
<span data-ttu-id="0cc8f-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc8f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc8f-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc8f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc8f-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cc8f-124">INPUTS</span></span>

## <span data-ttu-id="0cc8f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cc8f-125">OUTPUTS</span></span>

## <span data-ttu-id="0cc8f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cc8f-126">NOTES</span></span>

## <span data-ttu-id="0cc8f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cc8f-127">RELATED LINKS</span></span>

