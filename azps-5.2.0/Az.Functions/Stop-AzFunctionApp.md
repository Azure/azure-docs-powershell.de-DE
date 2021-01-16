---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/stop-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Stop-AzFunctionApp.md
ms.openlocfilehash: e6a5b243c4bb5c39528716194f37bd0bb722b5be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301291"
---
# <span data-ttu-id="82386-101">Stop-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="82386-101">Stop-AzFunctionApp</span></span>

## <span data-ttu-id="82386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82386-102">SYNOPSIS</span></span>
<span data-ttu-id="82386-103">Beendet eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="82386-103">Stops a function app.</span></span>

## <span data-ttu-id="82386-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82386-104">SYNTAX</span></span>

### <span data-ttu-id="82386-105">StopByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="82386-105">StopByName (Default)</span></span>
```
Stop-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="82386-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="82386-106">ByObjectInput</span></span>
```
Stop-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="82386-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82386-107">DESCRIPTION</span></span>
<span data-ttu-id="82386-108">Beendet eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="82386-108">Stops a function app.</span></span>

## <span data-ttu-id="82386-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82386-109">EXAMPLES</span></span>

### <span data-ttu-id="82386-110">Beispiel 1: Benennen Sie eine Funktions-App, und beenden Sie sie.</span><span class="sxs-lookup"><span data-stu-id="82386-110">Example 1: Get a function app by name and stop it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Stop-AzFunctionApp -Force
```

<span data-ttu-id="82386-111">Dieser Befehl ruft eine Funktions-App nach Name ab und beendet sie.</span><span class="sxs-lookup"><span data-stu-id="82386-111">This command gets a function app by name and stops it.</span></span>

### <span data-ttu-id="82386-112">Beispiel 2: Beenden einer Funktions-App nach Name.</span><span class="sxs-lookup"><span data-stu-id="82386-112">Example 2: Stop a function app by name.</span></span>
```powershell
PS C:\> Stop-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="82386-113">Mit diesem Befehl wird eine Funktions-App nach Name beendet.</span><span class="sxs-lookup"><span data-stu-id="82386-113">This command stops a function app by name.</span></span>

## <span data-ttu-id="82386-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82386-114">PARAMETERS</span></span>

### <span data-ttu-id="82386-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82386-115">-DefaultProfile</span></span>
<span data-ttu-id="82386-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82386-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82386-117">-Force</span><span class="sxs-lookup"><span data-stu-id="82386-117">-Force</span></span>
<span data-ttu-id="82386-118">Erzwingt das Cmdlet, die Funktions-App ohne Bestätigungsaufforderung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="82386-118">Forces the cmdlet to stop the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="82386-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82386-119">-InputObject</span></span>
<span data-ttu-id="82386-120">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="82386-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82386-121">-Name</span><span class="sxs-lookup"><span data-stu-id="82386-121">-Name</span></span>
<span data-ttu-id="82386-122">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="82386-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82386-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82386-123">-PassThru</span></span>
<span data-ttu-id="82386-124">Gibt "true" zurück, wenn der Befehl erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="82386-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="82386-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82386-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82386-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82386-126">-SubscriptionId</span></span>
<span data-ttu-id="82386-127">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="82386-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82386-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82386-128">-Confirm</span></span>
<span data-ttu-id="82386-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82386-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82386-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82386-130">-WhatIf</span></span>
<span data-ttu-id="82386-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82386-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82386-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82386-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82386-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82386-133">CommonParameters</span></span>
<span data-ttu-id="82386-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82386-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82386-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82386-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82386-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82386-136">INPUTS</span></span>

### <span data-ttu-id="82386-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="82386-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="82386-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82386-138">OUTPUTS</span></span>

### <span data-ttu-id="82386-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82386-139">System.Boolean</span></span>

## <span data-ttu-id="82386-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82386-140">NOTES</span></span>

<span data-ttu-id="82386-141">ALIASE</span><span class="sxs-lookup"><span data-stu-id="82386-141">ALIASES</span></span>

