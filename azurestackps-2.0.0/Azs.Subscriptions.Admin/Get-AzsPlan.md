---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005292"
---
# <span data-ttu-id="7ba0c-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="7ba0c-101">Get-AzsPlan</span></span>

## <span data-ttu-id="7ba0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba0c-103">Abrufen des angegebenen Plans</span><span class="sxs-lookup"><span data-stu-id="7ba0c-103">Get the specified plan.</span></span>

## <span data-ttu-id="7ba0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba0c-104">SYNTAX</span></span>

### <span data-ttu-id="7ba0c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ba0c-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ba0c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7ba0c-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ba0c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba0c-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7ba0c-108">List1</span><span class="sxs-lookup"><span data-stu-id="7ba0c-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ba0c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ba0c-109">DESCRIPTION</span></span>
<span data-ttu-id="7ba0c-110">Abrufen des angegebenen Plans</span><span class="sxs-lookup"><span data-stu-id="7ba0c-110">Get the specified plan.</span></span>

## <span data-ttu-id="7ba0c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ba0c-111">EXAMPLES</span></span>

### <span data-ttu-id="7ba0c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ba0c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="7ba0c-113">Rufen Sie einen spezifische-Plan unter diesen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="7ba0c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ba0c-114">PARAMETERS</span></span>

### <span data-ttu-id="7ba0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba0c-115">-DefaultProfile</span></span>
<span data-ttu-id="7ba0c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba0c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ba0c-117">-InputObject</span></span>
<span data-ttu-id="7ba0c-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ba0c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7ba0c-119">-Name</span></span>
<span data-ttu-id="7ba0c-120">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-120">Name of the plan.</span></span>

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

### <span data-ttu-id="7ba0c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba0c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ba0c-122">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7ba0c-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7ba0c-123">-SubscriptionId</span></span>
<span data-ttu-id="7ba0c-124">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7ba0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba0c-125">CommonParameters</span></span>
<span data-ttu-id="7ba0c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba0c-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ba0c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba0c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ba0c-128">INPUTS</span></span>

### <span data-ttu-id="7ba0c-129">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7ba0c-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="7ba0c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ba0c-130">OUTPUTS</span></span>

### <span data-ttu-id="7ba0c-131">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="7ba0c-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="7ba0c-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="7ba0c-132">ALIASES</span></span>

## <span data-ttu-id="7ba0c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ba0c-133">NOTES</span></span>

<span data-ttu-id="7ba0c-134">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ba0c-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7ba0c-136">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7ba0c-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ba0c-137">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="7ba0c-138">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="7ba0c-139">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7ba0c-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ba0c-140">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="7ba0c-141">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="7ba0c-142">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="7ba0c-143">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="7ba0c-144">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="7ba0c-145">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="7ba0c-146">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7ba0c-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="7ba0c-147">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7ba0c-148">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="7ba0c-149">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7ba0c-150">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="7ba0c-151">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="7ba0c-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="7ba0c-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ba0c-152">RELATED LINKS</span></span>

