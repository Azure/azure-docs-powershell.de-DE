---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 5aff9382cbeac47c8d4423769d6256d34d5d109a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927152"
---
# <span data-ttu-id="5a19b-101">Get-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="5a19b-101">Get-AzFunctionAppSetting</span></span>

## <span data-ttu-id="5a19b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a19b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a19b-103">Ruft App-Einstellungen für eine Funktions-App ab.</span><span class="sxs-lookup"><span data-stu-id="5a19b-103">Gets app settings for a function app.</span></span>

## <span data-ttu-id="5a19b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a19b-104">SYNTAX</span></span>

### <span data-ttu-id="5a19b-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a19b-105">ByName (Default)</span></span>
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5a19b-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="5a19b-106">ByObjectInput</span></span>
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5a19b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a19b-107">DESCRIPTION</span></span>
<span data-ttu-id="5a19b-108">Ruft App-Einstellungen für eine Funktions-App ab.</span><span class="sxs-lookup"><span data-stu-id="5a19b-108">Gets app settings for a function app.</span></span>

## <span data-ttu-id="5a19b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a19b-109">EXAMPLES</span></span>

### <span data-ttu-id="5a19b-110">Beispiel 1: Herunterladen der App-Einstellungen einer Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-110">Example 1: Get the app settings of a function app.</span></span>
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5a19b-111">Dieser Befehl ruft die App-Einstellungen einer Funktions-App ab.</span><span class="sxs-lookup"><span data-stu-id="5a19b-111">This command gets the app settings of a function app.</span></span>

## <span data-ttu-id="5a19b-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a19b-112">PARAMETERS</span></span>

### <span data-ttu-id="5a19b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a19b-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="5a19b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a19b-114">-InputObject</span></span>
<span data-ttu-id="5a19b-115">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5a19b-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5a19b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a19b-116">-Name</span></span>
<span data-ttu-id="5a19b-117">Name der Funktions-App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-117">Name of the function app.</span></span>

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

### <span data-ttu-id="5a19b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a19b-118">-ResourceGroupName</span></span>
<span data-ttu-id="5a19b-119">Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="5a19b-119">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="5a19b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a19b-120">-SubscriptionId</span></span>
<span data-ttu-id="5a19b-121">Die Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="5a19b-121">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a19b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a19b-122">-Confirm</span></span>
<span data-ttu-id="5a19b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a19b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a19b-124">-WhatIf</span></span>
<span data-ttu-id="5a19b-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a19b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a19b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a19b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a19b-127">CommonParameters</span></span>
<span data-ttu-id="5a19b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a19b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a19b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a19b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a19b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a19b-130">INPUTS</span></span>

### <span data-ttu-id="5a19b-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="5a19b-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="5a19b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a19b-132">OUTPUTS</span></span>

### <span data-ttu-id="5a19b-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="5a19b-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="5a19b-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a19b-134">NOTES</span></span>

<span data-ttu-id="5a19b-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5a19b-135">ALIASES</span></span>

