---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005545"
---
# <span data-ttu-id="ba79d-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ba79d-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="ba79d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba79d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba79d-103">Besorgen Sie sich ein angegebenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba79d-103">Get a specified subscription.</span></span>

## <span data-ttu-id="ba79d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba79d-104">SYNTAX</span></span>

### <span data-ttu-id="ba79d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba79d-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba79d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ba79d-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba79d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba79d-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba79d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba79d-108">DESCRIPTION</span></span>
<span data-ttu-id="ba79d-109">Besorgen Sie sich ein angegebenes Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba79d-109">Get a specified subscription.</span></span>

## <span data-ttu-id="ba79d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba79d-110">EXAMPLES</span></span>

### <span data-ttu-id="ba79d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba79d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="ba79d-112">Rufen Sie die Liste der Benutzer Abonnements als Operator ab.</span><span class="sxs-lookup"><span data-stu-id="ba79d-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="ba79d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba79d-113">PARAMETERS</span></span>

### <span data-ttu-id="ba79d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba79d-114">-DefaultProfile</span></span>
<span data-ttu-id="ba79d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba79d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba79d-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="ba79d-116">-Filter</span></span>
<span data-ttu-id="ba79d-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="ba79d-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ba79d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ba79d-118">-InputObject</span></span>
<span data-ttu-id="ba79d-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ba79d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ba79d-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ba79d-120">-SubscriptionId</span></span>
<span data-ttu-id="ba79d-121">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ba79d-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba79d-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba79d-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="ba79d-123">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ba79d-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="ba79d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba79d-124">CommonParameters</span></span>
<span data-ttu-id="ba79d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba79d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba79d-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba79d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba79d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba79d-127">INPUTS</span></span>

### <span data-ttu-id="ba79d-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ba79d-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="ba79d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba79d-129">OUTPUTS</span></span>

### <span data-ttu-id="ba79d-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="ba79d-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="ba79d-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="ba79d-131">ALIASES</span></span>

## <span data-ttu-id="ba79d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba79d-132">NOTES</span></span>

<span data-ttu-id="ba79d-133">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba79d-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba79d-134">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ba79d-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ba79d-135">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ba79d-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba79d-136">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ba79d-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="ba79d-137">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="ba79d-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="ba79d-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ba79d-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba79d-139">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ba79d-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="ba79d-140">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="ba79d-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="ba79d-141">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="ba79d-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="ba79d-142">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="ba79d-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="ba79d-143">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="ba79d-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="ba79d-144">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="ba79d-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="ba79d-145">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ba79d-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="ba79d-146">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="ba79d-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="ba79d-147">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ba79d-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="ba79d-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ba79d-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ba79d-149">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ba79d-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="ba79d-150">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="ba79d-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="ba79d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba79d-151">RELATED LINKS</span></span>

