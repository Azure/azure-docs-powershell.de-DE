---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/start-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
ms.openlocfilehash: 629cad3d54c575eb9f68dfbef43f1cbdd0502c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928627"
---
# <span data-ttu-id="0b1b3-101">Start-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0b1b3-101">Start-AzFunctionApp</span></span>

## <span data-ttu-id="0b1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b1b3-103">Startet eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-103">Starts a function app.</span></span>

## <span data-ttu-id="0b1b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b1b3-104">SYNTAX</span></span>

### <span data-ttu-id="0b1b3-105">StartByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b1b3-105">StartByName (Default)</span></span>
```
Start-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b1b3-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="0b1b3-106">ByObjectInput</span></span>
```
Start-AzFunctionApp -InputObject <ISite> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0b1b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b1b3-107">DESCRIPTION</span></span>
<span data-ttu-id="0b1b3-108">Startet eine Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-108">Starts a function app.</span></span>

## <span data-ttu-id="0b1b3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b1b3-109">EXAMPLES</span></span>

### <span data-ttu-id="0b1b3-110">Beispiel 1: Holen Sie sich eine Funktions-App nach Name, und starten Sie sie.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-110">Example 1: Get a function app by name and start it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Start-AzFunctionApp
```

<span data-ttu-id="0b1b3-111">Dieser Befehl ruft eine Funktions-App nach Name ab und startet sie.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-111">This command gets a function app by name and starts it.</span></span>

### <span data-ttu-id="0b1b3-112">Beispiel 2: Starten einer Funktions-App nach Name.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-112">Example 2: Start a function app by name.</span></span>
```powershell
PS C:\> Start-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="0b1b3-113">Mit diesem Befehl wird eine Funktions-App nach Name gestartet.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-113">This command starts a function app by name.</span></span>

## <span data-ttu-id="0b1b3-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b1b3-114">PARAMETERS</span></span>

### <span data-ttu-id="0b1b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b1b3-115">-DefaultProfile</span></span>
<span data-ttu-id="0b1b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b1b3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b1b3-117">-InputObject</span></span>
<span data-ttu-id="0b1b3-118">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b1b3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b1b3-119">-Name</span></span>
<span data-ttu-id="0b1b3-120">Der Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-120">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1b3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b1b3-121">-PassThru</span></span>
<span data-ttu-id="0b1b3-122">Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-122">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="0b1b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b1b3-123">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1b3-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b1b3-124">-SubscriptionId</span></span>
<span data-ttu-id="0b1b3-125">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b1b3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0b1b3-126">-Confirm</span></span>
<span data-ttu-id="0b1b3-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b1b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b1b3-128">-WhatIf</span></span>
<span data-ttu-id="0b1b3-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b1b3-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b1b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b1b3-131">CommonParameters</span></span>
<span data-ttu-id="0b1b3-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b1b3-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b1b3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b1b3-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b1b3-134">INPUTS</span></span>

### <span data-ttu-id="0b1b3-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="0b1b3-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="0b1b3-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b1b3-136">OUTPUTS</span></span>

### <span data-ttu-id="0b1b3-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0b1b3-137">System.Boolean</span></span>

## <span data-ttu-id="0b1b3-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b1b3-138">NOTES</span></span>

<span data-ttu-id="0b1b3-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0b1b3-139">ALIASES</span></span>

