---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007080"
---
# <span data-ttu-id="c6547-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="c6547-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="c6547-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6547-102">SYNOPSIS</span></span>
<span data-ttu-id="c6547-103">Rufen Sie einen Verzeichnis Mandanten nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="c6547-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="c6547-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6547-104">SYNTAX</span></span>

### <span data-ttu-id="c6547-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6547-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6547-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c6547-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6547-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6547-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6547-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6547-108">DESCRIPTION</span></span>
<span data-ttu-id="c6547-109">Rufen Sie einen Verzeichnis Mandanten nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="c6547-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="c6547-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6547-110">EXAMPLES</span></span>

### <span data-ttu-id="c6547-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6547-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="c6547-112">Listet alle Verzeichnis Mandanten unter dem aktuellen Abonnement und dem angegebenen Ressourcengruppennamen auf.</span><span class="sxs-lookup"><span data-stu-id="c6547-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="c6547-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6547-113">PARAMETERS</span></span>

### <span data-ttu-id="c6547-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6547-114">-DefaultProfile</span></span>
<span data-ttu-id="c6547-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6547-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6547-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6547-116">-InputObject</span></span>
<span data-ttu-id="c6547-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c6547-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6547-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c6547-118">-Name</span></span>
<span data-ttu-id="c6547-119">Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="c6547-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="c6547-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6547-120">-ResourceGroupName</span></span>
<span data-ttu-id="c6547-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c6547-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c6547-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c6547-122">-SubscriptionId</span></span>
<span data-ttu-id="c6547-123">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c6547-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c6547-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6547-124">CommonParameters</span></span>
<span data-ttu-id="c6547-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6547-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6547-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6547-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6547-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6547-127">INPUTS</span></span>

### <span data-ttu-id="c6547-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c6547-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c6547-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6547-129">OUTPUTS</span></span>

### <span data-ttu-id="c6547-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="c6547-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="c6547-131">Aliase</span><span class="sxs-lookup"><span data-stu-id="c6547-131">ALIASES</span></span>

## <span data-ttu-id="c6547-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6547-132">NOTES</span></span>

<span data-ttu-id="c6547-133">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6547-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6547-134">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c6547-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c6547-135">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c6547-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6547-136">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c6547-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c6547-137">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c6547-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c6547-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c6547-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6547-139">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c6547-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c6547-140">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="c6547-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c6547-141">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="c6547-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c6547-142">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="c6547-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c6547-143">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="c6547-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c6547-144">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="c6547-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c6547-145">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="c6547-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c6547-146">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="c6547-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c6547-147">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c6547-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c6547-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c6547-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c6547-149">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c6547-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c6547-150">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="c6547-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="c6547-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6547-151">RELATED LINKS</span></span>

