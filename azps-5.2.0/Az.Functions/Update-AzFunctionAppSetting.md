---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297089"
---
# <span data-ttu-id="e085e-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="e085e-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="e085e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e085e-102">SYNOPSIS</span></span>
<span data-ttu-id="e085e-103">Fügt in einer Funktions-App App App-Einstellungen hinzu oder aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="e085e-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="e085e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e085e-104">SYNTAX</span></span>

### <span data-ttu-id="e085e-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e085e-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e085e-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="e085e-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e085e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e085e-107">DESCRIPTION</span></span>
<span data-ttu-id="e085e-108">Fügt in einer Funktions-App Einstellungen hinzu oder aktualisiert diese.</span><span class="sxs-lookup"><span data-stu-id="e085e-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="e085e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e085e-109">EXAMPLES</span></span>

### <span data-ttu-id="e085e-110">Beispiel 1: Hinzufügen einer neuen App-Einstellung in einer Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="e085e-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="e085e-111">Mit diesem Befehl wird eine neue App-Einstellung in einer Funktions-App hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="e085e-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="e085e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e085e-112">PARAMETERS</span></span>

### <span data-ttu-id="e085e-113">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="e085e-113">-AppSetting</span></span>
<span data-ttu-id="e085e-114">Hashtable mit Schlüsseln und Werten beschreiben die App-Einstellungen, die in der #A0 hinzugefügt oder aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e085e-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="e085e-115">Beispiel: @{"myappsetting"="123"}</span><span class="sxs-lookup"><span data-stu-id="e085e-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e085e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e085e-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="e085e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e085e-117">-Force</span></span>
<span data-ttu-id="e085e-118">Erzwingt das Cmdlet, die Einstellung der Funktions-App ohne Bestätigungsaufforderung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e085e-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e085e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e085e-119">-InputObject</span></span>
<span data-ttu-id="e085e-120">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e085e-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e085e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e085e-121">-Name</span></span>
<span data-ttu-id="e085e-122">Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="e085e-122">Name of the function app.</span></span>

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

### <span data-ttu-id="e085e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e085e-123">-ResourceGroupName</span></span>
<span data-ttu-id="e085e-124">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="e085e-124">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="e085e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e085e-125">-SubscriptionId</span></span>
<span data-ttu-id="e085e-126">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="e085e-126">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e085e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e085e-127">-Confirm</span></span>
<span data-ttu-id="e085e-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e085e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e085e-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e085e-129">-WhatIf</span></span>
<span data-ttu-id="e085e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e085e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e085e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e085e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e085e-132">CommonParameters</span></span>
<span data-ttu-id="e085e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e085e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e085e-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e085e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e085e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e085e-135">INPUTS</span></span>

### <span data-ttu-id="e085e-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="e085e-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="e085e-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e085e-137">OUTPUTS</span></span>

### <span data-ttu-id="e085e-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="e085e-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="e085e-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e085e-139">NOTES</span></span>

<span data-ttu-id="e085e-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e085e-140">ALIASES</span></span>

