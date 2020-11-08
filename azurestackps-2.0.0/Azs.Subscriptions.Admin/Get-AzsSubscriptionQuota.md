---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005293"
---
# <span data-ttu-id="81801-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="81801-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="81801-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81801-102">SYNOPSIS</span></span>
<span data-ttu-id="81801-103">Ruft ein Kontingent nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="81801-103">Gets a quota by name.</span></span>

## <span data-ttu-id="81801-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81801-104">SYNTAX</span></span>

### <span data-ttu-id="81801-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="81801-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="81801-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="81801-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81801-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81801-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="81801-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81801-108">DESCRIPTION</span></span>
<span data-ttu-id="81801-109">Ruft ein Kontingent nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="81801-109">Gets a quota by name.</span></span>

## <span data-ttu-id="81801-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81801-110">EXAMPLES</span></span>

### <span data-ttu-id="81801-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81801-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="81801-112">Rufen Sie die Liste der Abonnement Ressourcenanbieter Kontingente ab.</span><span class="sxs-lookup"><span data-stu-id="81801-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="81801-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="81801-113">PARAMETERS</span></span>

### <span data-ttu-id="81801-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81801-114">-DefaultProfile</span></span>
<span data-ttu-id="81801-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81801-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81801-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="81801-116">-InputObject</span></span>
<span data-ttu-id="81801-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="81801-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="81801-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="81801-118">-Location</span></span>
<span data-ttu-id="81801-119">Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="81801-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="81801-120">-Kontingent</span><span class="sxs-lookup"><span data-stu-id="81801-120">-Quota</span></span>
<span data-ttu-id="81801-121">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="81801-121">Name of the quota.</span></span>

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

### <span data-ttu-id="81801-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="81801-122">-SubscriptionId</span></span>
<span data-ttu-id="81801-123">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="81801-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="81801-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81801-124">CommonParameters</span></span>
<span data-ttu-id="81801-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81801-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81801-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81801-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81801-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81801-127">INPUTS</span></span>

### <span data-ttu-id="81801-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="81801-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="81801-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81801-129">OUTPUTS</span></span>

### <span data-ttu-id="81801-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="81801-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="81801-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="81801-131">ALIASES</span></span>

<span data-ttu-id="81801-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="81801-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="81801-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="81801-133">NOTES</span></span>

<span data-ttu-id="81801-134">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="81801-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81801-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="81801-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="81801-136">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="81801-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81801-137">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="81801-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="81801-138">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="81801-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="81801-139">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="81801-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81801-140">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="81801-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="81801-141">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="81801-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="81801-142">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="81801-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="81801-143">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="81801-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="81801-144">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="81801-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="81801-145">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="81801-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="81801-146">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="81801-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="81801-147">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="81801-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="81801-148">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="81801-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="81801-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="81801-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="81801-150">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="81801-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="81801-151">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="81801-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="81801-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81801-152">RELATED LINKS</span></span>