<span data-ttu-id="82386-142">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="82386-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82386-143">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82386-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82386-144">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82386-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82386-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="82386-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="82386-146">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="82386-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="82386-147">`CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App.</span><span class="sxs-lookup"><span data-stu-id="82386-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="82386-148">Die App-Ressourcen-ID hat das Format /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsslots und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} für andere Slots.</span><span class="sxs-lookup"><span data-stu-id="82386-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="82386-149">`[Kind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="82386-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="82386-150">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="82386-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="82386-151">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="82386-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82386-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientaffinität, zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiter <code>false</code> routen.</span><span class="sxs-lookup"><span data-stu-id="82386-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="82386-153">Der Standardwert ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="82386-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS-gegenseitige Authentifizierung). Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="82386-155">Der Standardwert ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="82386-156">`[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="82386-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="82386-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellungsüberschreibungen für geklonte Apps.</span><span class="sxs-lookup"><span data-stu-id="82386-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="82386-158">Falls angegeben, setzen diese Einstellungen die Einstellungen außer Kraft, die aus der Quell-App geklont werden.</span><span class="sxs-lookup"><span data-stu-id="82386-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="82386-159">Andernfalls bleiben die Anwendungseinstellungen der Quell-App erhalten.</span><span class="sxs-lookup"><span data-stu-id="82386-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="82386-160">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="82386-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82386-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> um benutzerdefinierte Hostnamen aus der #A0 zu klonen. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82386-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> um das Quellsteuerelement aus der #A0 zu klonen. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82386-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell- und Ziel-App.</span><span class="sxs-lookup"><span data-stu-id="82386-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="82386-164">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs.</span><span class="sxs-lookup"><span data-stu-id="82386-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="82386-165">Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="82386-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="82386-166">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="82386-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="82386-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> um die #A0 zu überschreiben. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82386-168">`[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App, beispiel: USA, Westen oder Europa, Norden</span><span class="sxs-lookup"><span data-stu-id="82386-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="82386-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM Ressourcen-ID des zu verwendende Datenverkehrs-Manager-Profils, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="82386-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="82386-170">Die Ressourcen-ID des Datenverkehrs-Managers liegt im Format "/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}" vor.</span><span class="sxs-lookup"><span data-stu-id="82386-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="82386-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic-Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="82386-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="82386-172">Dies ist nur erforderlich, wenn das Profil von Traffic Manager noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="82386-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="82386-173">`[Config <ISiteConfig>]`: Konfiguration der App.</span><span class="sxs-lookup"><span data-stu-id="82386-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="82386-174">`IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt es fest, das angibt, ob der Pushendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82386-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="82386-175">`[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausgeführt werden muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="82386-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="82386-176">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.</span><span class="sxs-lookup"><span data-stu-id="82386-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="82386-177">`[AlwaysOn <Boolean?>]`: <code>true</code> wenn "Immer aktiviert" aktiviert ist; andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-178">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="82386-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="82386-179">`[ApiManagementConfigId <String>]`: APIM-Api-ID.</span><span class="sxs-lookup"><span data-stu-id="82386-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="82386-180">`[AppCommandLine <String>]`: Startbefehlszeile der App.</span><span class="sxs-lookup"><span data-stu-id="82386-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="82386-181">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="82386-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="82386-182">`[Name <String>]`: Name des Koppelns.</span><span class="sxs-lookup"><span data-stu-id="82386-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="82386-183">`[Value <String>]`: Paarwert.</span><span class="sxs-lookup"><span data-stu-id="82386-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="82386-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn die automatische Umergnung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-185">`[AutoSwapSlotName <String>]`: Name des automatischen Tauschs von Slot.</span><span class="sxs-lookup"><span data-stu-id="82386-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="82386-186">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="82386-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="82386-187">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="82386-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="82386-188">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="82386-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="82386-189">`[Type <ConnectionStringType?>]`: Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="82386-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="82386-190">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab oder legt sie fest, für die cross-origin-Aufrufe zulässig sein sollen (z. http://example.com:12345) B.:</span><span class="sxs-lookup"><span data-stu-id="82386-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="82386-191">Verwenden Sie "\*", um alle zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="82386-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="82386-192">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="82386-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="82386-193">Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="82386-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="82386-194">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82386-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="82386-195">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="82386-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="82386-196">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="82386-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="82386-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-198">`[DocumentRoot <String>]`: Dokumentstamm</span><span class="sxs-lookup"><span data-stu-id="82386-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="82386-199">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von dynamischen Tags enthält, die von Denkwerten im Pushregistrierungsendpunkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="82386-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="82386-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Regeln für die Einlaufung.</span><span class="sxs-lookup"><span data-stu-id="82386-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="82386-201">`[ActionHostName <String>]`: Hostname eines Slot, an das der Datenverkehr umgeleitet wird, wenn dies entschieden ist.</span><span class="sxs-lookup"><span data-stu-id="82386-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="82386-202">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="82386-202">E.g.</span></span> <span data-ttu-id="82386-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="82386-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="82386-204">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, welche URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="82386-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="82386-205">Informationen zum Gerüst und zu Verträgen finden Sie unter "TiPCallback-Websiteerweiterung".</span><span class="sxs-lookup"><span data-stu-id="82386-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="82386-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="82386-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="82386-207">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um "ReroutePercentage" neu zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="82386-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="82386-208">`[ChangeStep <Double?>]`: Im Szenario für die automatische Erstrecherhung ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> ist.</span><span class="sxs-lookup"><span data-stu-id="82386-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="82386-209">Websitemetriken werden alle N Minuten überprüft, die im ".\nCustom"-Entscheidungsalgorithmus angegeben sind, können in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der die <code>ChangeIntervalInMinutes</code> URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.</span><span class="sxs-lookup"><span data-stu-id="82386-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="82386-210">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="82386-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="82386-211">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der "ReroutePercentage" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="82386-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="82386-212">`[Name <String>]`: Name der Routingregel.</span><span class="sxs-lookup"><span data-stu-id="82386-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="82386-213">Der empfohlene Name ist, auf den Platz zu verweisen, der den Datenverkehr im Experiment erhält.</span><span class="sxs-lookup"><span data-stu-id="82386-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="82386-214">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der umgeleitet <code>ActionHostName</code> wird.</span><span class="sxs-lookup"><span data-stu-id="82386-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="82386-215">`[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts</span><span class="sxs-lookup"><span data-stu-id="82386-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="82386-216">`[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="82386-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="82386-217">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82386-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="82386-218">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen Anwendung FastCGI verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="82386-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="82386-219">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="82386-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="82386-220">`[HealthCheckPath <String>]`: Pfad der Integritätsprüfung</span><span class="sxs-lookup"><span data-stu-id="82386-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="82386-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website, damit Clients die Verbindung über http2.0 herstellen können.</span><span class="sxs-lookup"><span data-stu-id="82386-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="82386-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="82386-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für "main".</span><span class="sxs-lookup"><span data-stu-id="82386-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="82386-224">`[Action <String>]`: Zugriff für diesen IP-Bereich zulassen oder verweigern.</span><span class="sxs-lookup"><span data-stu-id="82386-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="82386-225">`[Description <String>]`: Beschreibung der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="82386-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="82386-226">`[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="82386-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="82386-227">Sie kann in Form einer reinen ipv4-Adresse (erforderliche Subnetzmask-Eigenschaft) oder einer CIDR-Notation wie "ipv4/mask" (führende Bit-Übereinstimmung) liegen.</span><span class="sxs-lookup"><span data-stu-id="82386-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="82386-228">Bei CIDR darf die Eigenschaft "SubnetMask" nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="82386-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="82386-229">`[Name <String>]`: Name der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="82386-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="82386-230">`[Priority <Int32?>]`: Priorität der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="82386-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="82386-231">`[SubnetMask <String>]`: Subnetzformat für den Bereich von IP-Adressen, für den die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="82386-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="82386-232">`[SubnetTrafficTag <Int32?>]`: (intern) Tag für Subnetzdatenverkehr</span><span class="sxs-lookup"><span data-stu-id="82386-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="82386-233">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82386-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="82386-234">Dies ist die Unterstützung der IP-Filterung auf Proxys.</span><span class="sxs-lookup"><span data-stu-id="82386-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="82386-235">`[VnetSubnetResourceId <String>]`: Ressourcen-ID des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="82386-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="82386-236">`[VnetTrafficTag <Int32?>]`: (intern) Vnet-Datenverkehrstag</span><span class="sxs-lookup"><span data-stu-id="82386-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="82386-237">`[JavaContainer <String>]`: Java Container.</span><span class="sxs-lookup"><span data-stu-id="82386-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="82386-238">`[JavaContainerVersion <String>]`: Java Containerversion.</span><span class="sxs-lookup"><span data-stu-id="82386-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="82386-239">`[JavaVersion <String>]`: Java Version.</span><span class="sxs-lookup"><span data-stu-id="82386-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="82386-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="82386-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="82386-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="82386-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="82386-242">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.</span><span class="sxs-lookup"><span data-stu-id="82386-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="82386-243">`[LinuxFxVersion <String>]`: Linux-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="82386-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="82386-244">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.</span><span class="sxs-lookup"><span data-stu-id="82386-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="82386-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> zum Aktivieren des lokalen MySQL. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-246">`[LogsDirectorySizeLimit <Int32?>]`: Beschränkung der Größe des HTTP-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="82386-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="82386-247">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="82386-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="82386-248">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="82386-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="82386-249">`[MachineKeyValidation <String>]`: MachineKey-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="82386-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="82386-250">`[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="82386-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="82386-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="82386-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="82386-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity ID</span><span class="sxs-lookup"><span data-stu-id="82386-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="82386-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die mindestversion von TLS, die für -SSL-Anforderungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="82386-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="82386-254">`[NetFrameworkVersion <String>]`: .NET Framework-Version.</span><span class="sxs-lookup"><span data-stu-id="82386-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="82386-255">`[NodeVersion <String>]`: Version Node.js.</span><span class="sxs-lookup"><span data-stu-id="82386-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="82386-256">`[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="82386-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="82386-257">`[PhpVersion <String>]`: Version von PHP.</span><span class="sxs-lookup"><span data-stu-id="82386-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="82386-258">`[PowerShellVersion <String>]`: Version von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82386-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="82386-259">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorab angezeigten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="82386-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="82386-260">Diese Einstellung gilt nur für die Verbrauchs- und Plänen</span><span class="sxs-lookup"><span data-stu-id="82386-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="82386-261">`[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens</span><span class="sxs-lookup"><span data-stu-id="82386-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="82386-262">`[PushKind <String>]`: Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="82386-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="82386-263">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="82386-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="82386-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn remote debuggen aktiviert ist. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-265">`[RemoteDebuggingVersion <String>]`: Remotedebugversion.</span><span class="sxs-lookup"><span data-stu-id="82386-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="82386-266">`[RequestCount <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="82386-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="82386-267">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="82386-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="82386-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="82386-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-269">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="82386-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="82386-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.</span><span class="sxs-lookup"><span data-stu-id="82386-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="82386-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für Scm zur Verwendung des Haupts.</span><span class="sxs-lookup"><span data-stu-id="82386-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="82386-272">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="82386-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="82386-273">`[SlowRequestCount <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="82386-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="82386-274">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="82386-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="82386-275">`[SlowRequestTimeTaken <String>]`: Genommene Zeit.</span><span class="sxs-lookup"><span data-stu-id="82386-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="82386-276">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die für die Verwendung durch den Pushregistrierungsendpunkt auf der Whiteliste aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="82386-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="82386-277">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste von Tags enthält, die die Verwendung der Benutzerauthentifizierung am Pushregistrierungsendpunkt erfordern.</span><span class="sxs-lookup"><span data-stu-id="82386-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="82386-278">Tags können aus alphanumerischen Zeichen bestehen und folgende Zeichen enthalten: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="82386-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="82386-279">Die Überprüfung sollte im PushRequestHandler durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="82386-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="82386-280">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="82386-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="82386-281">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel basierend auf privaten Bytes.</span><span class="sxs-lookup"><span data-stu-id="82386-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="82386-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="82386-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="82386-283">`[Count <Int32?>]`: Anzahl anfragen.</span><span class="sxs-lookup"><span data-stu-id="82386-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="82386-284">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="82386-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="82386-285">`[SubStatus <Int32?>]`: Unterstatus anfordern.</span><span class="sxs-lookup"><span data-stu-id="82386-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="82386-286">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="82386-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="82386-287">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="82386-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="82386-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> um den 32-Bit-Workerprozess zu verwenden. <code>false</code> Andernfalls.</span><span class="sxs-lookup"><span data-stu-id="82386-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="82386-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="82386-290">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="82386-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="82386-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="82386-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="82386-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="82386-293">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="82386-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="82386-294">`[VirtualPath <String>]`: Pfad zu virtueller Anwendung.</span><span class="sxs-lookup"><span data-stu-id="82386-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="82386-295">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="82386-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="82386-296">`[VnetName <String>]`: Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="82386-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="82386-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="82386-298">`[WindowsFxVersion <String>]`: Xenon-App-Framework und -Version</span><span class="sxs-lookup"><span data-stu-id="82386-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="82386-299">`[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste</span><span class="sxs-lookup"><span data-stu-id="82386-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="82386-300">`[ContainerSize <Int32?>]`: Größe des Funktionscontainers.</span><span class="sxs-lookup"><span data-stu-id="82386-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="82386-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicherzeitkontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="82386-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="82386-302">`[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist. Andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="82386-303">Wenn Sie diesen Wert auf "false" festlegen, wird die App deaktiviert (die App wird offline geschaltet).</span><span class="sxs-lookup"><span data-stu-id="82386-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="82386-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname-SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="82386-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="82386-305">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.</span><span class="sxs-lookup"><span data-stu-id="82386-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="82386-306">`[Name <String>]`: Hostname.</span><span class="sxs-lookup"><span data-stu-id="82386-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="82386-307">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="82386-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="82386-308">`[Thumbprint <String>]`: FINGERABDRUCK DES SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="82386-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="82386-309">`[ToUpdate <Boolean?>]`: Wird so <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="82386-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="82386-310">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82386-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="82386-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="82386-312">Wenn, <code>true</code> kann auf die App nur über die API-Verwaltungsprozesse zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="82386-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="82386-313">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="82386-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="82386-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: Konfiguriert eine Website so, dass nur https-Anfragen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="82386-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="82386-315">Problemumleitung für http-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82386-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="82386-316">`[HyperV <Boolean?>]`: Hyper-V Sandbox.</span><span class="sxs-lookup"><span data-stu-id="82386-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="82386-317">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="82386-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="82386-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="82386-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="82386-319">Die Verweise auf benutzeridentitätswörterbücher sind ARM Ressourcen-IDs im Format '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="82386-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="82386-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="82386-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="82386-321">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.</span><span class="sxs-lookup"><span data-stu-id="82386-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="82386-322">`[RedundancyMode <RedundancyMode?>]`: Modus "Websiteredundanz"</span><span class="sxs-lookup"><span data-stu-id="82386-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="82386-323">`[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="82386-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> zum Beenden der #A0 (KUDU), wenn die App beendet wird. Andernfalls. <code>false</code></span><span class="sxs-lookup"><span data-stu-id="82386-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="82386-325">Die Standardeinstellung ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="82386-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="82386-326">`[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App-Serviceplans, formatiert mit: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="82386-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="82386-327">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82386-327">RELATED LINKS</span></span>