<span data-ttu-id="e085e-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e085e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e085e-142">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e085e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e085e-143">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e085e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e085e-144">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="e085e-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="e085e-145">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e085e-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="e085e-146">`CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App.</span><span class="sxs-lookup"><span data-stu-id="e085e-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="e085e-147">Die App-Ressourcen-ID hat das Format /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsslots und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} für andere Slots.</span><span class="sxs-lookup"><span data-stu-id="e085e-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="e085e-148">`[Kind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e085e-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="e085e-149">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="e085e-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e085e-150">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e085e-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e085e-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientaffinität, zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiter <code>false</code> routen.</span><span class="sxs-lookup"><span data-stu-id="e085e-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="e085e-152">Der Standardwert ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="e085e-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS-gegenseitige Authentifizierung). Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="e085e-154">Der Standardwert ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-155">`[ClientCertExclusionPath <String>]`: Clientzertifikatauthentifizierung, durch Kommas getrennte Ausschlusspfade</span><span class="sxs-lookup"><span data-stu-id="e085e-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="e085e-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellungsüberschreibungen für geklonte Apps.</span><span class="sxs-lookup"><span data-stu-id="e085e-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="e085e-157">Falls angegeben, setzen diese Einstellungen die Einstellungen außer Kraft, die aus der Quell-App geklont werden.</span><span class="sxs-lookup"><span data-stu-id="e085e-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="e085e-158">Andernfalls bleiben die Anwendungseinstellungen der Quell-App erhalten.</span><span class="sxs-lookup"><span data-stu-id="e085e-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="e085e-159">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e085e-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e085e-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> um benutzerdefinierte Hostnamen aus der #A0 zu klonen. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> um das Quellsteuerelement aus der #A0 zu klonen. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell- und Ziel-App.</span><span class="sxs-lookup"><span data-stu-id="e085e-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="e085e-163">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs.</span><span class="sxs-lookup"><span data-stu-id="e085e-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="e085e-164">Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e085e-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="e085e-165">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="e085e-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="e085e-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> um die #A0 zu überschreiben. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-167">`[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App, beispiel: USA, Westen oder Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="e085e-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="e085e-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM Ressourcen-ID des zu verwendende Datenverkehrs-Manager-Profils, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e085e-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="e085e-169">Die Ressourcen-ID des Datenverkehrs-Managers liegt im Format "/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}" vor.</span><span class="sxs-lookup"><span data-stu-id="e085e-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="e085e-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic-Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="e085e-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="e085e-171">Dies ist nur erforderlich, wenn das Profil von Traffic Manager noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="e085e-172">`[Config <ISiteConfig>]`: Konfiguration der App.</span><span class="sxs-lookup"><span data-stu-id="e085e-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="e085e-173">`IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt es fest, das angibt, ob der Pushendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="e085e-174">`[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausgeführt werden muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="e085e-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="e085e-175">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.</span><span class="sxs-lookup"><span data-stu-id="e085e-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="e085e-176">`[AlwaysOn <Boolean?>]`: <code>true</code> wenn "Immer aktiviert" aktiviert ist; andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-177">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="e085e-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="e085e-178">`[ApiManagementConfigId <String>]`: APIM-Api-ID.</span><span class="sxs-lookup"><span data-stu-id="e085e-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="e085e-179">`[AppCommandLine <String>]`: Startbefehlszeile der App.</span><span class="sxs-lookup"><span data-stu-id="e085e-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="e085e-180">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="e085e-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="e085e-181">`[Name <String>]`: Name des Koppelns.</span><span class="sxs-lookup"><span data-stu-id="e085e-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="e085e-182">`[Value <String>]`: Paarwert.</span><span class="sxs-lookup"><span data-stu-id="e085e-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="e085e-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn die automatische Umergnung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-184">`[AutoSwapSlotName <String>]`: Name des automatischen Tauschs von Slot.</span><span class="sxs-lookup"><span data-stu-id="e085e-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="e085e-185">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="e085e-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="e085e-186">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e085e-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="e085e-187">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e085e-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="e085e-188">`[Type <ConnectionStringType?>]`: Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="e085e-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="e085e-189">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab oder legt sie fest, für die cross-origin-Aufrufe zulässig sein sollen (z. http://example.com:12345) B.:</span><span class="sxs-lookup"><span data-stu-id="e085e-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="e085e-190">Verwenden Sie "\*", um alle zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="e085e-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="e085e-191">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e085e-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="e085e-192">Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="e085e-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="e085e-193">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e085e-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="e085e-194">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="e085e-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="e085e-195">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="e085e-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="e085e-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-197">`[DocumentRoot <String>]`: Dokumentstamm</span><span class="sxs-lookup"><span data-stu-id="e085e-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="e085e-198">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste mit dynamischen Tags enthält, die aus Benutzeransprüchen im Pushregistrierungsendpunkt ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="e085e-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Anlaufregeln.</span><span class="sxs-lookup"><span data-stu-id="e085e-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="e085e-200">`[ActionHostName <String>]`: Hostname eines Slot, an das der Datenverkehr umgeleitet wird, wenn dies entschieden ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="e085e-201">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e085e-201">E.g.</span></span> <span data-ttu-id="e085e-202">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="e085e-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="e085e-203">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, welche URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e085e-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="e085e-204">Informationen zum Gerüst und zu Verträgen finden Sie unter "TiPCallback-Websiteerweiterung".</span><span class="sxs-lookup"><span data-stu-id="e085e-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="e085e-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="e085e-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="e085e-206">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um "ReroutePercentage" neu zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="e085e-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="e085e-207">`[ChangeStep <Double?>]`: Im Szenario für die automatische Erstrecherhung ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="e085e-208">Websitemetriken werden alle N Minuten überprüft, die im ".\nCustom"-Entscheidungsalgorithmus angegeben sind, können in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der die <code>ChangeIntervalInMinutes</code> URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.</span><span class="sxs-lookup"><span data-stu-id="e085e-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="e085e-209">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="e085e-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e085e-210">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="e085e-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="e085e-211">`[Name <String>]`: Name der Routingregel.</span><span class="sxs-lookup"><span data-stu-id="e085e-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="e085e-212">Der empfohlene Name ist, auf den Platz zu verweisen, der den Datenverkehr im Experiment erhält.</span><span class="sxs-lookup"><span data-stu-id="e085e-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="e085e-213">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der umgeleitet <code>ActionHostName</code> wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="e085e-214">`[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts</span><span class="sxs-lookup"><span data-stu-id="e085e-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="e085e-215">`[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="e085e-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="e085e-216">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e085e-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="e085e-217">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen Anwendung FastCGI verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e085e-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="e085e-218">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e085e-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="e085e-219">`[HealthCheckPath <String>]`: Pfad der Integritätsprüfung</span><span class="sxs-lookup"><span data-stu-id="e085e-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="e085e-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website, damit Clients die Verbindung über http2.0 herstellen können.</span><span class="sxs-lookup"><span data-stu-id="e085e-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="e085e-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e085e-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für "main".</span><span class="sxs-lookup"><span data-stu-id="e085e-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="e085e-223">`[Action <String>]`: Zugriff für diesen IP-Bereich zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="e085e-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="e085e-224">`[Description <String>]`: Beschreibung der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="e085e-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="e085e-225">`[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="e085e-226">Sie kann in Form einer reinen ipv4-Adresse (erforderliche Subnetzmask-Eigenschaft) oder einer CIDR-Notation wie "ipv4/mask" (führende Bit-Übereinstimmung) liegen.</span><span class="sxs-lookup"><span data-stu-id="e085e-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="e085e-227">Bei CIDR darf die Eigenschaft "SubnetMask" nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e085e-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="e085e-228">`[Name <String>]`: Name der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="e085e-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="e085e-229">`[Priority <Int32?>]`: Priorität der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="e085e-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="e085e-230">`[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="e085e-231">`[SubnetTrafficTag <Int32?>]`: (intern) Tag für Den Subnetzdatenverkehr</span><span class="sxs-lookup"><span data-stu-id="e085e-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="e085e-232">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="e085e-233">Dies ist die Unterstützung der IP-Filterung auf Proxys.</span><span class="sxs-lookup"><span data-stu-id="e085e-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="e085e-234">`[VnetSubnetResourceId <String>]`: Ressourcen-ID des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="e085e-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="e085e-235">`[VnetTrafficTag <Int32?>]`: (intern) Vnet-Datenverkehrstag</span><span class="sxs-lookup"><span data-stu-id="e085e-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="e085e-236">`[JavaContainer <String>]`: Java Container.</span><span class="sxs-lookup"><span data-stu-id="e085e-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="e085e-237">`[JavaContainerVersion <String>]`: Java Containerversion.</span><span class="sxs-lookup"><span data-stu-id="e085e-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="e085e-238">`[JavaVersion <String>]`: Java Version.</span><span class="sxs-lookup"><span data-stu-id="e085e-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="e085e-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="e085e-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="e085e-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="e085e-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="e085e-241">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.</span><span class="sxs-lookup"><span data-stu-id="e085e-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="e085e-242">`[LinuxFxVersion <String>]`: Linux-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="e085e-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="e085e-243">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.</span><span class="sxs-lookup"><span data-stu-id="e085e-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="e085e-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> zum Aktivieren des lokalen MySQL. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-245">`[LogsDirectorySizeLimit <Int32?>]`: Beschränkung der Größe des HTTP-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="e085e-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="e085e-246">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="e085e-247">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e085e-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="e085e-248">`[MachineKeyValidation <String>]`: MachineKey-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="e085e-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="e085e-249">`[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e085e-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="e085e-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="e085e-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="e085e-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity ID</span><span class="sxs-lookup"><span data-stu-id="e085e-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="e085e-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die mindestversion von TLS, die für -SSL-Anforderungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="e085e-253">`[NetFrameworkVersion <String>]`: .NET Framework-Version.</span><span class="sxs-lookup"><span data-stu-id="e085e-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="e085e-254">`[NodeVersion <String>]`: Version Node.js.</span><span class="sxs-lookup"><span data-stu-id="e085e-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="e085e-255">`[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="e085e-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="e085e-256">`[PhpVersion <String>]`: Version von PHP.</span><span class="sxs-lookup"><span data-stu-id="e085e-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="e085e-257">`[PowerShellVersion <String>]`: Version von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e085e-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="e085e-258">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorab angezeigten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="e085e-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="e085e-259">Diese Einstellung gilt nur für die Verbrauchs- und Plänen</span><span class="sxs-lookup"><span data-stu-id="e085e-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="e085e-260">`[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="e085e-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="e085e-261">`[PushKind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="e085e-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="e085e-262">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="e085e-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="e085e-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn remote debuggen aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-264">`[RemoteDebuggingVersion <String>]`: Remotedebugversion.</span><span class="sxs-lookup"><span data-stu-id="e085e-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="e085e-265">`[RequestCount <Int32?>]`: Anzahl der Anfragen.</span><span class="sxs-lookup"><span data-stu-id="e085e-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e085e-266">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="e085e-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e085e-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e085e-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-268">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e085e-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="e085e-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.</span><span class="sxs-lookup"><span data-stu-id="e085e-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="e085e-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für SCM zur Verwendung des Haupts.</span><span class="sxs-lookup"><span data-stu-id="e085e-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="e085e-271">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="e085e-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="e085e-272">`[SlowRequestCount <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="e085e-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="e085e-273">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="e085e-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="e085e-274">`[SlowRequestTimeTaken <String>]`: Genommene Zeit.</span><span class="sxs-lookup"><span data-stu-id="e085e-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="e085e-275">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die für die Verwendung durch den Pushregistrierungsendpunkt auf der Whiteliste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e085e-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="e085e-276">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von Tags enthält, für die die Benutzerauthentifizierung am Pushregistrierungsendpunkt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="e085e-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="e085e-277">Tags können aus alphanumerischen Zeichen bestehen und folgendes: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="e085e-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="e085e-278">Die Überprüfung sollte im PushRequestHandler durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e085e-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="e085e-279">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="e085e-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="e085e-280">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel basierend auf privaten Bytes.</span><span class="sxs-lookup"><span data-stu-id="e085e-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="e085e-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="e085e-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="e085e-282">`[Count <Int32?>]`: Anzahl der Anfragen.</span><span class="sxs-lookup"><span data-stu-id="e085e-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="e085e-283">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="e085e-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="e085e-284">`[SubStatus <Int32?>]`: Unterstatus anfordern.</span><span class="sxs-lookup"><span data-stu-id="e085e-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="e085e-285">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="e085e-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="e085e-286">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e085e-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="e085e-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> um den 32-Bit-Workerprozess zu verwenden. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="e085e-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e085e-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="e085e-289">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="e085e-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="e085e-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="e085e-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e085e-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="e085e-292">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="e085e-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="e085e-293">`[VirtualPath <String>]`: Pfad zu virtueller Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e085e-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="e085e-294">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="e085e-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="e085e-295">`[VnetName <String>]`: Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="e085e-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="e085e-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="e085e-297">`[WindowsFxVersion <String>]`: Xenon-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="e085e-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="e085e-298">`[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste</span><span class="sxs-lookup"><span data-stu-id="e085e-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="e085e-299">`[ContainerSize <Int32?>]`: Größe des Funktionscontainers.</span><span class="sxs-lookup"><span data-stu-id="e085e-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="e085e-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicher-Zeitkontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="e085e-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="e085e-301">`[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e085e-302">Wenn Sie diesen Wert auf "false" festlegen, wird die App deaktiviert (die App wird offline geschaltet).</span><span class="sxs-lookup"><span data-stu-id="e085e-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="e085e-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="e085e-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="e085e-304">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="e085e-305">`[Name <String>]`: Hostname.</span><span class="sxs-lookup"><span data-stu-id="e085e-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="e085e-306">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="e085e-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="e085e-307">`[Thumbprint <String>]`: FINGERABDRUCK DES SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="e085e-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="e085e-308">`[ToUpdate <Boolean?>]`: Wird so <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e085e-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="e085e-309">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="e085e-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="e085e-311">Wenn <code>true</code> die App nur über den API-Verwaltungsprozess zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="e085e-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="e085e-312">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="e085e-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="e085e-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: Konfiguriert eine Website so, dass nur https-Anfragen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="e085e-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="e085e-314">Problemumleitung für http-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e085e-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="e085e-315">`[HyperV <Boolean?>]`: Hyper-V Sandbox.</span><span class="sxs-lookup"><span data-stu-id="e085e-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e085e-316">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="e085e-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="e085e-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e085e-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="e085e-318">Die Verweise auf benutzeridentitätswörterbücher sind ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="e085e-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="e085e-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="e085e-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e085e-320">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.</span><span class="sxs-lookup"><span data-stu-id="e085e-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="e085e-321">`[RedundancyMode <RedundancyMode?>]`: Modus "Websiteredundanz"</span><span class="sxs-lookup"><span data-stu-id="e085e-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="e085e-322">`[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> zum Beenden der #A0 (KUDU), wenn die App beendet wird. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="e085e-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="e085e-324">Die Standardeinstellung ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="e085e-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="e085e-325">`[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App-Serviceplans, formatiert mit: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="e085e-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="e085e-326">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e085e-326">RELATED LINKS</span></span>

