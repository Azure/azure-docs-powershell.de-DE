---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005457"
---
# <span data-ttu-id="a3462-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="a3462-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="a3462-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3462-102">SYNOPSIS</span></span>
<span data-ttu-id="a3462-103">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3462-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="a3462-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3462-104">SYNTAX</span></span>

### <span data-ttu-id="a3462-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3462-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3462-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a3462-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3462-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3462-107">DESCRIPTION</span></span>
<span data-ttu-id="a3462-108">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3462-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="a3462-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3462-109">EXAMPLES</span></span>

### <span data-ttu-id="a3462-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3462-110">Example 1</span></span>
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

<span data-ttu-id="a3462-111">Aktualisiert ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="a3462-111">Updates a subscription</span></span>

## <span data-ttu-id="a3462-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3462-112">PARAMETERS</span></span>

### <span data-ttu-id="a3462-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3462-113">-DefaultProfile</span></span>
<span data-ttu-id="a3462-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3462-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3462-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3462-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="a3462-116">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a3462-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="a3462-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3462-117">-DisplayName</span></span>
<span data-ttu-id="a3462-118">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a3462-118">Subscription name.</span></span>

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

### <span data-ttu-id="a3462-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="a3462-119">-ExternalReferenceId</span></span>
<span data-ttu-id="a3462-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a3462-120">External reference identifier.</span></span>

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

### <span data-ttu-id="a3462-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a3462-121">-Id</span></span>
<span data-ttu-id="a3462-122">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a3462-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="a3462-123">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="a3462-123">-OfferId</span></span>
<span data-ttu-id="a3462-124">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a3462-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="a3462-125">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="a3462-125">-Owner</span></span>
<span data-ttu-id="a3462-126">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a3462-126">Subscription owner.</span></span>

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

### <span data-ttu-id="a3462-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="a3462-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="a3462-128">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="a3462-128">Routing resource manager type.</span></span>

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

### <span data-ttu-id="a3462-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="a3462-129">-State</span></span>
<span data-ttu-id="a3462-130">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a3462-130">Subscription state.</span></span>

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

### <span data-ttu-id="a3462-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a3462-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="a3462-132">Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3462-132">Subscription object properties.</span></span>
<span data-ttu-id="a3462-133">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SUBSCRIPTIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a3462-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3462-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a3462-134">-SubscriptionId</span></span>
<span data-ttu-id="a3462-135">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a3462-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3462-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="a3462-136">-SubscriptionId1</span></span>
<span data-ttu-id="a3462-137">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3462-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="a3462-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3462-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="a3462-139">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3462-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="a3462-140">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="a3462-140">-TenantId</span></span>
<span data-ttu-id="a3462-141">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="a3462-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="a3462-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3462-142">-Confirm</span></span>
<span data-ttu-id="a3462-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3462-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3462-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3462-144">-WhatIf</span></span>
<span data-ttu-id="a3462-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3462-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3462-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3462-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3462-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3462-147">CommonParameters</span></span>
<span data-ttu-id="a3462-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3462-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3462-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3462-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3462-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3462-150">INPUTS</span></span>

### <span data-ttu-id="a3462-151">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a3462-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="a3462-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3462-152">OUTPUTS</span></span>

### <span data-ttu-id="a3462-153">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="a3462-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="a3462-154">Aliase</span><span class="sxs-lookup"><span data-stu-id="a3462-154">ALIASES</span></span>

## <span data-ttu-id="a3462-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3462-155">NOTES</span></span>

<span data-ttu-id="a3462-156">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3462-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3462-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a3462-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a3462-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a3462-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="a3462-159">`[DelegatedProviderSubscriptionId <String>]`: Übergeordneter DelegatedProvider-Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a3462-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="a3462-160">`[DisplayName <String>]`: Abonnementname.</span><span class="sxs-lookup"><span data-stu-id="a3462-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="a3462-161">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="a3462-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="a3462-162">`[Id <String>]`: Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a3462-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="a3462-163">`[OfferId <String>]`: Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a3462-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="a3462-164">`[Owner <String>]`: Abonnementbesitzer.</span><span class="sxs-lookup"><span data-stu-id="a3462-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="a3462-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="a3462-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="a3462-166">`[State <SubscriptionState?>]`: Abonnement Zustand.</span><span class="sxs-lookup"><span data-stu-id="a3462-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="a3462-167">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a3462-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="a3462-168">`[TenantId <String>]`: Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="a3462-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="a3462-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3462-169">RELATED LINKS</span></span>

