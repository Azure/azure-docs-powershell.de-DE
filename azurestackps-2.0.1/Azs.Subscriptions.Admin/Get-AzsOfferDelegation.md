---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005493"
---
# <span data-ttu-id="d6a29-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d6a29-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="d6a29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6a29-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a29-103">Abrufen der angegebenen Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="d6a29-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="d6a29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6a29-104">SYNTAX</span></span>

### <span data-ttu-id="d6a29-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6a29-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a29-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="d6a29-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d6a29-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6a29-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6a29-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6a29-108">DESCRIPTION</span></span>
<span data-ttu-id="d6a29-109">Abrufen der angegebenen Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="d6a29-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="d6a29-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6a29-110">EXAMPLES</span></span>

### <span data-ttu-id="d6a29-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6a29-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="d6a29-112">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="d6a29-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="d6a29-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a29-113">PARAMETERS</span></span>

### <span data-ttu-id="d6a29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a29-114">-DefaultProfile</span></span>
<span data-ttu-id="d6a29-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6a29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6a29-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d6a29-116">-InputObject</span></span>
<span data-ttu-id="d6a29-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d6a29-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6a29-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d6a29-118">-Name</span></span>
<span data-ttu-id="d6a29-119">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="d6a29-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="d6a29-120">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="d6a29-120">-OfferName</span></span>
<span data-ttu-id="d6a29-121">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="d6a29-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6a29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a29-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6a29-123">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d6a29-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d6a29-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d6a29-124">-SubscriptionId</span></span>
<span data-ttu-id="d6a29-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d6a29-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6a29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a29-126">CommonParameters</span></span>
<span data-ttu-id="d6a29-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a29-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6a29-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a29-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6a29-129">INPUTS</span></span>

### <span data-ttu-id="d6a29-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d6a29-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d6a29-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6a29-131">OUTPUTS</span></span>

### <span data-ttu-id="d6a29-132">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="d6a29-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="d6a29-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="d6a29-133">ALIASES</span></span>

## <span data-ttu-id="d6a29-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6a29-134">NOTES</span></span>

<span data-ttu-id="d6a29-135">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d6a29-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6a29-136">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d6a29-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d6a29-137">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d6a29-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6a29-138">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d6a29-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d6a29-139">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d6a29-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d6a29-140">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d6a29-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6a29-141">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d6a29-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d6a29-142">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="d6a29-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d6a29-143">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="d6a29-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d6a29-144">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="d6a29-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d6a29-145">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="d6a29-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d6a29-146">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="d6a29-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d6a29-147">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d6a29-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d6a29-148">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="d6a29-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d6a29-149">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d6a29-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d6a29-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d6a29-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d6a29-151">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d6a29-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d6a29-152">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="d6a29-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d6a29-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6a29-153">RELATED LINKS</span></span>

