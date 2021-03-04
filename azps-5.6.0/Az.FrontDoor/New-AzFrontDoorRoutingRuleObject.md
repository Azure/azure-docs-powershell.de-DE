---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3d66db0baeca0e371800c4544f2f0360c448b108
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928107"
---
# <span data-ttu-id="40f07-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="40f07-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="40f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f07-102">SYNOPSIS</span></span>
<span data-ttu-id="40f07-103">Erstellen eines PSRoutingRuleObjects für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="40f07-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="40f07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40f07-104">SYNTAX</span></span>

### <span data-ttu-id="40f07-105">ByFieldsWithForwardingParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="40f07-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40f07-106">ByFieldsWithRedirectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40f07-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40f07-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40f07-107">DESCRIPTION</span></span>
<span data-ttu-id="40f07-108">Erstellen eines PSRoutingRuleObjects für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="40f07-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="40f07-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40f07-109">EXAMPLES</span></span>

### <span data-ttu-id="40f07-110">Beispiel 1: Erstellen eines PSRoutingRuleObjects für die Erstellung von Vordertüren mit einer Weiterleitungsregel</span><span class="sxs-lookup"><span data-stu-id="40f07-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
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

### <span data-ttu-id="40f07-111">Beispiel 2: Erstellen eines PSRoutingRuleObjects für die Erstellung von Vordertüren mit einer Umleitungsregel</span><span class="sxs-lookup"><span data-stu-id="40f07-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
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

<span data-ttu-id="40f07-112">Erstellen eines PSRoutingRuleObjects für die Erstellung von Vordertüren</span><span class="sxs-lookup"><span data-stu-id="40f07-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="40f07-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40f07-113">PARAMETERS</span></span>

### <span data-ttu-id="40f07-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="40f07-114">-AcceptedProtocol</span></span>
<span data-ttu-id="40f07-115">Protokollschemas, die mit dieser Regel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="40f07-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="40f07-116">Standardwert ist {Https, Http}</span><span class="sxs-lookup"><span data-stu-id="40f07-116">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="40f07-117">-Back-EndPoolName</span><span class="sxs-lookup"><span data-stu-id="40f07-117">-BackendPoolName</span></span>
<span data-ttu-id="40f07-118">Ressourcen-ID des Back-EndPools, zu dem diese Regel</span><span class="sxs-lookup"><span data-stu-id="40f07-118">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="40f07-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="40f07-119">-CustomForwardingPath</span></span>
<span data-ttu-id="40f07-120">Der benutzerdefinierte Pfad zum Neuschreiben von Ressourcenpfaden, der mit dieser Regel übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="40f07-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="40f07-121">Lassen Sie leer, um den posteingangspfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="40f07-121">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="40f07-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="40f07-122">-CustomFragment</span></span>
<span data-ttu-id="40f07-123">Fragment, das der Umleitungs-URL hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f07-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="40f07-124">Fragment ist der Teil der URL, der nach #kommt.</span><span class="sxs-lookup"><span data-stu-id="40f07-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="40f07-125">Schließen Sie das -Zeichen #nicht ein.</span><span class="sxs-lookup"><span data-stu-id="40f07-125">Do not include the #.</span></span>

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

### <span data-ttu-id="40f07-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="40f07-126">-CustomHost</span></span>
<span data-ttu-id="40f07-127">Host zum Umleiten.</span><span class="sxs-lookup"><span data-stu-id="40f07-127">Host to redirect.</span></span> <span data-ttu-id="40f07-128">Lassen Sie leer, um den eingehenden Host als Zielhost zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="40f07-128">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="40f07-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="40f07-129">-CustomPath</span></span>
<span data-ttu-id="40f07-130">Der vollständige Umleitungspfad.</span><span class="sxs-lookup"><span data-stu-id="40f07-130">The full path to redirect.</span></span> <span data-ttu-id="40f07-131">Pfad darf nicht leer sein und muss mit /beginnen.</span><span class="sxs-lookup"><span data-stu-id="40f07-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="40f07-132">Lassen Sie leer, um den eingehenden Pfad als Zielpfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="40f07-132">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="40f07-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="40f07-133">-CustomQueryString</span></span>
<span data-ttu-id="40f07-134">Die Gruppe der Abfragezeichenfolgen, die in der Umleitungs-URL platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="40f07-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="40f07-135">Durch Festlegen dieses Werts wird jede vorhandene Abfragezeichenfolge ersetzt. lassen Sie leer, um die eingehende Abfragezeichenfolge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="40f07-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="40f07-136">Abfragezeichenfolge muss in <key>=</span><span class="sxs-lookup"><span data-stu-id="40f07-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="40f07-137">formatieren.</span><span class="sxs-lookup"><span data-stu-id="40f07-137">format.</span></span> <span data-ttu-id="40f07-138">Das erste ?</span><span class="sxs-lookup"><span data-stu-id="40f07-138">The first ?</span></span> <span data-ttu-id="40f07-139">und & werden automatisch hinzugefügt, sodass Sie sie nicht in den Vordermann nehmen, sondern mehrere Abfragezeichenfolgen durch &.</span><span class="sxs-lookup"><span data-stu-id="40f07-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="40f07-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f07-140">-DefaultProfile</span></span>
<span data-ttu-id="40f07-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f07-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f07-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="40f07-142">-DynamicCompression</span></span>
<span data-ttu-id="40f07-143">Gibt an, ob die dynamische Komprimierung für zwischengespeicherte Inhalte aktiviert werden soll, wenn das Zwischenspeichern aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="40f07-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="40f07-144">Standardwert ist Aktiviert</span><span class="sxs-lookup"><span data-stu-id="40f07-144">Default value is Enabled</span></span>

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

