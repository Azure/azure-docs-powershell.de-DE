---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007210"
---
# <span data-ttu-id="98280-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="98280-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="98280-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98280-102">SYNOPSIS</span></span>
<span data-ttu-id="98280-103">Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="98280-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="98280-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98280-104">SYNTAX</span></span>

### <span data-ttu-id="98280-105">ValidateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="98280-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98280-106">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="98280-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="98280-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98280-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98280-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="98280-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98280-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98280-109">DESCRIPTION</span></span>
<span data-ttu-id="98280-110">Überprüfen Sie, ob Benutzer Abonnements zwischen angeboten des Delegierten Anbieters verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="98280-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="98280-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98280-111">EXAMPLES</span></span>

### <span data-ttu-id="98280-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98280-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="98280-113">Testen Sie, ob Benutzer Abonnements in ein Angebot für Delegierte Anbieter verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="98280-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="98280-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="98280-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="98280-115">Testen Sie, ob Benutzer Abonnements von einem Delegierten Anbieter an den Standardanbieter verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="98280-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="98280-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="98280-116">PARAMETERS</span></span>

### <span data-ttu-id="98280-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98280-117">-AsJob</span></span>
<span data-ttu-id="98280-118">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="98280-118">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98280-119">-DefaultProfile</span></span>
<span data-ttu-id="98280-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98280-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98280-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="98280-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="98280-122">Der Delegierte Anbieter bietet einen Bezeichner (aus dem Administratorkontext) an, in den die Abonnements verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98280-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98280-123">-InputObject</span></span>
<span data-ttu-id="98280-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="98280-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="98280-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="98280-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="98280-126">Die zu erstellbare Aktionsdefinition für "Abonnements verschieben" finden Sie unter Abschnitt "Notizen" für MOVESUBSCRIPTIONSDEFINITION-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="98280-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="98280-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="98280-127">-NoWait</span></span>
<span data-ttu-id="98280-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="98280-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98280-129">-PassThru</span></span>
<span data-ttu-id="98280-130">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="98280-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="98280-131">-ResourceId</span></span>
<span data-ttu-id="98280-132">Eine Sammlung von Abonnements, die in das Angebot des Delegierten Zielanbieters verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="98280-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="98280-133">-SubscriptionId</span></span>
<span data-ttu-id="98280-134">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="98280-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="98280-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98280-135">-Confirm</span></span>
<span data-ttu-id="98280-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98280-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98280-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98280-137">-WhatIf</span></span>
<span data-ttu-id="98280-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98280-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98280-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98280-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98280-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98280-140">CommonParameters</span></span>
<span data-ttu-id="98280-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98280-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98280-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98280-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98280-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98280-143">INPUTS</span></span>

### <span data-ttu-id="98280-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="98280-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="98280-145">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="98280-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="98280-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98280-146">OUTPUTS</span></span>

### <span data-ttu-id="98280-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98280-147">System.Boolean</span></span>

<span data-ttu-id="98280-148">Aliase</span><span class="sxs-lookup"><span data-stu-id="98280-148">ALIASES</span></span>

### <span data-ttu-id="98280-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="98280-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="98280-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="98280-150">NOTES</span></span>

<span data-ttu-id="98280-151">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98280-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98280-152">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="98280-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="98280-153">Inputobject <ISubscriptionsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="98280-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98280-154">`[DelegatedProvider <String>]`: DelegatedProvider-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="98280-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="98280-155">`[DelegatedProviderSubscriptionId <String>]`: Bezeichner des Delegierten Anbieter Abonnements.</span><span class="sxs-lookup"><span data-stu-id="98280-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="98280-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="98280-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98280-157">`[Location <String>]`: Der AzureStack-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="98280-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="98280-158">`[ManifestName <String>]`: Der Name des Manifests.</span><span class="sxs-lookup"><span data-stu-id="98280-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="98280-159">`[Offer <String>]`: Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="98280-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="98280-160">`[OfferDelegationName <String>]`: Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="98280-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="98280-161">`[OperationsStatusName <String>]`: Der Name des Vorgangsstatus.</span><span class="sxs-lookup"><span data-stu-id="98280-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="98280-162">`[Plan <String>]`: Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="98280-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="98280-163">`[PlanAcquisitionId <String>]`: Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="98280-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="98280-164">`[Quota <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="98280-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="98280-165">`[ResourceGroupName <String>]`: Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="98280-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="98280-166">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="98280-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="98280-167">`[TargetSubscriptionId <String>]`: Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="98280-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="98280-168">`[Tenant <String>]`: Name des Verzeichnis Mandanten.</span><span class="sxs-lookup"><span data-stu-id="98280-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="98280-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : die Aktionsdefinition ' Move Subscriptions '</span><span class="sxs-lookup"><span data-stu-id="98280-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="98280-170">`Resources <String[]>`: Eine Sammlung von Abonnements, die in das Angebot des Delegierten Zielanbieters verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="98280-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="98280-171">`[TargetDelegatedProviderOffer <String>]`: Der Delegierte Anbieter bietet einen Bezeichner (aus dem Administratorkontext) an, in den die Abonnements verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="98280-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="98280-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98280-172">RELATED LINKS</span></span>

