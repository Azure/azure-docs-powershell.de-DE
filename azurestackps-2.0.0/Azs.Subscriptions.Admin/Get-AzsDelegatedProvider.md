---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005341"
---
# <span data-ttu-id="15244-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="15244-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="15244-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15244-102">SYNOPSIS</span></span>
<span data-ttu-id="15244-103">Abrufen des angegebenen Delegierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="15244-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="15244-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15244-104">SYNTAX</span></span>

### <span data-ttu-id="15244-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="15244-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15244-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="15244-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15244-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15244-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="15244-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15244-108">DESCRIPTION</span></span>
<span data-ttu-id="15244-109">Abrufen des angegebenen Delegierten Anbieters</span><span class="sxs-lookup"><span data-stu-id="15244-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="15244-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15244-110">EXAMPLES</span></span>

### <span data-ttu-id="15244-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15244-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="15244-112">Besorgen Sie sich einen bestimmten Delegierten Anbieter.</span><span class="sxs-lookup"><span data-stu-id="15244-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="15244-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="15244-113">PARAMETERS</span></span>

### <span data-ttu-id="15244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15244-114">-DefaultProfile</span></span>
<span data-ttu-id="15244-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15244-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15244-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="15244-116">-DelegatedProviderId</span></span>
<span data-ttu-id="15244-117">DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="15244-117">DelegatedProvider identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15244-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15244-118">-InputObject</span></span>
<span data-ttu-id="15244-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="15244-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="15244-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="15244-120">-SubscriptionId</span></span>
<span data-ttu-id="15244-121">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="15244-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15244-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15244-122">CommonParameters</span></span>
<span data-ttu-id="15244-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15244-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15244-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15244-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15244-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15244-125">INPUTS</span></span>

### <span data-ttu-id="15244-126">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="15244-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="15244-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15244-127">OUTPUTS</span></span>

### <span data-ttu-id="15244-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="15244-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="15244-129">Aliase</span><span class="sxs-lookup"><span data-stu-id="15244-129">ALIASES</span></span>

## <span data-ttu-id="15244-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="15244-130">NOTES</span></span>

<span data-ttu-id="15244-131">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15244-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15244-132">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="15244-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="15244-133">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="15244-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15244-134">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="15244-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="15244-135">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="15244-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="15244-136">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="15244-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15244-137">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="15244-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="15244-138">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="15244-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="15244-139">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="15244-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="15244-140">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="15244-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="15244-141">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="15244-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="15244-142">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="15244-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="15244-143">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="15244-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="15244-144">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="15244-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="15244-145">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="15244-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="15244-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="15244-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="15244-147">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="15244-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="15244-148">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="15244-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="15244-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15244-149">RELATED LINKS</span></span>