<span data-ttu-id="5a19b-136">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5a19b-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5a19b-137">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="5a19b-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5a19b-138">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5a19b-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5a19b-139">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="5a19b-139">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="5a19b-140">`Location <String>`: Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="5a19b-140">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="5a19b-141">`CloningInfoSourceWebAppId <String>`: ARM Ressourcen-ID der Quell-App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-141">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="5a19b-142">Die App-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} für Produktionsplätze und /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}.</span><span class="sxs-lookup"><span data-stu-id="5a19b-142">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="5a19b-143">`[Kind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a19b-143">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="5a19b-144">`[Tag <IResourceTags>]`: Ressourcentags.</span><span class="sxs-lookup"><span data-stu-id="5a19b-144">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5a19b-145">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a19b-145">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5a19b-146">`[ClientAffinityEnabled <Boolean?>]`: zum Aktivieren der Clientaffinität; zum Beenden des Sendens von Sitzungsaffinitätscookies, die Clientanforderungen in derselben Sitzung an <code>true</code> <code>false</code> dieselbe Instanz weiterrouten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="5a19b-147">Standard ist <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-147">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="5a19b-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> zum Aktivieren der Clientzertifikatauthentifizierung (TLS Mutual Authentication); andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="5a19b-149">Standard ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-149">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-150">`[ClientCertExclusionPath <String>]`: Durch Kommas getrennte Ausschlusspfade für Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="5a19b-150">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="5a19b-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Anwendungseinstellung außer Kraft für geklonte Apps.</span><span class="sxs-lookup"><span data-stu-id="5a19b-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="5a19b-152">Wenn angegeben, setzen diese Einstellungen die aus der Quell-App geklonten Einstellungen außer Kraft.</span><span class="sxs-lookup"><span data-stu-id="5a19b-152">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="5a19b-153">Andernfalls bleiben die Anwendungseinstellungen aus der Quell-App erhalten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-153">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="5a19b-154">`[(Any) <String>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a19b-154">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5a19b-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> zum Klonen von benutzerdefinierten Hostnamen aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> zum Klonen der Quellcodeverwaltung aus der Quell-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> so konfigurieren Sie den Lastenausgleich für die Quell- und Ziel-App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="5a19b-158">`[CloningInfoCorrelationId <String>]`: Korrelations-ID des Klonvorgangs.</span><span class="sxs-lookup"><span data-stu-id="5a19b-158">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="5a19b-159">Diese ID bindet mehrere Klonvorgänge zusammen, um dieselbe Momentaufnahme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-159">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="5a19b-160">`[CloningInfoHostingEnvironment <String>]`: App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-160">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="5a19b-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> zum Überschreiben der Ziel-App; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-162">`[CloningInfoSourceWebAppLocation <String>]`: Speicherort der Quell-App ex: West US oder North Europe</span><span class="sxs-lookup"><span data-stu-id="5a19b-162">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="5a19b-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM ressourcen-ID des Traffic Manager-Profils, das verwendet werden soll, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="5a19b-164">Die Traffic Manager-Ressourcen-ID ist das Formular /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="5a19b-164">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="5a19b-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name des zu erstellende Traffic Manager-Profils.</span><span class="sxs-lookup"><span data-stu-id="5a19b-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="5a19b-166">Dies ist nur erforderlich, wenn das Traffic Manager-Profil noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-166">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="5a19b-167">`[Config <ISiteConfig>]`: Konfiguration der App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-167">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="5a19b-168">`IsPushEnabled <Boolean>`: Ruft ein Kennzeichen ab oder legt fest, ob der Pushendpunkt aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-168">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="5a19b-169">`[ActionMinProcessExecutionTime <String>]`: Mindestzeit, die der Prozess ausführen muss, bevor die Aktion ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="5a19b-169">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="5a19b-170">`[ActionType <AutoHealActionType?>]`: Vordefinierte Aktion, die sie ergreifen soll.</span><span class="sxs-lookup"><span data-stu-id="5a19b-170">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="5a19b-171">`[AlwaysOn <Boolean?>]`: <code>true</code> wenn Immer ein aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-171">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-172">`[ApiDefinitionUrl <String>]`: Die URL der API-Definition.</span><span class="sxs-lookup"><span data-stu-id="5a19b-172">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="5a19b-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span><span class="sxs-lookup"><span data-stu-id="5a19b-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="5a19b-174">`[AppCommandLine <String>]`: Startbefehlzeile der App.</span><span class="sxs-lookup"><span data-stu-id="5a19b-174">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="5a19b-175">`[AppSetting <INameValuePair[]>]`: Anwendungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-175">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="5a19b-176">`[Name <String>]`: Name des Paares.</span><span class="sxs-lookup"><span data-stu-id="5a19b-176">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="5a19b-177">`[Value <String>]`: Koppelwert.</span><span class="sxs-lookup"><span data-stu-id="5a19b-177">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="5a19b-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> wenn Automatisches Verheilen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-179">`[AutoSwapSlotName <String>]`: Name des automatischen Tauschplatzes.</span><span class="sxs-lookup"><span data-stu-id="5a19b-179">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="5a19b-180">`[ConnectionString <IConnStringInfo[]>]`: Verbindungszeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-180">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="5a19b-181">`[ConnectionString <String>]`: Wert der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5a19b-181">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="5a19b-182">`[Name <String>]`: Name der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5a19b-182">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="5a19b-183">`[Type <ConnectionStringType?>]`: Datenbanktyp.</span><span class="sxs-lookup"><span data-stu-id="5a19b-183">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="5a19b-184">`[CorAllowedOrigin <String[]>]`: Ruft die Liste der Ursprünge ab, die originsübergreifende Aufrufe (z. B. dürfen) zulässig sein sollen, oder legt sie http://example.com:12345) fest.</span><span class="sxs-lookup"><span data-stu-id="5a19b-184">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="5a19b-185">Verwenden Sie "\*", um alle zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="5a19b-185">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="5a19b-186">`[CorSupportCredentials <Boolean?>]`: Ruft ab oder legt fest, ob CORS-Anforderungen mit Anmeldeinformationen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="5a19b-186">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="5a19b-187">Weitere         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         Details finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="5a19b-187">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="5a19b-188">`[CustomActionExe <String>]`: Ausführbare Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a19b-188">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="5a19b-189">`[CustomActionParameter <String>]`: Parameter für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="5a19b-189">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="5a19b-190">`[DefaultDocument <String[]>]`: Standarddokumente.</span><span class="sxs-lookup"><span data-stu-id="5a19b-190">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="5a19b-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> wenn die detaillierte Fehlerprotokollierung aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-192">`[DocumentRoot <String>]`: Dokumentstamm.</span><span class="sxs-lookup"><span data-stu-id="5a19b-192">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="5a19b-193">`[DynamicTagsJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste dynamischer Tags enthält, die aus Benutzeransprüchen im Pushregistrierungsendpunkt ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-193">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="5a19b-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: Liste der Anlaufregeln.</span><span class="sxs-lookup"><span data-stu-id="5a19b-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="5a19b-195">`[ActionHostName <String>]`: Hostname eines Slot, an den der Datenverkehr umgeleitet wird, wenn dies entschieden ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-195">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="5a19b-196">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5a19b-196">E.g.</span></span> <span data-ttu-id="5a19b-197">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="5a19b-197">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="5a19b-198">`[ChangeDecisionCallbackUrl <String>]`: Benutzerdefinierter Entscheidungsalgorithmus kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, deren URL angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a19b-198">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="5a19b-199">Informationen zum Gerüst und den Verträgen finden Sie unter TiPCallback-Websiteerweiterung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-199">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="5a19b-200"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="5a19b-200">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="5a19b-201">`[ChangeIntervalInMinute <Int32?>]`: Gibt das Intervall in Minuten an, um den Umleitungsprozentwert neu zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-201">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="5a19b-202">`[ChangeStep <Double?>]`: Im Szenario für automatisches Hochfahren ist dies der Schritt zum Hinzufügen/Entfernen von, bis <code>ReroutePercentage</code> \n oder <code>MinReroutePercentage</code> erreicht         <code>MaxReroutePercentage</code> wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-202">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="5a19b-203">Websitemetriken werden alle N Minuten überprüft, die im .\nCustom-Entscheidungsalgorithmus angegeben sind, kann in der TiPCallback-Websiteerweiterung bereitgestellt werden, in der <code>ChangeIntervalInMinutes</code> die URL angegeben werden <code>ChangeDecisionCallbackUrl</code> kann.</span><span class="sxs-lookup"><span data-stu-id="5a19b-203">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="5a19b-204">`[MaxReroutePercentage <Double?>]`: Gibt die obere Grenze an, unter der "Umleitungsprozent" bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="5a19b-204">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="5a19b-205">`[MinReroutePercentage <Double?>]`: Gibt die untere Grenze an, über der die Umleitungslinie bleiben soll.</span><span class="sxs-lookup"><span data-stu-id="5a19b-205">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="5a19b-206">`[Name <String>]`: Name der Routingregel.</span><span class="sxs-lookup"><span data-stu-id="5a19b-206">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="5a19b-207">Der empfohlene Name wäre, auf den Slot zu verweisen, der den Datenverkehr im Experiment erhält.</span><span class="sxs-lookup"><span data-stu-id="5a19b-207">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="5a19b-208">`[ReroutePercentage <Double?>]`: Prozentsatz des Datenverkehrs, der an umgeleitet <code>ActionHostName</code> wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-208">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="5a19b-209">`[FtpsState <FtpsState?>]`: Status des FTP/FTPS-Diensts</span><span class="sxs-lookup"><span data-stu-id="5a19b-209">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="5a19b-210">`[HandlerMapping <IHandlerMapping[]>]`: Handlerzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="5a19b-211">`[Argument <String>]`: Befehlszeilenargumente, die an den Skriptprozessor übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-211">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="5a19b-212">`[Extension <String>]`: Anforderungen mit dieser Erweiterung werden mit der angegebenen FastCGI-Anwendung behandelt.</span><span class="sxs-lookup"><span data-stu-id="5a19b-212">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="5a19b-213">`[ScriptProcessor <String>]`: Der absolute Pfad zur FastCGI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-213">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="5a19b-214">`[HealthCheckPath <String>]`: Integritätsprüfungspfad</span><span class="sxs-lookup"><span data-stu-id="5a19b-214">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="5a19b-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: Konfiguriert eine Website so, dass Clients eine Verbindung über http2.0 herstellen können</span><span class="sxs-lookup"><span data-stu-id="5a19b-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="5a19b-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> wenn die #A0 aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für Main.</span><span class="sxs-lookup"><span data-stu-id="5a19b-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="5a19b-218">`[Action <String>]`: Zulassen oder Verweigern des Zugriffs für diesen IP-Bereich.</span><span class="sxs-lookup"><span data-stu-id="5a19b-218">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="5a19b-219">`[Description <String>]`: Beschreibung der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="5a19b-219">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="5a19b-220">`[IPAddress <String>]`: IP-Adresse, für die die Sicherheitseinschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-220">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="5a19b-221">Sie kann in Form einer reinen ipv4-Adresse (erforderliche SubnetMask-Eigenschaft) oder cidr-Notation wie ipv4/mask (leading bit match) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-221">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="5a19b-222">Für CIDR darf keine Subnetzmask-Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-222">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="5a19b-223">`[Name <String>]`: Name der IP-Einschränkungsregel.</span><span class="sxs-lookup"><span data-stu-id="5a19b-223">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="5a19b-224">`[Priority <Int32?>]`: Priorität der Regel für DIE IP-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-224">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="5a19b-225">`[SubnetMask <String>]`: Subnetzformat für den Bereich der IP-Adressen, für den die Einschränkung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-225">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="5a19b-226">`[SubnetTrafficTag <Int32?>]`: (internes) Subnetzverkehrstag</span><span class="sxs-lookup"><span data-stu-id="5a19b-226">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="5a19b-227">`[Tag <IPFilterTag?>]`: Definiert, wofür dieser IP-Filter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-227">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="5a19b-228">Dies soll die IP-Filterung für Proxys unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-228">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="5a19b-229">`[VnetSubnetResourceId <String>]`: Virtuelle Netzwerkressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="5a19b-229">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="5a19b-230">`[VnetTrafficTag <Int32?>]`: (internes) Vnet-Verkehrstag</span><span class="sxs-lookup"><span data-stu-id="5a19b-230">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="5a19b-231">`[JavaContainer <String>]`: Java Container.</span><span class="sxs-lookup"><span data-stu-id="5a19b-231">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="5a19b-232">`[JavaContainerVersion <String>]`: Java Containerversion.</span><span class="sxs-lookup"><span data-stu-id="5a19b-232">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="5a19b-233">`[JavaVersion <String>]`: Java Version.</span><span class="sxs-lookup"><span data-stu-id="5a19b-233">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="5a19b-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal zulässige Datenträgergröße in MB.</span><span class="sxs-lookup"><span data-stu-id="5a19b-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="5a19b-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximal zulässige Speicherauslastung in MB.</span><span class="sxs-lookup"><span data-stu-id="5a19b-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="5a19b-236">`[LimitMaxPercentageCpu <Double?>]`: Maximal zulässiger Prozentsatz der CPU-Nutzung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-236">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="5a19b-237">`[LinuxFxVersion <String>]`: Linux App Framework und Version</span><span class="sxs-lookup"><span data-stu-id="5a19b-237">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="5a19b-238">`[LoadBalancing <SiteLoadBalancing?>]`: Lastenausgleich der Website.</span><span class="sxs-lookup"><span data-stu-id="5a19b-238">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="5a19b-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> um lokales MySQL zu aktivieren; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP protokolliert das Verzeichnisgrößenlimit.</span><span class="sxs-lookup"><span data-stu-id="5a19b-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="5a19b-241">`[MachineKeyDecryption <String>]`: Algorithmus, der für die Entschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-241">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="5a19b-242">`[MachineKeyDecryptionKey <String>]`: Entschlüsselungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5a19b-242">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="5a19b-243">`[MachineKeyValidation <String>]`: MachineKey-Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-243">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="5a19b-244">`[MachineKeyValidationKey <String>]`: Überprüfungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5a19b-244">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="5a19b-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Verwalteter Pipelinemodus.</span><span class="sxs-lookup"><span data-stu-id="5a19b-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="5a19b-246">`[ManagedServiceIdentityId <Int32?>]`: Id für verwaltete Dienstidentität</span><span class="sxs-lookup"><span data-stu-id="5a19b-246">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="5a19b-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: Konfiguriert die für SSL-Anforderungen erforderliche Mindestversion von TLS</span><span class="sxs-lookup"><span data-stu-id="5a19b-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="5a19b-248">`[NetFrameworkVersion <String>]`: .NET Framework Version.</span><span class="sxs-lookup"><span data-stu-id="5a19b-248">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="5a19b-249">`[NodeVersion <String>]`: Version von Node.js.</span><span class="sxs-lookup"><span data-stu-id="5a19b-249">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="5a19b-250">`[NumberOfWorker <Int32?>]`: Anzahl der Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="5a19b-250">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="5a19b-251">`[PhpVersion <String>]`: Version von PHP.</span><span class="sxs-lookup"><span data-stu-id="5a19b-251">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="5a19b-252">`[PowerShellVersion <String>]`: Version von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5a19b-252">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="5a19b-253">`[PreWarmedInstanceCount <Int32?>]`: Anzahl der vordefinierten Instanzen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-253">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="5a19b-254">Diese Einstellung gilt nur für die Pläne "Verbrauch" und "Flexible Pläne".</span><span class="sxs-lookup"><span data-stu-id="5a19b-254">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="5a19b-255">`[PublishingUsername <String>]`: Veröffentlichen des Benutzernamens.</span><span class="sxs-lookup"><span data-stu-id="5a19b-255">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="5a19b-256">`[PushKind <String>]`: Art der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a19b-256">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="5a19b-257">`[PythonVersion <String>]`: Version von Python.</span><span class="sxs-lookup"><span data-stu-id="5a19b-257">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="5a19b-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> wenn das Remotedebuding aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-259">`[RemoteDebuggingVersion <String>]`: Remotedebugversion.</span><span class="sxs-lookup"><span data-stu-id="5a19b-259">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="5a19b-260">`[RequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a19b-260">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="5a19b-261">`[RequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="5a19b-261">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="5a19b-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> wenn die Anforderungsablaufverfolgung aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-263">`[RequestTracingExpirationTime <DateTime?>]`: Ablaufzeit der Ablaufverfolgung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a19b-263">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="5a19b-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-Sicherheitseinschränkungen für scm.</span><span class="sxs-lookup"><span data-stu-id="5a19b-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="5a19b-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-Sicherheitseinschränkungen für scm für die Verwendung von Main.</span><span class="sxs-lookup"><span data-stu-id="5a19b-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="5a19b-266">`[ScmType <ScmType?>]`: SCM-Typ.</span><span class="sxs-lookup"><span data-stu-id="5a19b-266">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="5a19b-267">`[SlowRequestCount <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a19b-267">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="5a19b-268">`[SlowRequestTimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="5a19b-268">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="5a19b-269">`[SlowRequestTimeTaken <String>]`: Zeit, die sie sich genommen hat.</span><span class="sxs-lookup"><span data-stu-id="5a19b-269">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="5a19b-270">`[TagWhitelistJson <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, die auf der Whitelist für die Verwendung durch den Pushregistrierungsendpunkt stehen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-270">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="5a19b-271">`[TagsRequiringAuth <String>]`: Ruft eine JSON-Zeichenfolge ab oder legt sie fest, die eine Liste der Tags enthält, für die die Benutzerauthentifizierung im Pushregistrierungsendpunkt verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="5a19b-271">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="5a19b-272">Tags können aus alphanumerischen Zeichen und den folgenden Zeichen bestehen: '_', '@', '#', '.', ':', '-'.</span><span class="sxs-lookup"><span data-stu-id="5a19b-272">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="5a19b-273">Die Überprüfung sollte im PushRequestHandler ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-273">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="5a19b-274">`[TracingOption <String>]`: Ablaufverfolgungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-274">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="5a19b-275">`[TriggerPrivateBytesInKb <Int32?>]`: Eine Regel, die auf privaten Bytes basiert.</span><span class="sxs-lookup"><span data-stu-id="5a19b-275">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="5a19b-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: Eine Regel, die auf Statuscodes basiert.</span><span class="sxs-lookup"><span data-stu-id="5a19b-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="5a19b-277">`[Count <Int32?>]`: Anzahl anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a19b-277">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="5a19b-278">`[Status <Int32?>]`: HTTP-Statuscode.</span><span class="sxs-lookup"><span data-stu-id="5a19b-278">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="5a19b-279">`[SubStatus <Int32?>]`: Unterstatus anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a19b-279">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="5a19b-280">`[TimeInterval <String>]`: Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="5a19b-280">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="5a19b-281">`[Win32Status <Int32?>]`: Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="5a19b-281">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="5a19b-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> zum Verwenden des 32-Bit-Workerprozesses; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="5a19b-284">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="5a19b-284">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="5a19b-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> wenn das Vorabladen aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="5a19b-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuelle Verzeichnisse für virtuelle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5a19b-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="5a19b-287">`[PhysicalPath <String>]`: Physischer Pfad.</span><span class="sxs-lookup"><span data-stu-id="5a19b-287">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="5a19b-288">`[VirtualPath <String>]`: Pfad zur virtuellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-288">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="5a19b-289">`[VirtualPath <String>]`: Virtueller Pfad.</span><span class="sxs-lookup"><span data-stu-id="5a19b-289">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="5a19b-290">`[VnetName <String>]`: Name des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5a19b-290">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="5a19b-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> wenn WebSocket aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5a19b-292">`[WindowsFxVersion <String>]`: Xenon App Framework und Version</span><span class="sxs-lookup"><span data-stu-id="5a19b-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="5a19b-293">`[XManagedServiceIdentityId <Int32?>]`: Explizite Identitäts-ID für verwaltete Dienste</span><span class="sxs-lookup"><span data-stu-id="5a19b-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="5a19b-294">`[ContainerSize <Int32?>]`: Größe des Funktionscontainers.</span><span class="sxs-lookup"><span data-stu-id="5a19b-294">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="5a19b-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximal zulässiges tägliches Speicher-Zeitkontingent (gilt nur für dynamische Apps).</span><span class="sxs-lookup"><span data-stu-id="5a19b-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="5a19b-296">`[Enabled <Boolean?>]`: <code>true</code> wenn die App aktiviert ist; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-296">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="5a19b-297">Wenn Sie diesen Wert auf false festlegen, wird die App deaktiviert (die App wird offline geschaltet).</span><span class="sxs-lookup"><span data-stu-id="5a19b-297">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="5a19b-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-Zustände werden verwendet, um die SSL-Bindungen für die Hostnamen der App zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="5a19b-299">`[HostType <HostType?>]`: Gibt an, ob der Hostname ein Standard- oder Repositoryhostname ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-299">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="5a19b-300">`[Name <String>]`: Hostname.</span><span class="sxs-lookup"><span data-stu-id="5a19b-300">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="5a19b-301">`[SslState <SslState?>]`: SSL-Typ.</span><span class="sxs-lookup"><span data-stu-id="5a19b-301">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="5a19b-302">`[Thumbprint <String>]`: Fingerabdruck des SSL-Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="5a19b-302">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="5a19b-303">`[ToUpdate <Boolean?>]`: So wird <code>true</code> festgelegt, dass der vorhandene Hostname aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5a19b-303">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="5a19b-304">`[VirtualIP <String>]`: Virtuelle IP-Adresse, die dem Hostnamen zugewiesen ist, wenn IP-basiertes SSL aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5a19b-304">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="5a19b-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> um die öffentlichen Hostnamen der App zu deaktivieren; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="5a19b-306">Wenn <code>true</code> , kann auf die App nur über den API-Verwaltungsvorgang zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-306">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="5a19b-307">`[HostingEnvironmentProfileId <String>]`: Ressourcen-ID der App-Dienstumgebung.</span><span class="sxs-lookup"><span data-stu-id="5a19b-307">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="5a19b-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfiguriert eine Website so, dass nur https-Anforderungen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a19b-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="5a19b-309">Umleitung von Problemen bei Http-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a19b-309">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="5a19b-310">`[HyperV <Boolean?>]`: Hyper-V-Sandkasten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-310">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="5a19b-311">`[IdentityType <ManagedServiceIdentityType?>]`: Typ der verwalteten Dienstidentität.</span><span class="sxs-lookup"><span data-stu-id="5a19b-311">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="5a19b-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Die Liste der benutzer zugewiesenen Identitäten, die der Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5a19b-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="5a19b-313">Die Schlüsselverweise für benutzeridentitätswörterbücher werden ARM Ressourcen-ID im Formular angezeigt: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="5a19b-313">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="5a19b-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Dies gibt an, dass diesem Objekt eine beliebige Eigenschaft hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a19b-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5a19b-315">`[IsXenon <Boolean?>]`: Veraltet: Hyper-V-Sandkasten.</span><span class="sxs-lookup"><span data-stu-id="5a19b-315">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="5a19b-316">`[RedundancyMode <RedundancyMode?>]`: Websiteredundanzmodus</span><span class="sxs-lookup"><span data-stu-id="5a19b-316">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="5a19b-317">`[Reserved <Boolean?>]`: <code>true</code> falls reserviert; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-317">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> um die #A0 (KUDU) zu beenden, wenn die App beendet wird; andernfalls <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="5a19b-319">Die Standardeinstellung ist <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5a19b-319">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="5a19b-320">`[ServerFarmId <String>]`: Ressourcen-ID des zugeordneten App Service-Plans, formatiert als: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="5a19b-320">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="5a19b-321">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a19b-321">RELATED LINKS</span></span>

