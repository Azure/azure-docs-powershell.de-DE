---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/set-azssubscription
schema: 2.0.0
ms.openlocfilehash: d4636bb8f6e3fdbe9fc1911c173680f966e0f9e4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007226"
---
# <span data-ttu-id="5da86-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="5da86-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="5da86-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5da86-102">SYNOPSIS</span></span>
<span data-ttu-id="5da86-103">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="5da86-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="5da86-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5da86-104">SYNTAX</span></span>

### <span data-ttu-id="5da86-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5da86-105">UpdateExpanded (Default)</span></span>
```
Set-AzsSubscription -SubscriptionId <String> [-DisplayName <String>] [-Id <String>] [-OfferId <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5da86-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="5da86-106">Update</span></span>
```
Set-AzsSubscription -SubscriptionDefinition <ISubscription> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5da86-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5da86-107">DESCRIPTION</span></span>
<span data-ttu-id="5da86-108">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="5da86-108">Create or updates a subscription.</span></span>

## <span data-ttu-id="5da86-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5da86-109">EXAMPLES</span></span>

### <span data-ttu-id="5da86-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5da86-110">Example 1</span></span>
```powershell
PS C:\> $subscription = Get-AzsSubscription | where DisplayName -eq 'testsubscription'
$subscription.DisplayName = 'update subscription'
$subscription | Set-AzsSubscription | fl *

DisplayName    : update subscription
Id             : /subscriptions/f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
OfferId        : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
State          : Enabled
SubscriptionId : f6f9665e-9831-4ac6-a2c3-26a591b9e6e8
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="5da86-111">Aktualisiert ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5da86-111">Updates a subscription.</span></span>

## <span data-ttu-id="5da86-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5da86-112">PARAMETERS</span></span>

### <span data-ttu-id="5da86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da86-113">-DefaultProfile</span></span>
<span data-ttu-id="5da86-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5da86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5da86-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5da86-115">-DisplayName</span></span>
<span data-ttu-id="5da86-116">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5da86-116">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-117">-ID</span><span class="sxs-lookup"><span data-stu-id="5da86-117">-Id</span></span>
<span data-ttu-id="5da86-118">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5da86-118">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-119">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="5da86-119">-OfferId</span></span>
<span data-ttu-id="5da86-120">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="5da86-120">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-121">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="5da86-121">-State</span></span>
<span data-ttu-id="5da86-122">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5da86-122">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-123">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="5da86-123">-SubscriptionDefinition</span></span>
<span data-ttu-id="5da86-124">Liste der unterstützten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5da86-124">List of supported operations.</span></span>
<span data-ttu-id="5da86-125">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SUBSCRIPTIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5da86-125">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5da86-126">-SubscriptionId</span></span>
<span data-ttu-id="5da86-127">Die ID des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="5da86-127">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-128">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="5da86-128">-TenantId</span></span>
<span data-ttu-id="5da86-129">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="5da86-129">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5da86-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5da86-130">-Confirm</span></span>
<span data-ttu-id="5da86-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5da86-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da86-132">-WhatIf</span></span>
<span data-ttu-id="5da86-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5da86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da86-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5da86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da86-135">CommonParameters</span></span>
<span data-ttu-id="5da86-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da86-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da86-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5da86-138">INPUTS</span></span>

### <span data-ttu-id="5da86-139">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="5da86-139">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>

## <span data-ttu-id="5da86-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5da86-140">OUTPUTS</span></span>

### <span data-ttu-id="5da86-141">Microsoft. Azure. PowerShell. Cmdlets. Subscription. Models. Api20151101. ISubscription</span><span class="sxs-lookup"><span data-stu-id="5da86-141">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="5da86-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5da86-142">NOTES</span></span>

<span data-ttu-id="5da86-143">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5da86-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5da86-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5da86-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5da86-145">SUBSCRIPTIONDEFINITION <ISubscription> : Liste unterstützter Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="5da86-145">SUBSCRIPTIONDEFINITION <ISubscription>: List of supported operations.</span></span>
  - <span data-ttu-id="5da86-146">`[DisplayName <String>]`: Abonnementname.</span><span class="sxs-lookup"><span data-stu-id="5da86-146">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="5da86-147">`[Id <String>]`: Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="5da86-147">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="5da86-148">`[OfferId <String>]`: Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="5da86-148">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="5da86-149">`[State <SubscriptionState?>]`: Abonnement Zustand.</span><span class="sxs-lookup"><span data-stu-id="5da86-149">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="5da86-150">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="5da86-150">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="5da86-151">`[TenantId <String>]`: Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="5da86-151">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="5da86-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5da86-152">RELATED LINKS</span></span>

