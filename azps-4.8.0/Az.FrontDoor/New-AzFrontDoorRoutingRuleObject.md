---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173776"
---
# <span data-ttu-id="86a13-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="86a13-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="86a13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86a13-102">SYNOPSIS</span></span>
<span data-ttu-id="86a13-103">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="86a13-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="86a13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86a13-104">SYNTAX</span></span>

### <span data-ttu-id="86a13-105">ByFieldsWithForwardingParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="86a13-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86a13-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86a13-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a13-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86a13-107">DESCRIPTION</span></span>
<span data-ttu-id="86a13-108">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="86a13-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="86a13-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86a13-109">EXAMPLES</span></span>

### <span data-ttu-id="86a13-110">Beispiel 1: Erstellen einer PSRoutingRuleObject für die Erstellung von Haustüren mit einer Weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="86a13-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="86a13-111">Beispiel 2: Erstellen einer PSRoutingRuleObject für die Erstellung von Haustüren mit einer Umleitungsregel</span><span class="sxs-lookup"><span data-stu-id="86a13-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

<span data-ttu-id="86a13-112">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="86a13-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="86a13-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="86a13-113">PARAMETERS</span></span>

### <span data-ttu-id="86a13-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="86a13-114">-AcceptedProtocol</span></span>
<span data-ttu-id="86a13-115">Protokollschemas, die für diese Regel übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="86a13-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="86a13-116">Der Standardwert ist {HTTPS; http}</span><span class="sxs-lookup"><span data-stu-id="86a13-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="86a13-117">-BackendPoolName</span></span>
<span data-ttu-id="86a13-118">Die Ressourcen-ID des BackendPool, zu dem diese Regel weitergeleitet wird</span><span class="sxs-lookup"><span data-stu-id="86a13-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="86a13-119">-CustomForwardingPath</span></span>
<span data-ttu-id="86a13-120">Der benutzerdefinierte Pfad, der zum Umschreiben von Ressourcenpfaden verwendet wird, die dieser Regel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="86a13-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="86a13-121">Leer lassen, um den eingehenden Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="86a13-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="86a13-122">-CustomFragment</span></span>
<span data-ttu-id="86a13-123">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86a13-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="86a13-124">Fragment ist der Teil der URL, der hinter # steht.</span><span class="sxs-lookup"><span data-stu-id="86a13-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="86a13-125">Schließen Sie nicht das # ein.</span><span class="sxs-lookup"><span data-stu-id="86a13-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="86a13-126">-CustomHost</span></span>
<span data-ttu-id="86a13-127">Host zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="86a13-127">Host to redirect.</span></span> <span data-ttu-id="86a13-128">Leer lassen, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="86a13-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="86a13-129">-CustomPath</span></span>
<span data-ttu-id="86a13-130">Der vollständige Pfad zum umleiten.</span><span class="sxs-lookup"><span data-stu-id="86a13-130">The full path to redirect.</span></span> <span data-ttu-id="86a13-131">Path darf nicht leer sein und muss mit/beginnen.</span><span class="sxs-lookup"><span data-stu-id="86a13-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="86a13-132">Leer lassen, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="86a13-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="86a13-133">-CustomQueryString</span></span>
<span data-ttu-id="86a13-134">Der Satz von Abfragezeichenfolgen, der in die Redirect-URL gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86a13-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="86a13-135">Wenn Sie diesen Wert festlegen, wird jede vorhandene Abfragezeichenfolge ersetzt. leer lassen, um die eingehende Abfragezeichenfolge beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="86a13-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="86a13-136">Abfragezeichenfolge muss in sein <key>=</span><span class="sxs-lookup"><span data-stu-id="86a13-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="86a13-137">Format.</span><span class="sxs-lookup"><span data-stu-id="86a13-137">format.</span></span> <span data-ttu-id="86a13-138">Der erste?</span><span class="sxs-lookup"><span data-stu-id="86a13-138">The first ?</span></span> <span data-ttu-id="86a13-139">und & werden automatisch hinzugefügt, sodass Sie nicht im Vordergrund enthalten sind, sondern mehrere Abfragezeichenfolgen mit & getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="86a13-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a13-140">-DefaultProfile</span></span>
<span data-ttu-id="86a13-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86a13-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="86a13-142">-DynamicCompression</span></span>
<span data-ttu-id="86a13-143">Ob die dynamische Komprimierung für zwischengespeicherte Inhalte aktiviert werden soll, wenn die Zwischenspeicherung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="86a13-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="86a13-144">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="86a13-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="86a13-145">-EnableCaching</span></span>
<span data-ttu-id="86a13-146">Gibt an, ob die Zwischenspeicherung für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86a13-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="86a13-147">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="86a13-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="86a13-148">-EnabledState</span></span>
<span data-ttu-id="86a13-149">Gibt an, ob die Verwendung dieser Regel aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86a13-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="86a13-150">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="86a13-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="86a13-151">-ForwardingProtocol</span></span>
<span data-ttu-id="86a13-152">Das Protokoll, das diese Regel bei der Weiterleitung des Datenverkehrs an den Backends verwendet, ist der Standardwert MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="86a13-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="86a13-153">-FrontDoorName</span></span>
<span data-ttu-id="86a13-154">Der Name der Haustür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="86a13-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="86a13-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="86a13-155">-FrontendEndpointName</span></span>
<span data-ttu-id="86a13-156">Die Namen der Frontend-Endpunkte, die dieser Regel zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="86a13-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="86a13-157">-Name</span><span class="sxs-lookup"><span data-stu-id="86a13-157">-Name</span></span>
<span data-ttu-id="86a13-158">RoutingRule-Name.</span><span class="sxs-lookup"><span data-stu-id="86a13-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="86a13-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="86a13-159">-PatternToMatch</span></span>
<span data-ttu-id="86a13-160">Die Routenmuster der Regel dürfen keine \* außer möglicherweise nach dem letzten/am Ende des Pfads enthalten.</span><span class="sxs-lookup"><span data-stu-id="86a13-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="86a13-161">Standardwert ist/\*</span><span class="sxs-lookup"><span data-stu-id="86a13-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="86a13-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="86a13-163">Die Behandlung von URL-Abfrageausdrücken beim bilden des Cacheschlüssels</span><span class="sxs-lookup"><span data-stu-id="86a13-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="86a13-164">Der Standardwert ist StripAll</span><span class="sxs-lookup"><span data-stu-id="86a13-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="86a13-165">-RedirectProtocol</span></span>
<span data-ttu-id="86a13-166">Das Protokoll des Ziels an die Stelle, an der der Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="86a13-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="86a13-167">Der Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="86a13-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-168">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="86a13-168">-RedirectType</span></span>
<span data-ttu-id="86a13-169">Der Redirect-Typ, der von der Regel beim Umleiten von Datenverkehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86a13-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="86a13-170">Standardwert wird verschoben</span><span class="sxs-lookup"><span data-stu-id="86a13-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a13-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a13-171">-ResourceGroupName</span></span>
<span data-ttu-id="86a13-172">Der Ressourcengruppenname, in dem der RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="86a13-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="86a13-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="86a13-173">-RulesEngineName</span></span>
<span data-ttu-id="86a13-174">Ein Verweis auf eine bestimmte Regelmodul Konfiguration, die auf diese Route angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86a13-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="86a13-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a13-175">CommonParameters</span></span>
<span data-ttu-id="86a13-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a13-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a13-177">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86a13-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a13-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86a13-178">INPUTS</span></span>

### <span data-ttu-id="86a13-179">Keine</span><span class="sxs-lookup"><span data-stu-id="86a13-179">None</span></span>

## <span data-ttu-id="86a13-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86a13-180">OUTPUTS</span></span>

### <span data-ttu-id="86a13-181">Microsoft. Azure. Commands. Haustür. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="86a13-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="86a13-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="86a13-182">NOTES</span></span>

## <span data-ttu-id="86a13-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86a13-183">RELATED LINKS</span></span>

<span data-ttu-id="86a13-184">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="86a13-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