<span data-ttu-id="0b1b3-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0b1b3-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b1b3-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b1b3-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b1b3-143">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="0b1b3-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="0b1b3-144">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="0b1b3-145">`CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="0b1b3-146">Die App-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsplätze und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="0b1b3-147">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="0b1b3-148">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0b1b3-149">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b1b3-150">`[ClientAffinityEnabled <Boolean?>]`: zum Aktivieren der Clientaffinität; zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an <code>true</code> <code>false</code> dieselbe Instanz weiterrouten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="0b1b3-151">Standard ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="0b1b3-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS Mutual Authentication); andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="0b1b3-153">Standard ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-154">`[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="0b1b3-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="0b1b3-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellung außer Kraft für geklonte Apps.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="0b1b3-156">Wenn angegeben, setzen diese Einstellungen die aus der Quell-App geklonten Einstellungen außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="0b1b3-157">Andernfalls bleiben die Anwendungseinstellungen aus der Quell-App erhalten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="0b1b3-158">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b1b3-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> zum Klonen von benutzerdefinierten Hostnamen aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> zum Klonen der Quellcodeverwaltung aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> so konfigurieren Sie den Lastenausgleich für die Quell- und Ziel-App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="0b1b3-162">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="0b1b3-163">Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="0b1b3-164">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="0b1b3-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> zum Überschreiben der Ziel-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-166">`[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App ex: West US oder North Europe</span><span class="sxs-lookup"><span data-stu-id="0b1b3-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="0b1b3-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ressourcen-ID des Traffic Manager-Profils, das verwendet werden soll, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="0b1b3-168">Die Traffic Manager-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="0b1b3-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="0b1b3-170">Dies ist nur erforderlich, wenn das Traffic Manager-Profil noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="0b1b3-171">`[Config <ISiteConfig>]`: Konfiguration der App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="0b1b3-172">`IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt fest, ob der Pushendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="0b1b3-173">`[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausführen muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="0b1b3-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="0b1b3-174">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="0b1b3-175">`[AlwaysOn <Boolean?>]`: <code>true</code> wenn Immer ein aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-176">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="0b1b3-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="0b1b3-178">`[AppCommandLine <String>]`: Startbefehlzeile der App.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="0b1b3-179">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="0b1b3-180">`[Name <String>]`: Name des Paares.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="0b1b3-181">`[Value <String>]`: Koppelwert.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="0b1b3-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn Automatisches Verheilen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-183">`[AutoSwapSlotName <String>]`: Name des automatischen Tauschplatzes.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="0b1b3-184">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="0b1b3-185">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="0b1b3-186">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="0b1b3-187">`[Type <ConnectionStringType?>]`: Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="0b1b3-188">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab, die originsübergreifende Aufrufe (z. B. dürfen) zulässig sein sollen, oder legt sie http://example.com:12345) fest.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="0b1b3-189">Verwenden Sie "\*", um alle zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="0b1b3-190">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="0b1b3-191">Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="0b1b3-192">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="0b1b3-193">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="0b1b3-194">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="0b1b3-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-196">`[DocumentRoot <String>]`: Dokumentstamm.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="0b1b3-197">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste dynamischer Tags enthält, die aus Benutzeransprüchen im Pushregistrierungsendpunkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="0b1b3-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Anlaufregeln.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="0b1b3-199">`[ActionHostName <String>]`: Hostname eines Slot, an den der Datenverkehr umgeleitet wird, wenn dies entschieden ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="0b1b3-200">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0b1b3-200">E.g.</span></span> <span data-ttu-id="0b1b3-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="0b1b3-202">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, deren URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="0b1b3-203">Informationen zum Gerüst und den Verträgen finden Sie unter TiPCallback-Websiteerweiterung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="0b1b3-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="0b1b3-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="0b1b3-205">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um den Umleitungsprozentwert neu zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="0b1b3-206">`[ChangeStep <Double?>]`: Im Szenario für automatisches Hochfahren ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="0b1b3-207">Websitemetriken werden alle N Minuten überprüft, die im .\nCustom-Entscheidungsalgorithmus angegeben sind, kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der <code>ChangeIntervalInMinutes</code> die URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="0b1b3-208">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "Umleitungsprozent" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="0b1b3-209">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der die Umleitungslinie bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="0b1b3-210">`[Name <String>]`: Name der Routingregel.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="0b1b3-211">Der empfohlene Name wäre, auf den Slot zu verweisen, der den Datenverkehr im Experiment erhält.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="0b1b3-212">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der an umgeleitet <code>ActionHostName</code> wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="0b1b3-213">`[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts</span><span class="sxs-lookup"><span data-stu-id="0b1b3-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="0b1b3-214">`[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="0b1b3-215">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="0b1b3-216">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen FastCGI-Anwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="0b1b3-217">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="0b1b3-218">`[HealthCheckPath <String>]`: Integritätsprüfungspfad</span><span class="sxs-lookup"><span data-stu-id="0b1b3-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="0b1b3-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website so, dass Clients eine Verbindung über http2.0 herstellen können</span><span class="sxs-lookup"><span data-stu-id="0b1b3-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="0b1b3-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für Main.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="0b1b3-222">`[Action <String>]`: Zulassen oder Verweigern des Zugriffs für diesen IP-Bereich.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="0b1b3-223">`[Description <String>]`: Beschreibung der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="0b1b3-224">`[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="0b1b3-225">Sie kann in Form einer reinen ipv4-Adresse (erforderliche SubnetMask-Eigenschaft) oder cidr-Notation wie ipv4/mask (leading bit match) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="0b1b3-226">Für CIDR darf keine Subnetzmask-Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="0b1b3-227">`[Name <String>]`: Name der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="0b1b3-228">`[Priority <Int32?>]`: Priorität der Regel für DIE IP-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="0b1b3-229">`[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="0b1b3-230">`[SubnetTrafficTag <Int32?>]`: (internes) Subnetzverkehrstag</span><span class="sxs-lookup"><span data-stu-id="0b1b3-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="0b1b3-231">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="0b1b3-232">Dies soll die IP-Filterung für Proxys unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="0b1b3-233">`[VnetSubnetResourceId <String>]`: Virtuelle Netzwerkressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0b1b3-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="0b1b3-234">`[VnetTrafficTag <Int32?>]`: (internes) Vnet-Verkehrstag</span><span class="sxs-lookup"><span data-stu-id="0b1b3-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="0b1b3-235">`[JavaContainer <String>]`: Java Container.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="0b1b3-236">`[JavaContainerVersion <String>]`: Java Containerversion.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="0b1b3-237">`[JavaVersion <String>]`: Java Version.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="0b1b3-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="0b1b3-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="0b1b3-240">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="0b1b3-241">`[LinuxFxVersion <String>]`: Linux App Framework und Version</span><span class="sxs-lookup"><span data-stu-id="0b1b3-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="0b1b3-242">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="0b1b3-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> um lokales MySQL zu aktivieren; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP protokolliert das Verzeichnisgrößenlimit.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="0b1b3-245">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="0b1b3-246">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="0b1b3-247">`[MachineKeyValidation <String>]`: MachineKey-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="0b1b3-248">`[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="0b1b3-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="0b1b3-250">`[ManagedServiceIdentityId <Int32?>]`: Id für verwaltete Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="0b1b3-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="0b1b3-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die für SSL-Anforderungen erforderliche Mindestversion von TLS</span><span class="sxs-lookup"><span data-stu-id="0b1b3-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="0b1b3-252">`[NetFrameworkVersion <String>]`: .NET Framework Version.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="0b1b3-253">`[NodeVersion <String>]`: Version von Node.js.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="0b1b3-254">`[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="0b1b3-255">`[PhpVersion <String>]`: Version von PHP.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="0b1b3-256">`[PowerShellVersion <String>]`: Version von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="0b1b3-257">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vordefinierten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="0b1b3-258">Diese Einstellung gilt nur für die Pläne "Verbrauch" und "Flexible Pläne".</span><span class="sxs-lookup"><span data-stu-id="0b1b3-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="0b1b3-259">`[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="0b1b3-260">`[PushKind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="0b1b3-261">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="0b1b3-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn das Remotedebuding aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-263">`[RemoteDebuggingVersion <String>]`: Remotedebugversion.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="0b1b3-264">`[RequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="0b1b3-265">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="0b1b3-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-267">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="0b1b3-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für scm.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="0b1b3-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für scm für die Verwendung von Main.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="0b1b3-270">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="0b1b3-271">`[SlowRequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="0b1b3-272">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="0b1b3-273">`[SlowRequestTimeTaken <String>]`: Zeit, die sie sich genommen hat.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="0b1b3-274">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die auf der Whitelist für die Verwendung durch den Pushregistrierungsendpunkt stehen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="0b1b3-275">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, für die die Benutzerauthentifizierung im Pushregistrierungsendpunkt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="0b1b3-276">Tags können aus alphanumerischen Zeichen und den folgenden Zeichen bestehen: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="0b1b3-277">Die Überprüfung sollte im PushRequestHandler ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="0b1b3-278">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="0b1b3-279">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel, die auf privaten Bytes basiert.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="0b1b3-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="0b1b3-281">`[Count <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="0b1b3-282">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="0b1b3-283">`[SubStatus <Int32?>]`: Unterstatus anfordern.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="0b1b3-284">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="0b1b3-285">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="0b1b3-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> zum Verwenden des 32-Bit-Workerprozesses; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="0b1b3-288">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="0b1b3-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="0b1b3-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="0b1b3-291">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="0b1b3-292">`[VirtualPath <String>]`: Pfad zur virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="0b1b3-293">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="0b1b3-294">`[VnetName <String>]`: Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="0b1b3-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="0b1b3-296">`[WindowsFxVersion <String>]`: Xenon App Framework und Version</span><span class="sxs-lookup"><span data-stu-id="0b1b3-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="0b1b3-297">`[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste</span><span class="sxs-lookup"><span data-stu-id="0b1b3-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="0b1b3-298">`[ContainerSize <Int32?>]`: Größe des Funktionscontainers.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="0b1b3-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicher-Zeitkontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="0b1b3-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="0b1b3-300">`[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="0b1b3-301">Wenn Sie diesen Wert auf false festlegen, wird die App deaktiviert (die App wird offline geschaltet).</span><span class="sxs-lookup"><span data-stu-id="0b1b3-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="0b1b3-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="0b1b3-303">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="0b1b3-304">`[Name <String>]`: Hostname.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="0b1b3-305">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="0b1b3-306">`[Thumbprint <String>]`: Fingerabdruck des SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="0b1b3-307">`[ToUpdate <Boolean?>]`: So wird <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="0b1b3-308">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="0b1b3-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="0b1b3-310">Wenn <code>true</code> , kann auf die App nur über den API-Verwaltungsvorgang zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="0b1b3-311">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="0b1b3-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguriert eine Website so, dass nur https-Anforderungen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="0b1b3-313">Umleitung von Problemen bei Http-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b1b3-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="0b1b3-314">`[HyperV <Boolean?>]`: Hyper-V-Sandkasten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="0b1b3-315">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="0b1b3-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="0b1b3-317">Die Schlüsselverweise für benutzeridentitätswörterbücher werden ARM Ressourcen-ID im Formular angezeigt: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="0b1b3-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="0b1b3-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0b1b3-319">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandkasten.</span><span class="sxs-lookup"><span data-stu-id="0b1b3-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="0b1b3-320">`[RedundancyMode <RedundancyMode?>]`: Websiteredundanzmodus</span><span class="sxs-lookup"><span data-stu-id="0b1b3-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="0b1b3-321">`[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> um die #A0 (KUDU) zu beenden, wenn die App beendet wird; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="0b1b3-323">Die Standardeinstellung ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0b1b3-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="0b1b3-324">`[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App Service-Plans, formatiert als: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="0b1b3-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="0b1b3-325">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b1b3-325">RELATED LINKS</span></span>

