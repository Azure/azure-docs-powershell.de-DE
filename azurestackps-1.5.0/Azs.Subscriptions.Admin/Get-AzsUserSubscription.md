---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662003"
---
# <span data-ttu-id="aa5bc-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="aa5bc-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="aa5bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5bc-103">Rufen Sie die Liste der Benutzer Abonnements als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="aa5bc-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="aa5bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5bc-104">SYNTAX</span></span>

### <span data-ttu-id="aa5bc-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa5bc-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa5bc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="aa5bc-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="aa5bc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa5bc-107">DESCRIPTION</span></span>
<span data-ttu-id="aa5bc-108">Rufen Sie die Liste der Benutzer Abonnements als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="aa5bc-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="aa5bc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa5bc-109">EXAMPLES</span></span>

### <span data-ttu-id="aa5bc-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa5bc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="aa5bc-111">Rufen Sie die Liste der Benutzer Abonnements als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="aa5bc-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="aa5bc-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5bc-112">PARAMETERS</span></span>

### <span data-ttu-id="aa5bc-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="aa5bc-113">-Filter</span></span>
<span data-ttu-id="aa5bc-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="aa5bc-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="aa5bc-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="aa5bc-115">-SubscriptionId</span></span>
<span data-ttu-id="aa5bc-116">Parameter für die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="aa5bc-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="aa5bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5bc-117">CommonParameters</span></span>
<span data-ttu-id="aa5bc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa5bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5bc-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa5bc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5bc-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa5bc-120">INPUTS</span></span>

## <span data-ttu-id="aa5bc-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa5bc-121">OUTPUTS</span></span>

### <span data-ttu-id="aa5bc-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="aa5bc-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="aa5bc-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa5bc-123">NOTES</span></span>

## <span data-ttu-id="aa5bc-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa5bc-124">RELATED LINKS</span></span>

