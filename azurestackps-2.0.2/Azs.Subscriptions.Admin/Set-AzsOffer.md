---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006870"
---
# <span data-ttu-id="27e50-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="27e50-101">Set-AzsOffer</span></span>

## <span data-ttu-id="27e50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27e50-102">SYNOPSIS</span></span>
<span data-ttu-id="27e50-103">Erstellen oder aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="27e50-103">Create or update the offer.</span></span>

## <span data-ttu-id="27e50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27e50-104">SYNTAX</span></span>

### <span data-ttu-id="27e50-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="27e50-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="27e50-106">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="27e50-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27e50-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27e50-107">DESCRIPTION</span></span>
<span data-ttu-id="27e50-108">Erstellen oder aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="27e50-108">Create or update the offer.</span></span>

## <span data-ttu-id="27e50-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27e50-109">EXAMPLES</span></span>

### <span data-ttu-id="27e50-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27e50-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="27e50-111">Aktualisieren eines Angebots</span><span class="sxs-lookup"><span data-stu-id="27e50-111">Update an offer.</span></span>

## <span data-ttu-id="27e50-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27e50-112">PARAMETERS</span></span>

### <span data-ttu-id="27e50-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="27e50-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="27e50-114">Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="27e50-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="27e50-115">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für ADDONPLANDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="27e50-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="27e50-116">-BasePlanIds</span></span>
<span data-ttu-id="27e50-117">Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="27e50-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e50-118">-DefaultProfile</span></span>
<span data-ttu-id="27e50-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27e50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27e50-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27e50-120">-Description</span></span>
<span data-ttu-id="27e50-121">Angebotsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="27e50-121">Description of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27e50-122">-DisplayName</span></span>
<span data-ttu-id="27e50-123">Anzeigename des Angebots.</span><span class="sxs-lookup"><span data-stu-id="27e50-123">Display name of offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="27e50-124">-ExternalReferenceId</span></span>
<span data-ttu-id="27e50-125">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="27e50-125">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="27e50-126">-Location</span></span>
<span data-ttu-id="27e50-127">Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="27e50-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="27e50-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="27e50-129">Maximale Abonnements pro Konto.</span><span class="sxs-lookup"><span data-stu-id="27e50-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-130">-Name</span><span class="sxs-lookup"><span data-stu-id="27e50-130">-Name</span></span>
<span data-ttu-id="27e50-131">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="27e50-131">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="27e50-132">-OfferDefinition</span></span>
<span data-ttu-id="27e50-133">Stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="27e50-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="27e50-134">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für OFFERDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="27e50-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-135">-Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="27e50-135">-PropertiesName</span></span>
<span data-ttu-id="27e50-136">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="27e50-136">Name of the Offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e50-137">-ResourceGroupName</span></span>
<span data-ttu-id="27e50-138">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="27e50-138">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-139">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="27e50-139">-State</span></span>
<span data-ttu-id="27e50-140">Barrierefreien Status anbieten.</span><span class="sxs-lookup"><span data-stu-id="27e50-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="27e50-141">-SubscriptionCount</span></span>
<span data-ttu-id="27e50-142">Aktuelle Abonnementanzahl.</span><span class="sxs-lookup"><span data-stu-id="27e50-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-143">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="27e50-143">-SubscriptionId</span></span>
<span data-ttu-id="27e50-144">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="27e50-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="27e50-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27e50-145">-Confirm</span></span>
<span data-ttu-id="27e50-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27e50-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27e50-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e50-147">-WhatIf</span></span>
<span data-ttu-id="27e50-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27e50-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27e50-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27e50-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27e50-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e50-150">CommonParameters</span></span>
<span data-ttu-id="27e50-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e50-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e50-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27e50-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e50-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27e50-153">INPUTS</span></span>

### <span data-ttu-id="27e50-154">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="27e50-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="27e50-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27e50-155">OUTPUTS</span></span>

### <span data-ttu-id="27e50-156">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="27e50-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="27e50-157">Aliase</span><span class="sxs-lookup"><span data-stu-id="27e50-157">ALIASES</span></span>

## <span data-ttu-id="27e50-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="27e50-158">NOTES</span></span>

<span data-ttu-id="27e50-159">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27e50-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27e50-160">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="27e50-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="27e50-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="27e50-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="27e50-162">`[MaxAcquisitionCount <Int32?>]`: Maximale Anzahl von Instanzen, die von einem einzelnen Abonnement abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="27e50-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="27e50-163">Wenn keine Angabe erfolgt, lautet der angenommene Wert 1.</span><span class="sxs-lookup"><span data-stu-id="27e50-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="27e50-164">`[PlanId <String>]`: Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="27e50-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="27e50-165">OFFERDEFINITION <IOffer> : stellt ein Angebot von Diensten dar, für die ein Abonnement erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="27e50-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="27e50-166">`[Location <String>]`: Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="27e50-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="27e50-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="27e50-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="27e50-168">`[MaxAcquisitionCount <Int32?>]`: Maximale Anzahl von Instanzen, die von einem einzelnen Abonnement abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="27e50-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="27e50-169">Wenn keine Angabe erfolgt, lautet der angenommene Wert 1.</span><span class="sxs-lookup"><span data-stu-id="27e50-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="27e50-170">`[PlanId <String>]`: Plan-ID.</span><span class="sxs-lookup"><span data-stu-id="27e50-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="27e50-171">`[BasePlanIds <String[]>]`: Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="27e50-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="27e50-172">`[Description <String>]`: Angebotsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="27e50-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="27e50-173">`[DisplayName <String>]`: Anzeige des Angebots namens.</span><span class="sxs-lookup"><span data-stu-id="27e50-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="27e50-174">`[ExternalReferenceId <String>]`: Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="27e50-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="27e50-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximale Abonnements pro Konto.</span><span class="sxs-lookup"><span data-stu-id="27e50-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="27e50-176">`[PropertiesName <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="27e50-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="27e50-177">`[State <AccessibilityState?>]`: Bieten Sie den Barrierefreiheitsstatus an.</span><span class="sxs-lookup"><span data-stu-id="27e50-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="27e50-178">`[SubscriptionCount <Int32?>]`: Aktuelle Abonnementanzahl.</span><span class="sxs-lookup"><span data-stu-id="27e50-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="27e50-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27e50-179">RELATED LINKS</span></span>

