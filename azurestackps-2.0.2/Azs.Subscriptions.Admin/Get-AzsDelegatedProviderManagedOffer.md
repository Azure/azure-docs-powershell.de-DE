---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007359"
---
# <span data-ttu-id="1a35d-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="1a35d-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="1a35d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a35d-102">SYNOPSIS</span></span>
<span data-ttu-id="1a35d-103">Rufen Sie das angegebene Angebot für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="1a35d-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="1a35d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a35d-104">SYNTAX</span></span>

### <span data-ttu-id="1a35d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a35d-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1a35d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="1a35d-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1a35d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1a35d-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a35d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a35d-108">DESCRIPTION</span></span>
<span data-ttu-id="1a35d-109">Rufen Sie das angegebene Angebot für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="1a35d-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="1a35d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a35d-110">EXAMPLES</span></span>

### <span data-ttu-id="1a35d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a35d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="1a35d-112">Rufen Sie die Liste der Angebote für Delegierte Anbieter ab.</span><span class="sxs-lookup"><span data-stu-id="1a35d-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="1a35d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a35d-113">PARAMETERS</span></span>

### <span data-ttu-id="1a35d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a35d-114">-DefaultProfile</span></span>
<span data-ttu-id="1a35d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a35d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a35d-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a35d-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="1a35d-117">Bezeichner des Delegierten Anbieter Abonnements</span><span class="sxs-lookup"><span data-stu-id="1a35d-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1a35d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a35d-118">-InputObject</span></span>
<span data-ttu-id="1a35d-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="1a35d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1a35d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1a35d-120">-Name</span></span>
<span data-ttu-id="1a35d-121">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="1a35d-121">Name of an offer.</span></span>

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

### <span data-ttu-id="1a35d-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="1a35d-122">-SubscriptionId</span></span>
<span data-ttu-id="1a35d-123">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1a35d-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1a35d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a35d-124">CommonParameters</span></span>
<span data-ttu-id="1a35d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a35d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a35d-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a35d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a35d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a35d-127">INPUTS</span></span>

### <span data-ttu-id="1a35d-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1a35d-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="1a35d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a35d-129">OUTPUTS</span></span>

### <span data-ttu-id="1a35d-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="1a35d-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="1a35d-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="1a35d-131">ALIASES</span></span>

## <span data-ttu-id="1a35d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a35d-132">NOTES</span></span>

<span data-ttu-id="1a35d-133">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1a35d-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a35d-134">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="1a35d-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1a35d-135">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="1a35d-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a35d-136">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1a35d-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="1a35d-137">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="1a35d-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="1a35d-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="1a35d-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a35d-139">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1a35d-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="1a35d-140">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="1a35d-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="1a35d-141">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="1a35d-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="1a35d-142">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="1a35d-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="1a35d-143">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="1a35d-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="1a35d-144">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="1a35d-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="1a35d-145">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1a35d-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="1a35d-146">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="1a35d-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1a35d-147">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="1a35d-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="1a35d-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="1a35d-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1a35d-149">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="1a35d-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="1a35d-150">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="1a35d-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="1a35d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a35d-151">RELATED LINKS</span></span>

