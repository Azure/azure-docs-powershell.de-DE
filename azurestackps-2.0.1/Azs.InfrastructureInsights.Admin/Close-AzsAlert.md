---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005505"
---
# <span data-ttu-id="69e30-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="69e30-101">Close-AzsAlert</span></span>

## <span data-ttu-id="69e30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69e30-102">SYNOPSIS</span></span>
<span data-ttu-id="69e30-103">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-103">Closes the given alert.</span></span>

## <span data-ttu-id="69e30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69e30-104">SYNTAX</span></span>

### <span data-ttu-id="69e30-105">CloseExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="69e30-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69e30-106">Schließen</span><span class="sxs-lookup"><span data-stu-id="69e30-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="69e30-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="69e30-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="69e30-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69e30-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69e30-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69e30-109">DESCRIPTION</span></span>
<span data-ttu-id="69e30-110">Schließt die angegebene Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-110">Closes the given alert.</span></span>

## <span data-ttu-id="69e30-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69e30-111">EXAMPLES</span></span>

### <span data-ttu-id="69e30-112">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="69e30-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="69e30-113">Schließen Sie eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="69e30-113">Close an alert by Name.</span></span>

### <span data-ttu-id="69e30-114">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="69e30-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="69e30-115">Schließen Sie eine Benachrichtigung über Piping.</span><span class="sxs-lookup"><span data-stu-id="69e30-115">Close an alert through piping.</span></span>

## <span data-ttu-id="69e30-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="69e30-116">PARAMETERS</span></span>

### <span data-ttu-id="69e30-117">-Alert</span><span class="sxs-lookup"><span data-stu-id="69e30-117">-Alert</span></span>
<span data-ttu-id="69e30-118">Dieses Objekt stellt eine Warnungs Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="69e30-118">This object represents an alert resource.</span></span>
<span data-ttu-id="69e30-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Warnungseigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="69e30-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-120">-Warnungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="69e30-120">-AlertId</span></span>
<span data-ttu-id="69e30-121">Ruft die ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-122">-Alertproperty</span><span class="sxs-lookup"><span data-stu-id="69e30-122">-AlertProperty</span></span>
<span data-ttu-id="69e30-123">Eigenschaften der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="69e30-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="69e30-125">Benutzer-Alias, der die Benachrichtigung geschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="69e30-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="69e30-126">-ClosedTimestamp</span></span>
<span data-ttu-id="69e30-127">Timestamp, wenn die Benachrichtigung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="69e30-128">-CreatedTimestamp</span></span>
<span data-ttu-id="69e30-129">Timestamp, wenn die Benachrichtigung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e30-130">-DefaultProfile</span></span>
<span data-ttu-id="69e30-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69e30-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e30-132">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69e30-132">-Description</span></span>
<span data-ttu-id="69e30-133">Beschreibung der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-134">-Fehler-Nr</span><span class="sxs-lookup"><span data-stu-id="69e30-134">-FaultId</span></span>
<span data-ttu-id="69e30-135">Ruft die Fehler-ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="69e30-136">-FaultTypeId</span></span>
<span data-ttu-id="69e30-137">Ruft die Fault Type-ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="69e30-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="69e30-139">Gibt an, ob die Benachrichtigung wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69e30-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="69e30-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="69e30-141">Anzeigename für das betroffene Element</span><span class="sxs-lookup"><span data-stu-id="69e30-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="69e30-142">-ImpactedResourceId</span></span>
<span data-ttu-id="69e30-143">Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-144">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69e30-144">-InputObject</span></span>
<span data-ttu-id="69e30-145">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="69e30-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="69e30-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="69e30-147">Timestamp, wenn die Benachrichtigung zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="69e30-148">-Location</span></span>
<span data-ttu-id="69e30-149">Name der Region</span><span class="sxs-lookup"><span data-stu-id="69e30-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="69e30-150">-Location1</span></span>
<span data-ttu-id="69e30-151">Der Azure-Bereich, in dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="69e30-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-152">-Name</span><span class="sxs-lookup"><span data-stu-id="69e30-152">-Name</span></span>
<span data-ttu-id="69e30-153">Der Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-154">-Behebung</span><span class="sxs-lookup"><span data-stu-id="69e30-154">-Remediation</span></span>
<span data-ttu-id="69e30-155">Ruft die Administrator freundlichen Behebungsanweisungen für die Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e30-156">-ResourceGroupName</span></span>
<span data-ttu-id="69e30-157">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69e30-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="69e30-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="69e30-159">Ruft die Registrierungs-ID des Diensts ab, zu dem die Benachrichtigung gehört, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="69e30-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="69e30-161">Ruft die Registrierungs-ID der Ressource ab, die der Benachrichtigung zugeordnet ist, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="69e30-162">Wenn die Benachrichtigung keiner Ressource zugeordnet ist, ist die Ressourcen Registrierungs-ID NULL.</span><span class="sxs-lookup"><span data-stu-id="69e30-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-163">-Schweregrad</span><span class="sxs-lookup"><span data-stu-id="69e30-163">-Severity</span></span>
<span data-ttu-id="69e30-164">Schweregrad der Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="69e30-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-165">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="69e30-165">-State</span></span>
<span data-ttu-id="69e30-166">Status der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-167">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="69e30-167">-SubscriptionId</span></span>
<span data-ttu-id="69e30-168">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69e30-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="69e30-169">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="69e30-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="69e30-170">-Tag</span></span>
<span data-ttu-id="69e30-171">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="69e30-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-172">-Title</span><span class="sxs-lookup"><span data-stu-id="69e30-172">-Title</span></span>
<span data-ttu-id="69e30-173">Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-174">-User</span><span class="sxs-lookup"><span data-stu-id="69e30-174">-User</span></span>
<span data-ttu-id="69e30-175">Der zum Ausführen des Vorgangs verwendete Benutzername.</span><span class="sxs-lookup"><span data-stu-id="69e30-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69e30-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69e30-176">-Confirm</span></span>
<span data-ttu-id="69e30-177">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69e30-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69e30-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e30-178">-WhatIf</span></span>
<span data-ttu-id="69e30-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69e30-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e30-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69e30-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69e30-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e30-181">CommonParameters</span></span>
<span data-ttu-id="69e30-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e30-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e30-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69e30-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e30-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69e30-184">INPUTS</span></span>

