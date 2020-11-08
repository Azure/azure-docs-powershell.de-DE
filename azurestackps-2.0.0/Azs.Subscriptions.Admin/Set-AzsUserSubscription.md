---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005307"
---
# <span data-ttu-id="1e88f-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="1e88f-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="1e88f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e88f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e88f-103">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e88f-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="1e88f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e88f-104">SYNTAX</span></span>

### <span data-ttu-id="1e88f-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e88f-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e88f-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1e88f-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e88f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e88f-107">DESCRIPTION</span></span>
<span data-ttu-id="1e88f-108">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e88f-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="1e88f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e88f-109">EXAMPLES</span></span>

### <span data-ttu-id="1e88f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e88f-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="1e88f-111">Aktualisiert ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e88f-111">Updates a subscription</span></span>

## <span data-ttu-id="1e88f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e88f-112">PARAMETERS</span></span>

### <span data-ttu-id="1e88f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e88f-113">-DefaultProfile</span></span>
<span data-ttu-id="1e88f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e88f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e88f-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e88f-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="1e88f-116">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e88f-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="1e88f-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1e88f-117">-DisplayName</span></span>
<span data-ttu-id="1e88f-118">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e88f-118">Subscription name.</span></span>

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

### <span data-ttu-id="1e88f-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="1e88f-119">-ExternalReferenceId</span></span>
<span data-ttu-id="1e88f-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e88f-120">External reference identifier.</span></span>

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

### <span data-ttu-id="1e88f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1e88f-121">-Id</span></span>
<span data-ttu-id="1e88f-122">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e88f-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="1e88f-123">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="1e88f-123">-OfferId</span></span>
<span data-ttu-id="1e88f-124">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1e88f-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="1e88f-125">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="1e88f-125">-Owner</span></span>
<span data-ttu-id="1e88f-126">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e88f-126">Subscription owner.</span></span>

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

### <span data-ttu-id="1e88f-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="1e88f-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="1e88f-128">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="1e88f-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1e88f-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="1e88f-129">-State</span></span>
<span data-ttu-id="1e88f-130">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1e88f-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1e88f-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1e88f-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="1e88f-132">Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e88f-132">Subscription object properties.</span></span>
<span data-ttu-id="1e88f-133">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SUBSCRIPTIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1e88f-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1e88f-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1e88f-134">-SubscriptionId</span></span>
<span data-ttu-id="1e88f-135">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1e88f-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1e88f-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="1e88f-136">-SubscriptionId1</span></span>
<span data-ttu-id="1e88f-137">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1e88f-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="1e88f-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e88f-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="1e88f-139">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1e88f-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="1e88f-140">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="1e88f-140">-TenantId</span></span>
<span data-ttu-id="1e88f-141">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="1e88f-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="1e88f-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e88f-142">-Confirm</span></span>
<span data-ttu-id="1e88f-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e88f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e88f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e88f-144">-WhatIf</span></span>
<span data-ttu-id="1e88f-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e88f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e88f-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e88f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e88f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e88f-147">CommonParameters</span></span>
<span data-ttu-id="1e88f-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e88f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e88f-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e88f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e88f-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e88f-150">INPUTS</span></span>

### <span data-ttu-id="1e88f-151">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1e88f-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="1e88f-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e88f-152">OUTPUTS</span></span>

### <span data-ttu-id="1e88f-153">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1e88f-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="1e88f-154">Aliase</span><span class="sxs-lookup"><span data-stu-id="1e88f-154">ALIASES</span></span>

## <span data-ttu-id="1e88f-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e88f-155">NOTES</span></span>

<span data-ttu-id="1e88f-156">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e88f-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e88f-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="1e88f-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1e88f-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e88f-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="1e88f-159">`[DelegatedProviderSubscriptionId <String>]`: Übergeordneter DelegatedProvider-Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e88f-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="1e88f-160">`[DisplayName <String>]`: Abonnementname.</span><span class="sxs-lookup"><span data-stu-id="1e88f-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="1e88f-161">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e88f-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="1e88f-162">`[Id <String>]`: Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1e88f-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="1e88f-163">`[OfferId <String>]`: Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="1e88f-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="1e88f-164">`[Owner <String>]`: Abonnementbesitzer.</span><span class="sxs-lookup"><span data-stu-id="1e88f-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="1e88f-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="1e88f-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="1e88f-166">`[State <SubscriptionState?>]`: Abonnement Zustand.</span><span class="sxs-lookup"><span data-stu-id="1e88f-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="1e88f-167">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1e88f-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="1e88f-168">`[TenantId <String>]`: Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="1e88f-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="1e88f-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e88f-169">RELATED LINKS</span></span>

