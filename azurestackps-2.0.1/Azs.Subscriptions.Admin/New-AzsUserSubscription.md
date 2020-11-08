---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005385"
---
# <span data-ttu-id="533f4-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="533f4-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="533f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="533f4-102">SYNOPSIS</span></span>
<span data-ttu-id="533f4-103">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="533f4-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="533f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="533f4-104">SYNTAX</span></span>

### <span data-ttu-id="533f4-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="533f4-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="533f4-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="533f4-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="533f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="533f4-107">DESCRIPTION</span></span>
<span data-ttu-id="533f4-108">Erstellt oder aktualisiert das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="533f4-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="533f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="533f4-109">EXAMPLES</span></span>

### <span data-ttu-id="533f4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="533f4-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="533f4-111">Erstellt ein neues Benutzer Abonnement</span><span class="sxs-lookup"><span data-stu-id="533f4-111">Creates a new user subscription</span></span>

## <span data-ttu-id="533f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="533f4-112">PARAMETERS</span></span>

### <span data-ttu-id="533f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533f4-113">-DefaultProfile</span></span>
<span data-ttu-id="533f4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="533f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="533f4-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="533f4-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="533f4-116">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="533f4-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="533f4-117">-DisplayName</span></span>
<span data-ttu-id="533f4-118">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="533f4-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="533f4-119">-ExternalReferenceId</span></span>
<span data-ttu-id="533f4-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="533f4-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="533f4-121">-Id</span></span>
<span data-ttu-id="533f4-122">Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="533f4-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-123">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="533f4-123">-OfferId</span></span>
<span data-ttu-id="533f4-124">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="533f4-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-125">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="533f4-125">-Owner</span></span>
<span data-ttu-id="533f4-126">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="533f4-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="533f4-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="533f4-128">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="533f4-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="533f4-129">-State</span></span>
<span data-ttu-id="533f4-130">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="533f4-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="533f4-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="533f4-132">Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="533f4-132">Subscription object properties.</span></span>
<span data-ttu-id="533f4-133">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SUBSCRIPTIONDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="533f4-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="533f4-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="533f4-135">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="533f4-135">The target subscription ID.</span></span>

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

### <span data-ttu-id="533f4-136">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="533f4-136">-TenantId</span></span>
<span data-ttu-id="533f4-137">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="533f4-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="533f4-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="533f4-138">-Confirm</span></span>
<span data-ttu-id="533f4-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="533f4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="533f4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="533f4-140">-WhatIf</span></span>
<span data-ttu-id="533f4-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="533f4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="533f4-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="533f4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="533f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533f4-143">CommonParameters</span></span>
<span data-ttu-id="533f4-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="533f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533f4-145">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="533f4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533f4-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="533f4-146">INPUTS</span></span>

### <span data-ttu-id="533f4-147">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="533f4-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="533f4-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="533f4-148">OUTPUTS</span></span>

### <span data-ttu-id="533f4-149">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="533f4-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="533f4-150">Aliase</span><span class="sxs-lookup"><span data-stu-id="533f4-150">ALIASES</span></span>

## <span data-ttu-id="533f4-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="533f4-151">NOTES</span></span>

<span data-ttu-id="533f4-152">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="533f4-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="533f4-153">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="533f4-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="533f4-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : Abonnementobjekt Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="533f4-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="533f4-155">`[DelegatedProviderSubscriptionId <String>]`: Übergeordneter DelegatedProvider-Abonnementbezeichner.</span><span class="sxs-lookup"><span data-stu-id="533f4-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="533f4-156">`[DisplayName <String>]`: Abonnementname.</span><span class="sxs-lookup"><span data-stu-id="533f4-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="533f4-157">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="533f4-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="533f4-158">`[Id <String>]`: Vollqualifizierter Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="533f4-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="533f4-159">`[OfferId <String>]`: Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="533f4-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="533f4-160">`[Owner <String>]`: Abonnementbesitzer.</span><span class="sxs-lookup"><span data-stu-id="533f4-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="533f4-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="533f4-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="533f4-162">`[State <SubscriptionState?>]`: Abonnement Zustand.</span><span class="sxs-lookup"><span data-stu-id="533f4-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="533f4-163">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="533f4-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="533f4-164">`[TenantId <String>]`: Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="533f4-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="533f4-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="533f4-165">RELATED LINKS</span></span>

