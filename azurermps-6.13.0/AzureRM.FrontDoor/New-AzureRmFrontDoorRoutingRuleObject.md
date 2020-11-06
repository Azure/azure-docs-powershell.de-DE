---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499498"
---
# <span data-ttu-id="e5cc2-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="e5cc2-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="e5cc2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e5cc2-103">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="e5cc2-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5cc2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5cc2-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5cc2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e5cc2-106">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="e5cc2-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="e5cc2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="e5cc2-108">Beispiel 1: Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="e5cc2-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="e5cc2-109">Erstellen einer PSRoutingRuleObject für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="e5cc2-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="e5cc2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5cc2-110">PARAMETERS</span></span>

### <span data-ttu-id="e5cc2-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="e5cc2-111">-AcceptedProtocol</span></span>
<span data-ttu-id="e5cc2-112">Protokollschemas, die für diese Regel übereinstimmen sollen.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="e5cc2-113">Der Standardwert ist {HTTPS; http}</span><span class="sxs-lookup"><span data-stu-id="e5cc2-113">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="e5cc2-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="e5cc2-114">-BackendPoolName</span></span>
<span data-ttu-id="e5cc2-115">Die Ressourcen-ID des BackendPool, zu dem diese Regel weitergeleitet wird</span><span class="sxs-lookup"><span data-stu-id="e5cc2-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="e5cc2-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="e5cc2-116">-CustomForwardingPath</span></span>
<span data-ttu-id="e5cc2-117">Der benutzerdefinierte Pfad, der zum Umschreiben von Ressourcenpfaden verwendet wird, die dieser Regel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="e5cc2-118">Leer lassen, um den eingehenden Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="e5cc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5cc2-119">-DefaultProfile</span></span>
<span data-ttu-id="e5cc2-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5cc2-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="e5cc2-121">-DynamicCompression</span></span>
<span data-ttu-id="e5cc2-122">Ob die dynamische Komprimierung für zwischengespeicherte Inhalte aktiviert werden soll, wenn die Zwischenspeicherung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="e5cc2-123">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="e5cc2-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="e5cc2-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="e5cc2-124">-EnableCaching</span></span>
<span data-ttu-id="e5cc2-125">Gibt an, ob die Zwischenspeicherung für diese Route aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="e5cc2-126">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="e5cc2-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5cc2-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e5cc2-127">-EnabledState</span></span>
<span data-ttu-id="e5cc2-128">Gibt an, ob die Verwendung dieser Regel aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="e5cc2-129">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="e5cc2-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="e5cc2-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="e5cc2-130">-ForwardingProtocol</span></span>
<span data-ttu-id="e5cc2-131">Das Protokoll, das diese Regel bei der Weiterleitung des Datenverkehrs an den Backends verwendet, ist der Standardwert MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5cc2-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e5cc2-132">-FrontDoorName</span></span>
<span data-ttu-id="e5cc2-133">Der Name der Haustür, zu der diese Routingregel gehört.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e5cc2-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="e5cc2-134">-FrontendEndpointName</span></span>
<span data-ttu-id="e5cc2-135">Die Namen der Frontend-Endpunkte, die dieser Regel zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="e5cc2-135">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="e5cc2-136">-Name</span><span class="sxs-lookup"><span data-stu-id="e5cc2-136">-Name</span></span>
<span data-ttu-id="e5cc2-137">RoutingRule-Name.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="e5cc2-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="e5cc2-138">-PatternToMatch</span></span>
<span data-ttu-id="e5cc2-139">Die Routenmuster der Regel dürfen keine \* außer möglicherweise nach dem letzten/am Ende des Pfads enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="e5cc2-140">Standardwert ist/\*</span><span class="sxs-lookup"><span data-stu-id="e5cc2-140">Default value is /\*</span></span>

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

### <span data-ttu-id="e5cc2-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="e5cc2-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="e5cc2-142">Die Behandlung von URL-Abfrageausdrücken beim bilden des Cacheschlüssels</span><span class="sxs-lookup"><span data-stu-id="e5cc2-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="e5cc2-143">Der Standardwert ist StripAll</span><span class="sxs-lookup"><span data-stu-id="e5cc2-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5cc2-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5cc2-144">-ResourceGroupName</span></span>
<span data-ttu-id="e5cc2-145">Der Ressourcengruppenname, in dem der RoutingRule erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e5cc2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5cc2-146">CommonParameters</span></span>
<span data-ttu-id="e5cc2-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5cc2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5cc2-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5cc2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5cc2-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5cc2-149">INPUTS</span></span>

### <span data-ttu-id="e5cc2-150">Keine</span><span class="sxs-lookup"><span data-stu-id="e5cc2-150">None</span></span>

## <span data-ttu-id="e5cc2-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5cc2-151">OUTPUTS</span></span>

### <span data-ttu-id="e5cc2-152">Microsoft. Azure. Commands. Haustür. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e5cc2-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="e5cc2-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5cc2-153">NOTES</span></span>

## <span data-ttu-id="e5cc2-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5cc2-154">RELATED LINKS</span></span>

<span data-ttu-id="e5cc2-155">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e5cc2-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
