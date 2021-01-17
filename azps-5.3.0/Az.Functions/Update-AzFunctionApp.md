---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458579"
---
# <span data-ttu-id="cf18c-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="cf18c-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="cf18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf18c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf18c-103">Aktualisiert eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-103">Updates a function app.</span></span>

## <span data-ttu-id="cf18c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf18c-104">SYNTAX</span></span>

### <span data-ttu-id="cf18c-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf18c-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf18c-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="cf18c-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cf18c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf18c-107">DESCRIPTION</span></span>
<span data-ttu-id="cf18c-108">Aktualisiert eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-108">Updates a function app.</span></span>

## <span data-ttu-id="cf18c-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf18c-109">EXAMPLES</span></span>

### <span data-ttu-id="cf18c-110">Beispiel 1: Aktualisieren des Hostingplans für eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="cf18c-111">Mit diesem Befehl wird der Hostingplan der Funktions-App aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf18c-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="cf18c-112">Beispiel 2: Festlegen einer verwalteten SystemAssigned-Identität für eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="cf18c-113">Dieser Befehl legt eine verwaltete SystemAssigned-Identität für eine Funktions-App fest.</span><span class="sxs-lookup"><span data-stu-id="cf18c-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="cf18c-114">Beispiel 3: Aktualisieren von Application Insights für die Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="cf18c-115">Mit diesem Befehl werden Application Insights für die Funktions-App aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="cf18c-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="cf18c-116">Beispiel 3: Entfernen der verwalteten Identität aus einer Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="cf18c-117">Mit diesem Befehl wird eine verwaltete Identität aus einer Funktions-App entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf18c-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="cf18c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf18c-118">PARAMETERS</span></span>

### <span data-ttu-id="cf18c-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="cf18c-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="cf18c-120">Instrumentationsschlüssel der App-Einblicke, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-120">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="cf18c-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="cf18c-122">Name des vorhandenen App-Insights-Projekts, das der Funktions-App hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf18c-122">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf18c-123">-AsJob</span></span>
<span data-ttu-id="cf18c-124">Führt das Cmdlet als Hintergrundauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="cf18c-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="cf18c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf18c-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="cf18c-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="cf18c-126">-IdentityID</span></span>
<span data-ttu-id="cf18c-127">Gibt die Liste der Benutzeridentitäten an, die der Funktions-App zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cf18c-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="cf18c-128">Die Verweise auf die Benutzeridentität ARM Ressourcen-ID im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="cf18c-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cf18c-129">-IdentityType</span></span>
<span data-ttu-id="cf18c-130">Gibt den für die Funktions-App verwendeten Identitätstyp an.</span><span class="sxs-lookup"><span data-stu-id="cf18c-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="cf18c-131">Mit dem Typ "Keine" werden alle Identitäten aus der Funktions-App entfernt.</span><span class="sxs-lookup"><span data-stu-id="cf18c-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="cf18c-132">Die zulässigen Werte für diesen Parameter sind: - SystemAssigned - UserAssigned - None</span><span class="sxs-lookup"><span data-stu-id="cf18c-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf18c-133">-InputObject</span></span>
<span data-ttu-id="cf18c-134">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cf18c-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cf18c-135">-Name</span></span>
<span data-ttu-id="cf18c-136">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-136">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf18c-137">-NoWait</span></span>
<span data-ttu-id="cf18c-138">Startet den Vorgang und kehrt unmittelbar vor Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="cf18c-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="cf18c-139">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cf18c-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="cf18c-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="cf18c-140">-PlanName</span></span>
<span data-ttu-id="cf18c-141">Der Name des Serviceplans.</span><span class="sxs-lookup"><span data-stu-id="cf18c-141">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf18c-142">-ResourceGroupName</span></span>
<span data-ttu-id="cf18c-143">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf18c-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf18c-144">-SubscriptionId</span></span>
<span data-ttu-id="cf18c-145">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="cf18c-145">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf18c-146">-Tag</span></span>
<span data-ttu-id="cf18c-147">Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="cf18c-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf18c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf18c-148">-Confirm</span></span>
<span data-ttu-id="cf18c-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf18c-150">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cf18c-150">-WhatIf</span></span>
<span data-ttu-id="cf18c-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf18c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf18c-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf18c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf18c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf18c-153">CommonParameters</span></span>
<span data-ttu-id="cf18c-154">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf18c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf18c-155">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf18c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf18c-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf18c-156">INPUTS</span></span>