### <span data-ttu-id="69e30-185">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="69e30-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="69e30-186">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="69e30-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="69e30-187">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69e30-187">OUTPUTS</span></span>

### <span data-ttu-id="69e30-188">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="69e30-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="69e30-189">Notizen</span><span class="sxs-lookup"><span data-stu-id="69e30-189">NOTES</span></span>

<span data-ttu-id="69e30-190">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69e30-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69e30-191">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="69e30-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="69e30-192">Warnung <IAlert> : dieses Objekt stellt eine Warnungs Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="69e30-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="69e30-193">`[Location <String>]`: Der Azure-Bereich, in dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="69e30-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="69e30-194">`[Tag <ITrackedResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="69e30-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="69e30-195">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69e30-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="69e30-196">`[AlertId <String>]`: Ruft die ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="69e30-197">`[AlertProperty <IAlertModelAlertProperties>]`: Eigenschaften der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="69e30-198">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69e30-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="69e30-199">`[ClosedByUserAlias <String>]`: Benutzer-Alias, der die Benachrichtigung geschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="69e30-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="69e30-200">`[ClosedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="69e30-201">`[CreatedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="69e30-202">`[Description <IDictionary[]>]`: Beschreibung der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="69e30-203">`[FaultId <String>]`: Ruft die Fehler-ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="69e30-204">`[FaultTypeId <String>]`: Ruft die Fault Type-ID der Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="69e30-205">`[HasValidRemediationAction <Boolean?>]`: Gibt an, ob die Benachrichtigung wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69e30-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="69e30-206">`[ImpactedResourceDisplayName <String>]`: Anzeigename für das betroffene Element</span><span class="sxs-lookup"><span data-stu-id="69e30-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="69e30-207">`[ImpactedResourceId <String>]`: Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="69e30-208">`[LastUpdatedTimestamp <String>]`: Timestamp, wenn die Benachrichtigung zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="69e30-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="69e30-209">`[Remediation <IDictionary[]>]`: Ruft die Administrator freundlichen Behebungsanweisungen für die Benachrichtigung ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="69e30-210">`[ResourceProviderRegistrationId <String>]`: Ruft die Registrierungs-ID des Diensts ab, zu dem die Benachrichtigung gehört, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="69e30-211">`[ResourceRegistrationId <String>]`: Ruft die Registrierungs-ID der Ressource ab, die der Benachrichtigung zugeordnet ist, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="69e30-212">Wenn die Benachrichtigung keiner Ressource zugeordnet ist, ist die Ressourcen Registrierungs-ID NULL.</span><span class="sxs-lookup"><span data-stu-id="69e30-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="69e30-213">`[Severity <String>]`: Schweregrad der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="69e30-214">`[State <String>]`: Zustand der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="69e30-215">`[Title <String>]`: Ruft die Ressourcen-ID für das betroffene Element ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="69e30-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="69e30-216">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="69e30-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69e30-217">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="69e30-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="69e30-218">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="69e30-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69e30-219">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="69e30-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="69e30-220">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69e30-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="69e30-221">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="69e30-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="69e30-222">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="69e30-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="69e30-223">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="69e30-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="69e30-224">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69e30-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="69e30-225">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="69e30-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="69e30-226">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69e30-226">RELATED LINKS</span></span>