### <span data-ttu-id="40f07-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="40f07-145">-EnableCaching</span></span>
<span data-ttu-id="40f07-146">Gibt an, ob die Zwischenspeicherung für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f07-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="40f07-147">Standardwert ist falsch</span><span class="sxs-lookup"><span data-stu-id="40f07-147">Default value is false</span></span>

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

### <span data-ttu-id="40f07-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="40f07-148">-EnabledState</span></span>
<span data-ttu-id="40f07-149">Gibt an, ob die Verwendung dieser Regel aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f07-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="40f07-150">Standardwert ist Aktiviert</span><span class="sxs-lookup"><span data-stu-id="40f07-150">Default value is Enabled</span></span>

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

### <span data-ttu-id="40f07-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="40f07-151">-ForwardingProtocol</span></span>
<span data-ttu-id="40f07-152">Das Protokoll, das diese Regel verwendet, wenn Datenverkehr an Back-End-Enden weitergeleitet wird Standardwert ist MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="40f07-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

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

### <span data-ttu-id="40f07-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="40f07-153">-FrontDoorName</span></span>
<span data-ttu-id="40f07-154">Der Name der Eingangstür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="40f07-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="40f07-155">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="40f07-155">-FrontendEndpointName</span></span>
<span data-ttu-id="40f07-156">Die Namen der dieser Regel zugeordneten Frontend-Endpunkte</span><span class="sxs-lookup"><span data-stu-id="40f07-156">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="40f07-157">-Name</span><span class="sxs-lookup"><span data-stu-id="40f07-157">-Name</span></span>
<span data-ttu-id="40f07-158">RoutingRule-Name.</span><span class="sxs-lookup"><span data-stu-id="40f07-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="40f07-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="40f07-159">-PatternToMatch</span></span>
<span data-ttu-id="40f07-160">Die Routenmuster der Regel dürfen keine \* haben, außer möglicherweise nach dem endgültigen /am Ende des Pfads.</span><span class="sxs-lookup"><span data-stu-id="40f07-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="40f07-161">Der Standardwert ist /\*</span><span class="sxs-lookup"><span data-stu-id="40f07-161">Default value is /\*</span></span>

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

### <span data-ttu-id="40f07-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="40f07-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="40f07-163">Die Behandlung von URL-Abfragebegriffen beim Erstellen des Cacheschlüssels.</span><span class="sxs-lookup"><span data-stu-id="40f07-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="40f07-164">Standardwert ist StripAll</span><span class="sxs-lookup"><span data-stu-id="40f07-164">Default value is StripAll</span></span>

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

### <span data-ttu-id="40f07-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="40f07-165">-RedirectProtocol</span></span>
<span data-ttu-id="40f07-166">Das Protokoll des Ziels, an das der Datenverkehr umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="40f07-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="40f07-167">Standardwert ist MatchRequest</span><span class="sxs-lookup"><span data-stu-id="40f07-167">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="40f07-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="40f07-168">-RedirectType</span></span>
<span data-ttu-id="40f07-169">Der Umleitungstyp, den die Regel beim Umleiten von Datenverkehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="40f07-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="40f07-170">Standardwert wird verschoben</span><span class="sxs-lookup"><span data-stu-id="40f07-170">Default Value is Moved</span></span>

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

### <span data-ttu-id="40f07-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f07-171">-ResourceGroupName</span></span>
<span data-ttu-id="40f07-172">Der Ressourcengruppenname, in dem die RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40f07-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="40f07-173">-RulesEngineName</span><span class="sxs-lookup"><span data-stu-id="40f07-173">-RulesEngineName</span></span>
<span data-ttu-id="40f07-174">Ein Verweis auf eine bestimmte Regelmodulkonfiguration, die auf diese Route angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f07-174">A reference to a specific Rules Engine Configuration to apply to this route.</span></span>

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

### <span data-ttu-id="40f07-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f07-175">CommonParameters</span></span>
<span data-ttu-id="40f07-176">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40f07-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f07-177">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40f07-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f07-178">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40f07-178">INPUTS</span></span>

### <span data-ttu-id="40f07-179">Keine</span><span class="sxs-lookup"><span data-stu-id="40f07-179">None</span></span>

## <span data-ttu-id="40f07-180">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40f07-180">OUTPUTS</span></span>

### <span data-ttu-id="40f07-181">Microsoft.Azure.Commands.Frontdoor.Models.PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="40f07-181">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="40f07-182">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40f07-182">NOTES</span></span>

## <span data-ttu-id="40f07-183">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40f07-183">RELATED LINKS</span></span>

<span data-ttu-id="40f07-184">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="40f07-184">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
