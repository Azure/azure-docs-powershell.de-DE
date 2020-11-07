---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827860"
---
# <span data-ttu-id="e1e38-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e1e38-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="e1e38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1e38-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e38-103">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="e1e38-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e1e38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1e38-104">SYNTAX</span></span>

### <span data-ttu-id="e1e38-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1e38-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="e1e38-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="e1e38-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="e1e38-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1e38-107">DESCRIPTION</span></span>
<span data-ttu-id="e1e38-108">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="e1e38-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e1e38-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1e38-109">EXAMPLES</span></span>

### <span data-ttu-id="e1e38-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1e38-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="e1e38-111">Rufen Sie die Liste der Benutzer Abonnements als Administrator ab.</span><span class="sxs-lookup"><span data-stu-id="e1e38-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e1e38-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1e38-112">PARAMETERS</span></span>

### <span data-ttu-id="e1e38-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="e1e38-113">-Filter</span></span>
<span data-ttu-id="e1e38-114">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="e1e38-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="e1e38-115">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e1e38-115">-SubscriptionId</span></span>
<span data-ttu-id="e1e38-116">Parameter für die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e1e38-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="e1e38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e38-117">CommonParameters</span></span>
<span data-ttu-id="e1e38-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e38-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1e38-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e38-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1e38-120">INPUTS</span></span>

## <span data-ttu-id="e1e38-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1e38-121">OUTPUTS</span></span>

### <span data-ttu-id="e1e38-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="e1e38-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e1e38-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1e38-123">NOTES</span></span>

## <span data-ttu-id="e1e38-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1e38-124">RELATED LINKS</span></span>

