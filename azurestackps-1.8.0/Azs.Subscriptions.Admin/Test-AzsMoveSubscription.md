---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a04836e2d361f4c9686fa5dfe62babfa57ade189
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827795"
---
# <span data-ttu-id="007d0-101">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="007d0-101">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="007d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="007d0-102">SYNOPSIS</span></span>
<span data-ttu-id="007d0-103">Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="007d0-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="007d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="007d0-104">SYNTAX</span></span>

```
Test-AzsMoveSubscription [[-DestinationDelegatedProviderOffer] <String>] [-ResourceId] <String[]> [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="007d0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="007d0-105">DESCRIPTION</span></span>
<span data-ttu-id="007d0-106">Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="007d0-106">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="007d0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="007d0-107">EXAMPLES</span></span>

### <span data-ttu-id="007d0-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="007d0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test that user subscriptions can be moved to a delegated provider offer.
```

<span data-ttu-id="007d0-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/RO1"-Resourcen-"/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6"; "/Subscriptions/45ec4d39-8dea-4D26-A373-c176ec53717a/Providers/Microsoft.Subscriptions.admin/Subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span><span class="sxs-lookup"><span data-stu-id="007d0-109">Test-MoveSubscription \` -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1" -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"</span></span>

### <span data-ttu-id="007d0-110">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="007d0-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Test that user subscriptions can be moved from a delegated provider to the Default Provider.
```

<span data-ttu-id="007d0-111">$resourceIds = Get-AzsUserSubscription-Filter "Offername EQ ' O1 '" | SELECT-expando-ID Test-MoveSubscription-ResoruceId $resourceIds</span><span class="sxs-lookup"><span data-stu-id="007d0-111">$resourceIds = Get-AzsUserSubscription -Filter "offerName eq 'o1'" | Select -ExpandProperty Id Test-MoveSubscription -ResoruceId $resourceIds</span></span>

## <span data-ttu-id="007d0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="007d0-112">PARAMETERS</span></span>

### <span data-ttu-id="007d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="007d0-113">-AsJob</span></span>
<span data-ttu-id="007d0-114">Gibt an, ob der Verschiebevorgang als Job ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="007d0-114">Specifies whether the move operation is to be executed as a job.</span></span>

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

### <span data-ttu-id="007d0-115">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="007d0-115">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="007d0-116">Gibt das vollqualifizierte Anbieter Angebot für Delegierte an, in das dieses Cmdlet Abonnements verschiebt.</span><span class="sxs-lookup"><span data-stu-id="007d0-116">Specifies the fully qualified delegated provider offer into which this cmdlet moves subscriptions.</span></span>
<span data-ttu-id="007d0-117">NULL, wenn die Abonnements zurück zum Standardanbieter verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="007d0-117">NULL if the subscriptions are to be moved back to the Default Provider.</span></span>

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

### <span data-ttu-id="007d0-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="007d0-118">-ResourceId</span></span>
<span data-ttu-id="007d0-119">Gibt ein Array vollständig qualifizierter Abonnement Ressourcen-IDs an, die dieses Cmdlet verschiebt.</span><span class="sxs-lookup"><span data-stu-id="007d0-119">Specifies an array of fully qualified subscription resource identifiers that this cmdlet moves.</span></span>

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

### <span data-ttu-id="007d0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007d0-120">CommonParameters</span></span>
<span data-ttu-id="007d0-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007d0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007d0-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007d0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007d0-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="007d0-123">INPUTS</span></span>

## <span data-ttu-id="007d0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="007d0-124">OUTPUTS</span></span>

## <span data-ttu-id="007d0-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="007d0-125">NOTES</span></span>

## <span data-ttu-id="007d0-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="007d0-126">RELATED LINKS</span></span>

