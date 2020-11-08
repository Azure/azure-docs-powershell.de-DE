---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005347"
---
# <span data-ttu-id="4a273-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="4a273-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="4a273-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a273-102">SYNOPSIS</span></span>
<span data-ttu-id="4a273-103">Abrufen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="4a273-103">Get the specified offer.</span></span>

## <span data-ttu-id="4a273-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a273-104">SYNTAX</span></span>

### <span data-ttu-id="4a273-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a273-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a273-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4a273-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a273-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a273-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a273-108">List1</span><span class="sxs-lookup"><span data-stu-id="4a273-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a273-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a273-109">DESCRIPTION</span></span>
<span data-ttu-id="4a273-110">Abrufen des angegebenen Angebots</span><span class="sxs-lookup"><span data-stu-id="4a273-110">Get the specified offer.</span></span>

## <span data-ttu-id="4a273-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a273-111">EXAMPLES</span></span>

### <span data-ttu-id="4a273-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a273-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="4a273-113">Angebot nach Name und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a273-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="4a273-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a273-114">PARAMETERS</span></span>

### <span data-ttu-id="4a273-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a273-115">-DefaultProfile</span></span>
<span data-ttu-id="4a273-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a273-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a273-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4a273-117">-InputObject</span></span>
<span data-ttu-id="4a273-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4a273-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a273-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4a273-119">-Name</span></span>
<span data-ttu-id="4a273-120">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="4a273-120">Name of an offer.</span></span>

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

### <span data-ttu-id="4a273-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a273-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a273-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4a273-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a273-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4a273-123">-SubscriptionId</span></span>
<span data-ttu-id="4a273-124">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4a273-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4a273-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a273-125">CommonParameters</span></span>
<span data-ttu-id="4a273-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a273-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a273-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a273-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a273-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a273-128">INPUTS</span></span>

### <span data-ttu-id="4a273-129">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4a273-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="4a273-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a273-130">OUTPUTS</span></span>

### <span data-ttu-id="4a273-131">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="4a273-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="4a273-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="4a273-132">ALIASES</span></span>

<span data-ttu-id="4a273-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="4a273-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="4a273-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a273-134">NOTES</span></span>

<span data-ttu-id="4a273-135">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4a273-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a273-136">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4a273-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4a273-137">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4a273-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a273-138">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4a273-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="4a273-139">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="4a273-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="4a273-140">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4a273-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a273-141">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="4a273-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="4a273-142">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="4a273-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="4a273-143">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="4a273-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="4a273-144">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="4a273-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="4a273-145">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="4a273-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="4a273-146">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="4a273-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="4a273-147">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="4a273-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="4a273-148">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="4a273-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4a273-149">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4a273-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="4a273-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4a273-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4a273-151">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4a273-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="4a273-152">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="4a273-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="4a273-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a273-153">RELATED LINKS</span></span>

