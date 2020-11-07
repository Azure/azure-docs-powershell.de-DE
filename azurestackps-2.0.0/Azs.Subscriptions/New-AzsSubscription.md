---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840963"
---
# <span data-ttu-id="fb32c-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="fb32c-101">New-AzsSubscription</span></span>

## <span data-ttu-id="fb32c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb32c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb32c-103">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="fb32c-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="fb32c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb32c-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fb32c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb32c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb32c-106">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="fb32c-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="fb32c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb32c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb32c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb32c-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="fb32c-109">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb32c-109">Create a subscription.</span></span>

## <span data-ttu-id="fb32c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb32c-110">PARAMETERS</span></span>

### <span data-ttu-id="fb32c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb32c-111">-DefaultProfile</span></span>
<span data-ttu-id="fb32c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb32c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fb32c-113">-DisplayName</span></span>
<span data-ttu-id="fb32c-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fb32c-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-115">-ID</span><span class="sxs-lookup"><span data-stu-id="fb32c-115">-Id</span></span>
<span data-ttu-id="fb32c-116">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="fb32c-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-117">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="fb32c-117">-OfferId</span></span>
<span data-ttu-id="fb32c-118">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="fb32c-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-119">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="fb32c-119">-State</span></span>
<span data-ttu-id="fb32c-120">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fb32c-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-121">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="fb32c-121">-SubscriptionId</span></span>
<span data-ttu-id="fb32c-122">Die ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fb32c-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-123">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="fb32c-123">-TenantId</span></span>
<span data-ttu-id="fb32c-124">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="fb32c-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb32c-125">-Confirm</span></span>
<span data-ttu-id="fb32c-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb32c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb32c-127">-WhatIf</span></span>
<span data-ttu-id="fb32c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb32c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb32c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb32c-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fb32c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb32c-130">CommonParameters</span></span>
<span data-ttu-id="fb32c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb32c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb32c-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb32c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb32c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb32c-133">INPUTS</span></span>

## <span data-ttu-id="fb32c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb32c-134">OUTPUTS</span></span>

### <span data-ttu-id="fb32c-135">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="fb32c-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="fb32c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb32c-136">NOTES</span></span>

## <span data-ttu-id="fb32c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb32c-137">RELATED LINKS</span></span>

