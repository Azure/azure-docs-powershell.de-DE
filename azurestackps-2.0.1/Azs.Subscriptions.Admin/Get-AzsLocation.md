---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005581"
---
# <span data-ttu-id="b6820-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="b6820-101">Get-AzsLocation</span></span>

## <span data-ttu-id="b6820-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6820-102">SYNOPSIS</span></span>
<span data-ttu-id="b6820-103">Abrufen des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="b6820-103">Get the specified location.</span></span>

## <span data-ttu-id="b6820-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6820-104">SYNTAX</span></span>

### <span data-ttu-id="b6820-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6820-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6820-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b6820-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6820-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6820-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b6820-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6820-108">DESCRIPTION</span></span>
<span data-ttu-id="b6820-109">Abrufen des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="b6820-109">Get the specified location.</span></span>

## <span data-ttu-id="b6820-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6820-110">EXAMPLES</span></span>

### <span data-ttu-id="b6820-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6820-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="b6820-112">Abrufen einer Liste aller AzureStack-Speicherorte</span><span class="sxs-lookup"><span data-stu-id="b6820-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="b6820-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6820-113">PARAMETERS</span></span>

### <span data-ttu-id="b6820-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6820-114">-DefaultProfile</span></span>
<span data-ttu-id="b6820-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6820-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6820-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b6820-116">-InputObject</span></span>
<span data-ttu-id="b6820-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b6820-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b6820-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b6820-118">-Name</span></span>
<span data-ttu-id="b6820-119">Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="b6820-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b6820-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b6820-120">-SubscriptionId</span></span>
<span data-ttu-id="b6820-121">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b6820-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6820-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6820-122">CommonParameters</span></span>
<span data-ttu-id="b6820-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6820-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6820-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6820-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6820-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6820-125">INPUTS</span></span>

### <span data-ttu-id="b6820-126">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b6820-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b6820-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6820-127">OUTPUTS</span></span>

### <span data-ttu-id="b6820-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="b6820-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="b6820-129">Aliase</span><span class="sxs-lookup"><span data-stu-id="b6820-129">ALIASES</span></span>

## <span data-ttu-id="b6820-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6820-130">NOTES</span></span>

<span data-ttu-id="b6820-131">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6820-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6820-132">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b6820-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b6820-133">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="b6820-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6820-134">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="b6820-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b6820-135">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b6820-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b6820-136">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b6820-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6820-137">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="b6820-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b6820-138">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="b6820-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b6820-139">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="b6820-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b6820-140">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="b6820-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b6820-141">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="b6820-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b6820-142">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="b6820-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b6820-143">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b6820-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b6820-144">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="b6820-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b6820-145">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="b6820-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b6820-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="b6820-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b6820-147">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b6820-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b6820-148">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="b6820-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b6820-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6820-149">RELATED LINKS</span></span>

