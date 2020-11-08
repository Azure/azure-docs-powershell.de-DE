---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007191"
---
# <span data-ttu-id="1c02b-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="1c02b-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="1c02b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c02b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c02b-103">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="1c02b-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="1c02b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c02b-104">SYNTAX</span></span>

### <span data-ttu-id="1c02b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c02b-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c02b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1c02b-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="1c02b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c02b-107">DESCRIPTION</span></span>
<span data-ttu-id="1c02b-108">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="1c02b-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="1c02b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c02b-109">EXAMPLES</span></span>

### <span data-ttu-id="1c02b-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1c02b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="1c02b-111">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="1c02b-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="1c02b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c02b-112">PARAMETERS</span></span>

### <span data-ttu-id="1c02b-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="1c02b-113">-Filter</span></span>
<span data-ttu-id="1c02b-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="1c02b-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c02b-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1c02b-115">-SubscriptionId</span></span>
<span data-ttu-id="1c02b-116">Parameter für die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1c02b-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c02b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c02b-117">CommonParameters</span></span>
<span data-ttu-id="1c02b-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c02b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c02b-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c02b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c02b-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c02b-120">INPUTS</span></span>

## <span data-ttu-id="1c02b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c02b-121">OUTPUTS</span></span>

### <span data-ttu-id="1c02b-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="1c02b-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="1c02b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c02b-123">NOTES</span></span>

## <span data-ttu-id="1c02b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c02b-124">RELATED LINKS</span></span>

