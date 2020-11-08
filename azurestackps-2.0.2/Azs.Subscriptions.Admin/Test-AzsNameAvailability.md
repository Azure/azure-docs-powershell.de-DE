---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007350"
---
# <span data-ttu-id="2dbcc-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2dbcc-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="2dbcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dbcc-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbcc-103">Rufen Sie die Liste der Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="2dbcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dbcc-104">SYNTAX</span></span>

### <span data-ttu-id="2dbcc-105">CheckExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2dbcc-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dbcc-106">Kontroll</span><span class="sxs-lookup"><span data-stu-id="2dbcc-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dbcc-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2dbcc-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dbcc-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2dbcc-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2dbcc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dbcc-109">DESCRIPTION</span></span>
<span data-ttu-id="2dbcc-110">Rufen Sie die Liste der Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="2dbcc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dbcc-111">EXAMPLES</span></span>

### <span data-ttu-id="2dbcc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2dbcc-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="2dbcc-113">Gibt die Verfügbarkeit des angegebenen Abonnement Ressourcentyps und-Namens zurück.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="2dbcc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dbcc-114">PARAMETERS</span></span>

### <span data-ttu-id="2dbcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbcc-115">-DefaultProfile</span></span>
<span data-ttu-id="2dbcc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dbcc-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2dbcc-117">-InputObject</span></span>
<span data-ttu-id="2dbcc-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2dbcc-119">-Name</span></span>
<span data-ttu-id="2dbcc-120">Der zu überprüfende Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="2dbcc-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="2dbcc-122">Die Definition der Verfügbarkeits Aktion für Namen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-122">The check name availability action definition.</span></span>
<span data-ttu-id="2dbcc-123">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für NAMEAVAILABILITYDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-124">-</span><span class="sxs-lookup"><span data-stu-id="2dbcc-124">-ResourceType</span></span>
<span data-ttu-id="2dbcc-125">Der zu überprüfende Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2dbcc-126">-SubscriptionId</span></span>
<span data-ttu-id="2dbcc-127">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2dbcc-128">-Confirm</span></span>
<span data-ttu-id="2dbcc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dbcc-130">-WhatIf</span></span>
<span data-ttu-id="2dbcc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dbcc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dbcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbcc-133">CommonParameters</span></span>
<span data-ttu-id="2dbcc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbcc-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dbcc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbcc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dbcc-136">INPUTS</span></span>

### <span data-ttu-id="2dbcc-137">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="2dbcc-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="2dbcc-138">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2dbcc-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="2dbcc-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dbcc-139">OUTPUTS</span></span>

### <span data-ttu-id="2dbcc-140">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2dbcc-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="2dbcc-141">Aliase</span><span class="sxs-lookup"><span data-stu-id="2dbcc-141">ALIASES</span></span>

## <span data-ttu-id="2dbcc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dbcc-142">NOTES</span></span>

<span data-ttu-id="2dbcc-143">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2dbcc-144">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2dbcc-145">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2dbcc-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2dbcc-146">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="2dbcc-147">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="2dbcc-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2dbcc-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2dbcc-149">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="2dbcc-150">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="2dbcc-151">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="2dbcc-152">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="2dbcc-153">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="2dbcc-154">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="2dbcc-155">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2dbcc-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="2dbcc-156">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="2dbcc-157">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="2dbcc-158">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2dbcc-159">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="2dbcc-160">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="2dbcc-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : die Definition der Verfügbarkeits Aktion für Namen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="2dbcc-162">`[Name <String>]`: Der zu überprüfende Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="2dbcc-163">`[ResourceType <String>]`: Der zu überprüfende Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="2dbcc-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="2dbcc-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dbcc-164">RELATED LINKS</span></span>

