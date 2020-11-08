---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005351"
---
# <span data-ttu-id="3f074-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="3f074-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="3f074-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f074-102">SYNOPSIS</span></span>
<span data-ttu-id="3f074-103">Verknüpft einen Plan mit einem Angebot.</span><span class="sxs-lookup"><span data-stu-id="3f074-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="3f074-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f074-104">SYNTAX</span></span>

### <span data-ttu-id="3f074-105">LinkExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f074-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f074-106">Link</span><span class="sxs-lookup"><span data-stu-id="3f074-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f074-107">LinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f074-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f074-108">LinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3f074-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3f074-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f074-109">DESCRIPTION</span></span>
<span data-ttu-id="3f074-110">Verknüpft einen Plan mit einem Angebot.</span><span class="sxs-lookup"><span data-stu-id="3f074-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="3f074-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f074-111">EXAMPLES</span></span>

### <span data-ttu-id="3f074-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f074-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

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

<span data-ttu-id="3f074-113">Verknüpft einen Plan mit einem Angebot.</span><span class="sxs-lookup"><span data-stu-id="3f074-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="3f074-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f074-114">PARAMETERS</span></span>

### <span data-ttu-id="3f074-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f074-115">-DefaultProfile</span></span>
<span data-ttu-id="3f074-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f074-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f074-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3f074-117">-InputObject</span></span>
<span data-ttu-id="3f074-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3f074-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="3f074-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="3f074-120">Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="3f074-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-121">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="3f074-121">-OfferName</span></span>
<span data-ttu-id="3f074-122">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="3f074-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="3f074-123">-PlanLink</span></span>
<span data-ttu-id="3f074-124">Definition für das Verknüpfen und Aufheben der Verknüpfung von Plänen zu angeboten.</span><span class="sxs-lookup"><span data-stu-id="3f074-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="3f074-125">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PLANLINK-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3f074-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="3f074-126">-PlanLinkType</span></span>
<span data-ttu-id="3f074-127">Der Typ des Plan Links.</span><span class="sxs-lookup"><span data-stu-id="3f074-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-128">-Planname</span><span class="sxs-lookup"><span data-stu-id="3f074-128">-PlanName</span></span>
<span data-ttu-id="3f074-129">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="3f074-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f074-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f074-131">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="3f074-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="3f074-132">-SubscriptionId</span></span>
<span data-ttu-id="3f074-133">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="3f074-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f074-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f074-134">-Confirm</span></span>
<span data-ttu-id="3f074-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f074-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f074-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f074-136">-WhatIf</span></span>
<span data-ttu-id="3f074-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f074-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f074-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f074-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f074-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f074-139">CommonParameters</span></span>
<span data-ttu-id="3f074-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f074-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f074-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f074-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f074-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f074-142">INPUTS</span></span>

### <span data-ttu-id="3f074-143">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="3f074-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="3f074-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3f074-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="3f074-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f074-145">OUTPUTS</span></span>

### <span data-ttu-id="3f074-146">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="3f074-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="3f074-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="3f074-147">ALIASES</span></span>

## <span data-ttu-id="3f074-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f074-148">NOTES</span></span>

<span data-ttu-id="3f074-149">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f074-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f074-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="3f074-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f074-151">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="3f074-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f074-152">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="3f074-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="3f074-153">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="3f074-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="3f074-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="3f074-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f074-155">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="3f074-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="3f074-156">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="3f074-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="3f074-157">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="3f074-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="3f074-158">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="3f074-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="3f074-159">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="3f074-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="3f074-160">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="3f074-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="3f074-161">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3f074-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="3f074-162">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="3f074-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3f074-163">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="3f074-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="3f074-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="3f074-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3f074-165">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3f074-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="3f074-166">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="3f074-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="3f074-167">PLANLINK <IPlanLinkDefinition> : Definition für das Verknüpfen und Aufheben der Verknüpfung von Plänen zu angeboten.</span><span class="sxs-lookup"><span data-stu-id="3f074-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="3f074-168">`[MaxAcquisitionCount <Int32?>]`: Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="3f074-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="3f074-169">`[PlanLinkType <PlanLinkType?>]`: Geben Sie den Plan-Link ein.</span><span class="sxs-lookup"><span data-stu-id="3f074-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="3f074-170">`[PlanName <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="3f074-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="3f074-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f074-171">RELATED LINKS</span></span>