### <span data-ttu-id="cf18c-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="cf18c-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="cf18c-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf18c-158">OUTPUTS</span></span>

### <span data-ttu-id="cf18c-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="cf18c-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="cf18c-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf18c-160">NOTES</span></span>

<span data-ttu-id="cf18c-161">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cf18c-161">ALIASES</span></span>

<span data-ttu-id="cf18c-162">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cf18c-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf18c-163">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf18c-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf18c-164">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf18c-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf18c-165">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="cf18c-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="cf18c-166">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="cf18c-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="cf18c-167">`CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="cf18c-168">Die App-Ressourcen-ID hat das Format /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsslots und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} für andere Slots.</span><span class="sxs-lookup"><span data-stu-id="cf18c-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="cf18c-169">`[Kind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="cf18c-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="cf18c-170">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="cf18c-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="cf18c-171">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf18c-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cf18c-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> zur Aktivierung der Clientaffinität; zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiter <code>false</code> routen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="cf18c-173">Der Standardwert ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="cf18c-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS-gegenseitige Authentifizierung). Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="cf18c-175">Der Standardwert ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-176">`[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="cf18c-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="cf18c-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellungsüberschreibungen für geklonte Apps.</span><span class="sxs-lookup"><span data-stu-id="cf18c-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="cf18c-178">Falls angegeben, setzen diese Einstellungen die Einstellungen außer Kraft, die aus der Quell-App geklont werden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="cf18c-179">Andernfalls bleiben die Anwendungseinstellungen der Quell-App erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf18c-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="cf18c-180">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf18c-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cf18c-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> um benutzerdefinierte Hostnamen aus der #A0 zu klonen. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> um das Quellsteuerelement aus der #A0 zu klonen. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell- und Ziel-App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="cf18c-184">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs.</span><span class="sxs-lookup"><span data-stu-id="cf18c-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="cf18c-185">Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="cf18c-186">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="cf18c-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> um die #A0 zu überschreiben. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-188">`[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App, beispiel: USA, Westen oder Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="cf18c-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="cf18c-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM Ressourcen-ID des zu verwendende Datenverkehrs-Manager-Profils, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="cf18c-190">Die Ressourcen-ID des Datenverkehrs-Managers liegt im Format "/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}" vor.</span><span class="sxs-lookup"><span data-stu-id="cf18c-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="cf18c-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic-Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="cf18c-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="cf18c-192">Dies ist nur erforderlich, wenn das Profil von Traffic Manager noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="cf18c-193">`[Config <ISiteConfig>]`: Konfiguration der App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="cf18c-194">`IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt es fest, das angibt, ob der Pushendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="cf18c-195">`[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausgeführt werden muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="cf18c-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="cf18c-196">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.</span><span class="sxs-lookup"><span data-stu-id="cf18c-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="cf18c-197">`[AlwaysOn <Boolean?>]`: <code>true</code> wenn "Immer aktiviert" aktiviert ist; andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-198">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="cf18c-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="cf18c-199">`[ApiManagementConfigId <String>]`: APIM-Api-ID.</span><span class="sxs-lookup"><span data-stu-id="cf18c-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="cf18c-200">`[AppCommandLine <String>]`: Startbefehlszeile der App.</span><span class="sxs-lookup"><span data-stu-id="cf18c-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="cf18c-201">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="cf18c-202">`[Name <String>]`: Name des Koppelns</span><span class="sxs-lookup"><span data-stu-id="cf18c-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="cf18c-203">`[Value <String>]`: Paarwert.</span><span class="sxs-lookup"><span data-stu-id="cf18c-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="cf18c-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn die automatische Umergnung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-205">`[AutoSwapSlotName <String>]`: Name des automatischen Tauschs von Slot.</span><span class="sxs-lookup"><span data-stu-id="cf18c-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="cf18c-206">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="cf18c-207">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf18c-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="cf18c-208">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="cf18c-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="cf18c-209">`[Type <ConnectionStringType?>]`: Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="cf18c-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="cf18c-210">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab oder legt sie fest, für die cross-origin-Aufrufe zulässig sein sollen (z. http://example.com:12345) B.:</span><span class="sxs-lookup"><span data-stu-id="cf18c-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="cf18c-211">Verwenden Sie "\*", um alle zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="cf18c-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="cf18c-212">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="cf18c-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="cf18c-213">Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="cf18c-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="cf18c-214">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf18c-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="cf18c-215">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="cf18c-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="cf18c-216">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="cf18c-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="cf18c-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-218">`[DocumentRoot <String>]`: Dokumentstamm</span><span class="sxs-lookup"><span data-stu-id="cf18c-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="cf18c-219">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von dynamischen Tags enthält, die von Denkwerten im Pushregistrierungsendpunkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="cf18c-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Regeln für die Einlaufung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="cf18c-221">`[ActionHostName <String>]`: Hostname eines Slot, an das der Datenverkehr umgeleitet wird, wenn dies entschieden ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="cf18c-222">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cf18c-222">E.g.</span></span> <span data-ttu-id="cf18c-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="cf18c-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="cf18c-224">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, welche URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="cf18c-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="cf18c-225">Informationen zum Gerüst und zu Verträgen finden Sie unter "TiPCallback-Websiteerweiterung".</span><span class="sxs-lookup"><span data-stu-id="cf18c-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="cf18c-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="cf18c-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="cf18c-227">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um "ReroutePercentage" neu zuvaluieren.</span><span class="sxs-lookup"><span data-stu-id="cf18c-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="cf18c-228">`[ChangeStep <Double?>]`: Im Szenario für die automatische Erstrecherhung ist dies der Schritt zum Hinzufügen/Entfernen, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="cf18c-229">Websitemetriken werden alle N Minuten überprüft, die im ".\nCustom"-Entscheidungsalgorithmus angegeben sind, können in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der <code>ChangeIntervalInMinutes</code> die URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.</span><span class="sxs-lookup"><span data-stu-id="cf18c-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="cf18c-230">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="cf18c-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="cf18c-231">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="cf18c-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="cf18c-232">`[Name <String>]`: Name der Routingregel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="cf18c-233">Der empfohlene Name ist, auf den Platz zu verweisen, der den Datenverkehr im Experiment erhält.</span><span class="sxs-lookup"><span data-stu-id="cf18c-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="cf18c-234">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der umgeleitet <code>ActionHostName</code> wird.</span><span class="sxs-lookup"><span data-stu-id="cf18c-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="cf18c-235">`[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts</span><span class="sxs-lookup"><span data-stu-id="cf18c-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="cf18c-236">`[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="cf18c-237">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="cf18c-238">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen Anwendung FastCGI verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cf18c-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="cf18c-239">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="cf18c-240">`[HealthCheckPath <String>]`: Pfad der Integritätsprüfung</span><span class="sxs-lookup"><span data-stu-id="cf18c-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="cf18c-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website, damit Clients die Verbindung über http2.0 herstellen können.</span><span class="sxs-lookup"><span data-stu-id="cf18c-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="cf18c-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="cf18c-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für "main".</span><span class="sxs-lookup"><span data-stu-id="cf18c-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="cf18c-244">`[Action <String>]`: Zugriff für diesen IP-Bereich zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="cf18c-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="cf18c-245">`[Description <String>]`: Beschreibung der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="cf18c-246">`[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="cf18c-247">Sie kann in Form einer reinen ipv4-Adresse (erforderliche Subnetzmask-Eigenschaft) oder einer CIDR-Notation wie "ipv4/mask" (führende Bit-Übereinstimmung) liegen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="cf18c-248">Bei CIDR darf die Eigenschaft "SubnetMask" nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="cf18c-249">`[Name <String>]`: Name der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="cf18c-250">`[Priority <Int32?>]`: Priorität der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="cf18c-251">`[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="cf18c-252">`[SubnetTrafficTag <Int32?>]`: (intern) Tag für Den Subnetzdatenverkehr</span><span class="sxs-lookup"><span data-stu-id="cf18c-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="cf18c-253">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf18c-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="cf18c-254">Dies ist die Unterstützung der IP-Filterung auf Proxys.</span><span class="sxs-lookup"><span data-stu-id="cf18c-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="cf18c-255">`[VnetSubnetResourceId <String>]`: Id der virtuellen Netzwerkressource</span><span class="sxs-lookup"><span data-stu-id="cf18c-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="cf18c-256">`[VnetTrafficTag <Int32?>]`: (intern) Vnet-Datenverkehrstag</span><span class="sxs-lookup"><span data-stu-id="cf18c-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="cf18c-257">`[JavaContainer <String>]`: Java Container.</span><span class="sxs-lookup"><span data-stu-id="cf18c-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="cf18c-258">`[JavaContainerVersion <String>]`: Java Containerversion.</span><span class="sxs-lookup"><span data-stu-id="cf18c-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="cf18c-259">`[JavaVersion <String>]`: Java Version.</span><span class="sxs-lookup"><span data-stu-id="cf18c-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="cf18c-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="cf18c-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="cf18c-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="cf18c-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="cf18c-262">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="cf18c-263">`[LinuxFxVersion <String>]`: Linux-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="cf18c-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="cf18c-264">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.</span><span class="sxs-lookup"><span data-stu-id="cf18c-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="cf18c-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> zum Aktivieren des lokalen MySQL. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-266">`[LogsDirectorySizeLimit <Int32?>]`: Beschränkung der Größe des HTTP-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="cf18c-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="cf18c-267">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf18c-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="cf18c-268">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="cf18c-269">`[MachineKeyValidation <String>]`: MachineKey-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="cf18c-270">`[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="cf18c-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="cf18c-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="cf18c-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="cf18c-272">`[ManagedServiceIdentityId <Int32?>]`: Verwaltete Dienstidentitäts-ID</span><span class="sxs-lookup"><span data-stu-id="cf18c-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="cf18c-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die mindestens erforderliche Version von TLS für SSL-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="cf18c-274">`[NetFrameworkVersion <String>]`: .NET Framework-Version.</span><span class="sxs-lookup"><span data-stu-id="cf18c-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="cf18c-275">`[NodeVersion <String>]`: Version Node.js.</span><span class="sxs-lookup"><span data-stu-id="cf18c-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="cf18c-276">`[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="cf18c-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="cf18c-277">`[PhpVersion <String>]`: Version von PHP.</span><span class="sxs-lookup"><span data-stu-id="cf18c-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="cf18c-278">`[PowerShellVersion <String>]`: Version von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf18c-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="cf18c-279">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorab angezeigten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="cf18c-280">Diese Einstellung gilt nur für die Verbrauchs- und Plänen</span><span class="sxs-lookup"><span data-stu-id="cf18c-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="cf18c-281">`[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="cf18c-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="cf18c-282">`[PushKind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="cf18c-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="cf18c-283">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="cf18c-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="cf18c-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn remote debuggen aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-285">`[RemoteDebuggingVersion <String>]`: Remotedebugversion.</span><span class="sxs-lookup"><span data-stu-id="cf18c-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="cf18c-286">`[RequestCount <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="cf18c-287">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="cf18c-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="cf18c-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-289">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="cf18c-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="cf18c-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.</span><span class="sxs-lookup"><span data-stu-id="cf18c-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="cf18c-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für SCM zur Verwendung des Haupts.</span><span class="sxs-lookup"><span data-stu-id="cf18c-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="cf18c-292">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="cf18c-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="cf18c-293">`[SlowRequestCount <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="cf18c-294">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="cf18c-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="cf18c-295">`[SlowRequestTimeTaken <String>]`: Genommene Zeit.</span><span class="sxs-lookup"><span data-stu-id="cf18c-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="cf18c-296">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die für die Verwendung durch den Pushregistrierungsendpunkt auf der Whiteliste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cf18c-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="cf18c-297">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von Tags enthält, für die die Benutzerauthentifizierung am Pushregistrierungsendpunkt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cf18c-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="cf18c-298">Tags können aus alphanumerischen Zeichen bestehen und folgende Zeichen enthalten: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="cf18c-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="cf18c-299">Die Überprüfung sollte im PushRequestHandler durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="cf18c-300">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="cf18c-301">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel basierend auf privaten Bytes.</span><span class="sxs-lookup"><span data-stu-id="cf18c-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="cf18c-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="cf18c-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="cf18c-303">`[Count <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="cf18c-304">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="cf18c-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="cf18c-305">`[SubStatus <Int32?>]`: Unterstatus anfordern.</span><span class="sxs-lookup"><span data-stu-id="cf18c-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="cf18c-306">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="cf18c-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="cf18c-307">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="cf18c-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="cf18c-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> um den 32-Bit-Workerprozess zu verwenden. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="cf18c-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="cf18c-310">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="cf18c-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="cf18c-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="cf18c-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="cf18c-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="cf18c-313">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="cf18c-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="cf18c-314">`[VirtualPath <String>]`: Pfad zu virtueller Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="cf18c-315">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="cf18c-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="cf18c-316">`[VnetName <String>]`: Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="cf18c-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="cf18c-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="cf18c-318">`[WindowsFxVersion <String>]`: Xenon-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="cf18c-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="cf18c-319">`[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste</span><span class="sxs-lookup"><span data-stu-id="cf18c-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="cf18c-320">`[ContainerSize <Int32?>]`: Größe des Funktionscontainers.</span><span class="sxs-lookup"><span data-stu-id="cf18c-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="cf18c-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicherzeitkontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="cf18c-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="cf18c-322">`[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="cf18c-323">Wenn Sie diesen Wert auf "false" festlegen, wird die App deaktiviert (die App wird offline geschaltet).</span><span class="sxs-lookup"><span data-stu-id="cf18c-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="cf18c-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="cf18c-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="cf18c-325">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="cf18c-326">`[Name <String>]`: Hostname.</span><span class="sxs-lookup"><span data-stu-id="cf18c-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="cf18c-327">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="cf18c-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="cf18c-328">`[Thumbprint <String>]`: FINGERABDRUCK DES SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="cf18c-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="cf18c-329">`[ToUpdate <Boolean?>]`: Wird so <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="cf18c-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="cf18c-330">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="cf18c-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="cf18c-332">Wenn <code>true</code> die App nur über den API-Verwaltungsprozess zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="cf18c-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="cf18c-333">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="cf18c-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="cf18c-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: Konfiguriert eine Website so, dass nur https-Anfragen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="cf18c-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="cf18c-335">Problemumleitung für http-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf18c-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="cf18c-336">`[HyperV <Boolean?>]`: Hyper-V Sandbox.</span><span class="sxs-lookup"><span data-stu-id="cf18c-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="cf18c-337">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="cf18c-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="cf18c-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cf18c-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="cf18c-339">Die Verweise auf benutzeridentitätswörterbücher sind ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="cf18c-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="cf18c-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="cf18c-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cf18c-341">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.</span><span class="sxs-lookup"><span data-stu-id="cf18c-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="cf18c-342">`[RedundancyMode <RedundancyMode?>]`: Modus "Websiteredundanz"</span><span class="sxs-lookup"><span data-stu-id="cf18c-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="cf18c-343">`[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> zum Beenden der #A0 (KUDU), wenn die App beendet wird. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="cf18c-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="cf18c-345">Die Standardeinstellung ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf18c-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="cf18c-346">`[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App-Serviceplans, formatiert mit: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="cf18c-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="cf18c-347">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf18c-347">RELATED LINKS</span></span>

