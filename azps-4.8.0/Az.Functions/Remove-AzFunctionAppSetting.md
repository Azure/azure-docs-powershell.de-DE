---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174724"
---
# <span data-ttu-id="c7217-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="c7217-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="c7217-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7217-102">SYNOPSIS</span></span>
<span data-ttu-id="c7217-103">Entfernt App-Einstellungen aus einer Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="c7217-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="c7217-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7217-104">SYNTAX</span></span>

### <span data-ttu-id="c7217-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7217-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7217-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="c7217-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7217-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7217-107">DESCRIPTION</span></span>
<span data-ttu-id="c7217-108">Entfernt App-Einstellungen aus einer Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="c7217-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="c7217-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7217-109">EXAMPLES</span></span>

### <span data-ttu-id="c7217-110">Beispiel 1: Entfernen von App-Einstellungen in einer Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="c7217-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="c7217-111">Dieser Befehl entfernt App-Einstellungen in einer Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="c7217-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="c7217-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7217-112">PARAMETERS</span></span>

### <span data-ttu-id="c7217-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="c7217-113">-AppSettingName</span></span>
<span data-ttu-id="c7217-114">Liste der Funktions-APP-Einstellungen, die aus der Funktions-APP entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7217-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7217-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7217-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="c7217-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c7217-116">-Force</span></span>
<span data-ttu-id="c7217-117">Erzwingt das Cmdlet zum Entfernen der Funktion-app-Einstellung ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="c7217-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c7217-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7217-118">-InputObject</span></span>
<span data-ttu-id="c7217-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c7217-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c7217-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c7217-120">-Name</span></span>
<span data-ttu-id="c7217-121">Der Name der Funktions-APP.</span><span class="sxs-lookup"><span data-stu-id="c7217-121">Name of the function app.</span></span>

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

### <span data-ttu-id="c7217-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7217-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7217-123">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="c7217-123">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="c7217-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c7217-124">-SubscriptionId</span></span>
<span data-ttu-id="c7217-125">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c7217-125">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="c7217-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7217-126">-Confirm</span></span>
<span data-ttu-id="c7217-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7217-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7217-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7217-128">-WhatIf</span></span>
<span data-ttu-id="c7217-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7217-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7217-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7217-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7217-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7217-131">CommonParameters</span></span>
<span data-ttu-id="c7217-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7217-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7217-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7217-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7217-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7217-134">INPUTS</span></span>

### <span data-ttu-id="c7217-135">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="c7217-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="c7217-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7217-136">OUTPUTS</span></span>

### <span data-ttu-id="c7217-137">Microsoft. Azure. PowerShell. Cmdlets. Functions. Models. Api20190801. IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="c7217-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="c7217-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7217-138">NOTES</span></span>

<span data-ttu-id="c7217-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="c7217-139">ALIASES</span></span>

