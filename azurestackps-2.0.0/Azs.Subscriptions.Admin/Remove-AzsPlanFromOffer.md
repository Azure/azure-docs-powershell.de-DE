---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005316"
---
# <span data-ttu-id="d2c59-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="d2c59-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="d2c59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2c59-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c59-103">Aufheben der Verknüpfung zwischen einem Plan und einem Angebot</span><span class="sxs-lookup"><span data-stu-id="d2c59-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d2c59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2c59-104">SYNTAX</span></span>

### <span data-ttu-id="d2c59-105">UnlinkExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2c59-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2c59-106">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d2c59-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2c59-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2c59-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2c59-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2c59-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d2c59-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2c59-109">DESCRIPTION</span></span>
<span data-ttu-id="d2c59-110">Aufheben der Verknüpfung zwischen einem Plan und einem Angebot</span><span class="sxs-lookup"><span data-stu-id="d2c59-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d2c59-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2c59-111">EXAMPLES</span></span>

### <span data-ttu-id="d2c59-112">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="d2c59-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="d2c59-113">Aufheben der Verknüpfung zwischen einem Plan und einem Angebot</span><span class="sxs-lookup"><span data-stu-id="d2c59-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="d2c59-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c59-114">PARAMETERS</span></span>

### <span data-ttu-id="d2c59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c59-115">-DefaultProfile</span></span>
<span data-ttu-id="d2c59-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2c59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c59-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d2c59-117">-InputObject</span></span>
<span data-ttu-id="d2c59-118">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d2c59-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="d2c59-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="d2c59-120">Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="d2c59-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-121">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="d2c59-121">-OfferName</span></span>
<span data-ttu-id="d2c59-122">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="d2c59-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="d2c59-123">-PlanLink</span></span>
<span data-ttu-id="d2c59-124">Definition für das Verknüpfen und Aufheben der Verknüpfung von Plänen zu angeboten.</span><span class="sxs-lookup"><span data-stu-id="d2c59-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="d2c59-125">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für PLANLINK-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d2c59-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="d2c59-126">-PlanLinkType</span></span>
<span data-ttu-id="d2c59-127">Der Typ des Plan Links.</span><span class="sxs-lookup"><span data-stu-id="d2c59-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-128">-Planname</span><span class="sxs-lookup"><span data-stu-id="d2c59-128">-PlanName</span></span>
<span data-ttu-id="d2c59-129">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="d2c59-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c59-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2c59-131">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d2c59-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d2c59-132">-SubscriptionId</span></span>
<span data-ttu-id="d2c59-133">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d2c59-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d2c59-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2c59-134">-Confirm</span></span>
<span data-ttu-id="d2c59-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2c59-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c59-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c59-136">-WhatIf</span></span>
<span data-ttu-id="d2c59-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2c59-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c59-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2c59-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c59-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c59-139">CommonParameters</span></span>
<span data-ttu-id="d2c59-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c59-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c59-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2c59-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c59-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2c59-142">INPUTS</span></span>

### <span data-ttu-id="d2c59-143">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="d2c59-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="d2c59-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d2c59-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d2c59-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2c59-145">OUTPUTS</span></span>

### <span data-ttu-id="d2c59-146">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d2c59-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="d2c59-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="d2c59-147">ALIASES</span></span>

## <span data-ttu-id="d2c59-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2c59-148">NOTES</span></span>

<span data-ttu-id="d2c59-149">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2c59-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2c59-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d2c59-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d2c59-151">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c59-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2c59-152">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d2c59-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d2c59-153">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="d2c59-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d2c59-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d2c59-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2c59-155">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="d2c59-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d2c59-156">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="d2c59-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d2c59-157">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="d2c59-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d2c59-158">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="d2c59-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d2c59-159">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="d2c59-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d2c59-160">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="d2c59-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d2c59-161">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d2c59-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d2c59-162">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="d2c59-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d2c59-163">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="d2c59-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d2c59-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d2c59-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d2c59-165">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="d2c59-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d2c59-166">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="d2c59-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="d2c59-167">PLANLINK <IPlanLinkDefinition> : Definition für das Verknüpfen und Aufheben der Verknüpfung von Plänen zu angeboten.</span><span class="sxs-lookup"><span data-stu-id="d2c59-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="d2c59-168">`[MaxAcquisitionCount <Int32?>]`: Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="d2c59-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="d2c59-169">`[PlanLinkType <PlanLinkType?>]`: Geben Sie den Plan-Link ein.</span><span class="sxs-lookup"><span data-stu-id="d2c59-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="d2c59-170">`[PlanName <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="d2c59-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="d2c59-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2c59-171">RELATED LINKS</span></span>

