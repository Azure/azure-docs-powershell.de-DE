---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007362"
---
# <span data-ttu-id="7a755-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="7a755-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="7a755-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a755-102">SYNOPSIS</span></span>
<span data-ttu-id="7a755-103">Ruft den angegebenen Plan ab, der von einem Abonnement, das das Angebot beansprucht, erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="7a755-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="7a755-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a755-104">SYNTAX</span></span>

### <span data-ttu-id="7a755-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a755-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a755-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7a755-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a755-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7a755-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a755-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a755-108">DESCRIPTION</span></span>
<span data-ttu-id="7a755-109">Ruft den angegebenen Plan ab, der von einem Abonnement, das das Angebot beansprucht, erworben wurde.</span><span class="sxs-lookup"><span data-stu-id="7a755-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="7a755-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a755-110">EXAMPLES</span></span>

### <span data-ttu-id="7a755-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a755-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="7a755-112">Abrufen einer Sammlung aller erworbenen Pläne, auf die das Abonnement zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7a755-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="7a755-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a755-113">PARAMETERS</span></span>

### <span data-ttu-id="7a755-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a755-114">-DefaultProfile</span></span>
<span data-ttu-id="7a755-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a755-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a755-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a755-116">-InputObject</span></span>
<span data-ttu-id="7a755-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7a755-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a755-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="7a755-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="7a755-119">Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7a755-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="7a755-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7a755-120">-SubscriptionId</span></span>
<span data-ttu-id="7a755-121">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7a755-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7a755-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a755-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="7a755-123">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7a755-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="7a755-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a755-124">CommonParameters</span></span>
<span data-ttu-id="7a755-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a755-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a755-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a755-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a755-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a755-127">INPUTS</span></span>

### <span data-ttu-id="7a755-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7a755-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7a755-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a755-129">OUTPUTS</span></span>

### <span data-ttu-id="7a755-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="7a755-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="7a755-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="7a755-131">ALIASES</span></span>

<span data-ttu-id="7a755-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7a755-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7a755-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a755-133">NOTES</span></span>

<span data-ttu-id="7a755-134">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a755-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a755-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7a755-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7a755-136">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7a755-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7a755-137">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7a755-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7a755-138">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7a755-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7a755-139">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7a755-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7a755-140">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7a755-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7a755-141">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="7a755-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7a755-142">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="7a755-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7a755-143">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="7a755-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7a755-144">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="7a755-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7a755-145">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="7a755-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7a755-146">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7a755-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7a755-147">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="7a755-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7a755-148">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7a755-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7a755-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7a755-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7a755-150">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7a755-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7a755-151">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="7a755-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="7a755-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a755-152">RELATED LINKS</span></span>