<span data-ttu-id="c7217-140">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7217-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7217-141">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7217-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7217-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c7217-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7217-143">Inputobject <ISite> :</span><span class="sxs-lookup"><span data-stu-id="c7217-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="c7217-144">`Location <String>`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="c7217-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="c7217-145">`CloningInfoSourceWebAppId <String>`: Arm-Ressourcen-ID der Quell-app.</span><span class="sxs-lookup"><span data-stu-id="c7217-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="c7217-146">Die APP-Ressourcen-ID hat das Format/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Web/Sites/{Sitename} für Produktions Steckplätze und/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Web/Sites/{Sitename}/Slots/{slotName} für andere Slots.</span><span class="sxs-lookup"><span data-stu-id="c7217-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="c7217-147">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c7217-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="c7217-148">`[Tag <IResourceTags>]`: Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="c7217-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="c7217-149">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7217-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c7217-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> um die Clientaffinität zu <code>false</code> aktivieren, können Sie das Senden von Sitzungs Affinitäts Cookies beenden, die Clientanforderungen in derselben Sitzung an dieselbe Instanz weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="c7217-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="c7217-151">Standardwert ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="c7217-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> um die Clientzertifikatauthentifizierung (MTLS-gegenseitige Authentifizierung) zu aktivieren, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="c7217-153">Standardwert ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-154">`[ClientCertExclusionPath <String>]`: Clientzertifikatauthentifizierung durch Kommas getrennte Ausschluss Pfade</span><span class="sxs-lookup"><span data-stu-id="c7217-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="c7217-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellung Außerkraftsetzungen für geklonte app.</span><span class="sxs-lookup"><span data-stu-id="c7217-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="c7217-156">Wenn diese Einstellungen angegeben sind, überschreiben Sie die von der Quell-App geklonten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="c7217-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="c7217-157">Andernfalls bleiben die Anwendungseinstellungen aus der Quell-APP erhalten.</span><span class="sxs-lookup"><span data-stu-id="c7217-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="c7217-158">`[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7217-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c7217-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> zum Klonen von benutzerdefinierten Hostnamen aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> zum Klonen der Quellcodeverwaltung aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> zum Konfigurieren des Lastenausgleichs für die Quell-und Ziel-app.</span><span class="sxs-lookup"><span data-stu-id="c7217-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="c7217-162">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Cloning-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c7217-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="c7217-163">Diese ID bindet mehrere Cloning-Vorgänge zusammen, um denselben Snapshot zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7217-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="c7217-164">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="c7217-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="c7217-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> zum Überschreiben der Ziel-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-166">`[CloningInfoSourceWebAppLocation <String>]`: Standort der Quell-App Ex: West-und Nordeuropa</span><span class="sxs-lookup"><span data-stu-id="c7217-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="c7217-167">`[CloningInfoTrafficManagerProfileId <String>]`: Arm-Ressourcen-ID des zu verwendenden Traffic Manager-Profils, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7217-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="c7217-168">Die Datenverkehrs-Manager-Ressourcen-ID hat das Format/Subscriptions/{subId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.Network/trafficManagerProfiles/{ProfileName}.</span><span class="sxs-lookup"><span data-stu-id="c7217-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="c7217-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellenden Traffic Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="c7217-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="c7217-170">Dies ist nur erforderlich, wenn das Traffic Manager-Profil noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c7217-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="c7217-171">`[Config <ISiteConfig>]`: Konfiguration der app.</span><span class="sxs-lookup"><span data-stu-id="c7217-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="c7217-172">`IsPushEnabled <Boolean>`: Ruft ein Flag ab, das angibt, ob der Push-Endpunkt aktiviert ist, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="c7217-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="c7217-173">`[ActionMinProcessExecutionTime <String>]`: Minimale Zeitdauer, die der Prozess ausführen muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="c7217-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="c7217-174">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7217-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="c7217-175">`[AlwaysOn <Boolean?>]`: <code>true</code> Wenn immer aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-176">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="c7217-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="c7217-177">`[ApiManagementConfigId <String>]`: APIM-Api-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c7217-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="c7217-178">`[AppCommandLine <String>]`: App-Befehlszeile zum Starten.</span><span class="sxs-lookup"><span data-stu-id="c7217-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="c7217-179">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c7217-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="c7217-180">`[Name <String>]`: Pair-Name.</span><span class="sxs-lookup"><span data-stu-id="c7217-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="c7217-181">`[Value <String>]`: Pair-Wert.</span><span class="sxs-lookup"><span data-stu-id="c7217-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="c7217-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> Wenn Auto Heal aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-183">`[AutoSwapSlotName <String>]`: Automatisches austauschen des Steckplatz namens.</span><span class="sxs-lookup"><span data-stu-id="c7217-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="c7217-184">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c7217-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="c7217-185">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7217-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="c7217-186">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7217-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="c7217-187">`[Type <ConnectionStringType?>]`: Typ der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c7217-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="c7217-188">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab, die für die über-Origin-Aufrufe zulässig sein sollen (beispielsweise: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="c7217-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="c7217-189">Verwenden Sie "\*", um alle zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c7217-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="c7217-190">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c7217-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="c7217-191">Weitere Informationen finden Sie unter         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         .</span><span class="sxs-lookup"><span data-stu-id="c7217-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="c7217-192">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7217-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="c7217-193">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="c7217-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="c7217-194">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="c7217-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="c7217-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> Wenn die detaillierte Fehlerprotokollierung aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-196">`[DocumentRoot <String>]`: Dokumentstamm.</span><span class="sxs-lookup"><span data-stu-id="c7217-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="c7217-197">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab, die eine Liste der dynamischen Tags enthält, die aus benutzeransprüchen im Push-Registrierungs Endpunkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="c7217-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="c7217-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Weiterverfolgungs Regeln.</span><span class="sxs-lookup"><span data-stu-id="c7217-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="c7217-199">`[ActionHostName <String>]`: Hostname eines Slots, in den der Datenverkehr umgeleitet wird, wenn entschieden wird.</span><span class="sxs-lookup"><span data-stu-id="c7217-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="c7217-200">Z.b..</span><span class="sxs-lookup"><span data-stu-id="c7217-200">E.g.</span></span> <span data-ttu-id="c7217-201">MyApp-Stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="c7217-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="c7217-202">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungs Algorithmus kann in TiPCallback Site Extension bereitgestellt werden, die URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7217-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="c7217-203">Informationen finden Sie unter TiPCallback Site Extension für das Gerüst und die Verträge.</span><span class="sxs-lookup"><span data-stu-id="c7217-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="c7217-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="c7217-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="c7217-205">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um ReroutePercentage neu auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="c7217-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="c7217-206">`[ChangeStep <Double?>]`: Im Szenario für das automatische Hochfahren ist dies der Schritt zum hinzufügen/entfernen, <code>ReroutePercentage</code> bis er \n <code>MinReroutePercentage</code> oder erreicht         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="c7217-207">Website Metriken werden überprüft alle N Minuten <code>ChangeIntervalInMinutes</code> , die im .\nCustom-Entscheidungs Algorithmus angegeben sind, können in TiPCallback Site Extension bereitgestellt werden, in der URL angegeben werden kann <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="c7217-208">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der ReroutePercentage bleibt.</span><span class="sxs-lookup"><span data-stu-id="c7217-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="c7217-209">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der ReroutePercentage bleibt.</span><span class="sxs-lookup"><span data-stu-id="c7217-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="c7217-210">`[Name <String>]`: Name der Routingregel</span><span class="sxs-lookup"><span data-stu-id="c7217-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="c7217-211">Der empfohlene Name lautet, auf den Steckplatz zu zeigen, der den Datenverkehr im Experiment empfängt.</span><span class="sxs-lookup"><span data-stu-id="c7217-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="c7217-212">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, zu dem umgeleitet wird <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="c7217-213">`[FtpsState <FtpsState?>]`: Zustand des FTP/FTP-Diensts</span><span class="sxs-lookup"><span data-stu-id="c7217-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="c7217-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler-Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="c7217-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="c7217-215">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7217-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="c7217-216">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mithilfe der angegebenen FastCGI-Anwendung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c7217-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="c7217-217">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c7217-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="c7217-218">`[HealthCheckPath <String>]`: Pfad für Integritätsprüfung</span><span class="sxs-lookup"><span data-stu-id="c7217-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="c7217-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfiguriert eine Website, um Clients die Verbindung über http 2.0 zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c7217-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="c7217-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> Wenn die HTTP-Protokollierung aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für Main.</span><span class="sxs-lookup"><span data-stu-id="c7217-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="c7217-222">`[Action <String>]`: Gewähren oder Verweigern des Zugriffs für diesen IP-Bereich.</span><span class="sxs-lookup"><span data-stu-id="c7217-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="c7217-223">`[Description <String>]`: Beschreibung der IP-Einschränkungs Regel</span><span class="sxs-lookup"><span data-stu-id="c7217-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="c7217-224">`[IPAddress <String>]`: IP-Adresse die Sicherheitsbeschränkung ist gültig für.</span><span class="sxs-lookup"><span data-stu-id="c7217-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="c7217-225">Sie kann in Form einer reinen IPv4-Adresse (erforderliche Subnetzmaske-Eigenschaft) oder CIDR-Notation wie IPv4/Mask (Leading Bit Match) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c7217-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="c7217-226">Für CIDR darf keine Subnetzmaske-Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c7217-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="c7217-227">`[Name <String>]`: Name der IP-Einschränkungs Regel</span><span class="sxs-lookup"><span data-stu-id="c7217-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="c7217-228">`[Priority <Int32?>]`: Priorität der IP-Einschränkungs Regel</span><span class="sxs-lookup"><span data-stu-id="c7217-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="c7217-229">`[SubnetMask <String>]`: Subnetzmaske für den Bereich der IP-Adressen, für die die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="c7217-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="c7217-230">`[SubnetTrafficTag <Int32?>]`: (interner) Subnet Traffic-Tag</span><span class="sxs-lookup"><span data-stu-id="c7217-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="c7217-231">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7217-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="c7217-232">Dadurch wird die IP-Filterung für Proxys unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7217-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="c7217-233">`[VnetSubnetResourceId <String>]`: Virtuelle Netzwerk-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c7217-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="c7217-234">`[VnetTrafficTag <Int32?>]`: (intern) vnet Traffic-Tag</span><span class="sxs-lookup"><span data-stu-id="c7217-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="c7217-235">`[JavaContainer <String>]`: Java-Container.</span><span class="sxs-lookup"><span data-stu-id="c7217-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="c7217-236">`[JavaContainerVersion <String>]`: Java-Container Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="c7217-237">`[JavaVersion <String>]`: Java-Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="c7217-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="c7217-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="c7217-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="c7217-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="c7217-240">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässige CPU-Auslastung Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="c7217-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="c7217-241">`[LinuxFxVersion <String>]`: Linux-App-Framework und-Version</span><span class="sxs-lookup"><span data-stu-id="c7217-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="c7217-242">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich für Websites.</span><span class="sxs-lookup"><span data-stu-id="c7217-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="c7217-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> um lokales MySQL zu aktivieren, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-244">`[LogsDirectorySizeLimit <Int32?>]`: Maximale Größe des http-Logs-Verzeichnisses.</span><span class="sxs-lookup"><span data-stu-id="c7217-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="c7217-245">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7217-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="c7217-246">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c7217-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="c7217-247">`[MachineKeyValidation <String>]`: MachineKey-Validierung.</span><span class="sxs-lookup"><span data-stu-id="c7217-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="c7217-248">`[MachineKeyValidationKey <String>]`: Gültigkeits Taste.</span><span class="sxs-lookup"><span data-stu-id="c7217-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="c7217-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="c7217-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="c7217-250">`[ManagedServiceIdentityId <Int32?>]`: Verwaltete Dienst Identitäts-ID</span><span class="sxs-lookup"><span data-stu-id="c7217-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="c7217-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfiguriert die für SSL-Anforderungen erforderliche minimale Version von TLS</span><span class="sxs-lookup"><span data-stu-id="c7217-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="c7217-252">`[NetFrameworkVersion <String>]`: .NET Framework-Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="c7217-253">`[NodeVersion <String>]`: Version von Node.js.</span><span class="sxs-lookup"><span data-stu-id="c7217-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="c7217-254">`[NumberOfWorker <Int32?>]`: Anzahl der Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="c7217-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="c7217-255">`[PhpVersion <String>]`: PHP-Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="c7217-256">`[PowerShellVersion <String>]`: PowerShell-Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="c7217-257">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vorgewärmten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="c7217-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="c7217-258">Diese Einstellung gilt nur für den Verbrauch und die elastischen Pläne.</span><span class="sxs-lookup"><span data-stu-id="c7217-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="c7217-259">`[PublishingUsername <String>]`: Veröffentlichungs Benutzername.</span><span class="sxs-lookup"><span data-stu-id="c7217-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="c7217-260">`[PushKind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c7217-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="c7217-261">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="c7217-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="c7217-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> Wenn das Remotedebuggen aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-263">`[RemoteDebuggingVersion <String>]`: Remote Debugging-Version.</span><span class="sxs-lookup"><span data-stu-id="c7217-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="c7217-264">`[RequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="c7217-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="c7217-265">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="c7217-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="c7217-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> Wenn die Anforderungs Ablaufverfolgung aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-267">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c7217-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="c7217-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für SCM.</span><span class="sxs-lookup"><span data-stu-id="c7217-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="c7217-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für SCM, um Main zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7217-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="c7217-270">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="c7217-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="c7217-271">`[SlowRequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="c7217-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="c7217-272">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="c7217-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="c7217-273">`[SlowRequestTimeTaken <String>]`: Zeitaufwand.</span><span class="sxs-lookup"><span data-stu-id="c7217-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="c7217-274">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge mit einer Liste von Tags ab, die für die Verwendung durch den Push-Registrierungs Endpunkt whitelisted sind, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c7217-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="c7217-275">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge mit einer Liste von Tags ab, für die die Benutzerauthentifizierung im Push-Registrierungs Endpunkt verwendet werden muss, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c7217-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="c7217-276">Tags können aus alphanumerischen Zeichen und folgendem bestehen: "_"; "@"; "#"; "."; ":"; "-".</span><span class="sxs-lookup"><span data-stu-id="c7217-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="c7217-277">Die Validierung sollte am PushRequestHandler durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c7217-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="c7217-278">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="c7217-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="c7217-279">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel, die auf privaten Bytes basiert.</span><span class="sxs-lookup"><span data-stu-id="c7217-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="c7217-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="c7217-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="c7217-281">`[Count <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="c7217-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="c7217-282">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="c7217-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="c7217-283">`[SubStatus <Int32?>]`: Untergeordneten Status anfordern.</span><span class="sxs-lookup"><span data-stu-id="c7217-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="c7217-284">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="c7217-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="c7217-285">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c7217-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="c7217-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> So verwenden Sie den 32-Bit-Workerprozess; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c7217-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="c7217-288">`[PhysicalPath <String>]`: Physikalischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="c7217-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="c7217-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> Wenn das Vorabladen aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="c7217-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c7217-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="c7217-291">`[PhysicalPath <String>]`: Physikalischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="c7217-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="c7217-292">`[VirtualPath <String>]`: Pfad zur virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c7217-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="c7217-293">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="c7217-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="c7217-294">`[VnetName <String>]`: Virtueller Netzwerkname.</span><span class="sxs-lookup"><span data-stu-id="c7217-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="c7217-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> Wenn WebSocket aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="c7217-296">`[WindowsFxVersion <String>]`: Xenon-App-Framework und-Version</span><span class="sxs-lookup"><span data-stu-id="c7217-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="c7217-297">`[XManagedServiceIdentityId <Int32?>]`: Explizite verwaltete Dienst Identitäts-ID</span><span class="sxs-lookup"><span data-stu-id="c7217-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="c7217-298">`[ContainerSize <Int32?>]`: Größe des Funktions Containers.</span><span class="sxs-lookup"><span data-stu-id="c7217-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="c7217-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässige tägliche Speicherzeit Kontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="c7217-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="c7217-300">`[Enabled <Boolean?>]`: <code>true</code> Wenn die App aktiviert ist, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="c7217-301">Wenn dieser Wert auf "false" festgelegt wird, wird die APP deaktiviert (übernimmt die APP offline).</span><span class="sxs-lookup"><span data-stu-id="c7217-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="c7217-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Status werden verwendet, um die SSL-Bindungen für die Hostnamen der APP zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c7217-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="c7217-303">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard-oder Repository-Hostname ist.</span><span class="sxs-lookup"><span data-stu-id="c7217-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="c7217-304">`[Name <String>]`Hostname.</span><span class="sxs-lookup"><span data-stu-id="c7217-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="c7217-305">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="c7217-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="c7217-306">`[Thumbprint <String>]`: Fingerabdruck des SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="c7217-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="c7217-307">`[ToUpdate <Boolean?>]`: Auf <code>true</code> , um vorhandenen Hostnamen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c7217-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="c7217-308">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c7217-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="c7217-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> zum Deaktivieren der öffentlichen hostnames der APP; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="c7217-310">Wenn <code>true</code> die app nur über API-Verwaltungsprozess zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="c7217-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="c7217-311">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der APP-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="c7217-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="c7217-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguriert eine Website so, dass nur HTTPS-Anforderungen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="c7217-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="c7217-313">Probleme beim Umleiten für HTTP-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7217-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="c7217-314">`[HyperV <Boolean?>]`: Hyper-V-Sandbox.</span><span class="sxs-lookup"><span data-stu-id="c7217-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="c7217-315">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="c7217-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="c7217-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der Benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c7217-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="c7217-317">Die Schlüssel Verweise für das Benutzer-ID-Wörterbuch sind arm-Ressourcen-IDs im folgenden Format: "/Subscriptions/{SubscriptionId}/resourceGroups/{resourceGroupName}/Providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="c7217-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="c7217-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7217-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c7217-319">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandbox.</span><span class="sxs-lookup"><span data-stu-id="c7217-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="c7217-320">`[RedundancyMode <RedundancyMode?>]`: Website Redundanzmodus</span><span class="sxs-lookup"><span data-stu-id="c7217-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="c7217-321">`[Reserved <Boolean?>]`: <code>true</code> Wenn reserviert; andernfalls; <code>false</code></span><span class="sxs-lookup"><span data-stu-id="c7217-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> um die SCM-Website (KUDU) zu beenden, wenn die APP angehalten wird, andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="c7217-323">Der Standardwert ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="c7217-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="c7217-324">`[ServerFarmId <String>]`: Ressourcen-ID des zugehörigen App-Service Plans, formatiert als: "/Subscriptions/{subscriptionID}/resourceGroups/{GroupName}/Providers/Microsoft.Web/Serverfarms/{appServicePlanName}"</span><span class="sxs-lookup"><span data-stu-id="c7217-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="c7217-325">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7217-325">RELATED LINKS</span></span>

