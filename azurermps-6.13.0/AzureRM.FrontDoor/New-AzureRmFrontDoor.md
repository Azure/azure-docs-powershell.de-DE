---
<span data-ttu-id="49a9a-101">externe Hilfedatei: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Modul Name: AzureRM. Haustür Online-Version: die entsprechende URL sollte wie folgt lauten: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor Schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="49a9a-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="49a9a-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="49a9a-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="49a9a-103">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49a9a-103">SYNOPSIS</span></span>
<span data-ttu-id="49a9a-104">Erstellen eines neuen Azure Front Door Load Balancer</span><span class="sxs-lookup"><span data-stu-id="49a9a-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="49a9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a9a-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="49a9a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49a9a-106">DESCRIPTION</span></span>
<span data-ttu-id="49a9a-107">Das Cmdlet **New-AzureRmFrontDoor** erstellt ein neues Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter Aktuelles Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49a9a-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="49a9a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49a9a-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="49a9a-109">Beispiel 1: Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="49a9a-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="49a9a-110">Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="49a9a-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="49a9a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="49a9a-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="49a9a-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="49a9a-112">-BackendPool</span></span>
<span data-ttu-id="49a9a-113">Backendpools ist für Routingregel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="49a9a-113">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-defaultprofile"></a><span data-ttu-id="49a9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a9a-114">-DefaultProfile</span></span>
<span data-ttu-id="49a9a-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49a9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="49a9a-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="49a9a-116">-EnabledState</span></span>
<span data-ttu-id="49a9a-117">EnabledState des Front Door Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="49a9a-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="49a9a-118">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="49a9a-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="49a9a-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="49a9a-119">-FrontendEndpoint</span></span>
<span data-ttu-id="49a9a-120">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="49a9a-120">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-healthprobesetting"></a><span data-ttu-id="49a9a-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="49a9a-121">-HealthProbeSetting</span></span>
<span data-ttu-id="49a9a-122">Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="49a9a-122">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-loadbalancingsetting"></a><span data-ttu-id="49a9a-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="49a9a-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="49a9a-124">Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="49a9a-124">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-name"></a><span data-ttu-id="49a9a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="49a9a-125">-Name</span></span>
<span data-ttu-id="49a9a-126">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="49a9a-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="49a9a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a9a-127">-ResourceGroupName</span></span>
<span data-ttu-id="49a9a-128">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="49a9a-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="49a9a-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="49a9a-129">-RoutingRule</span></span>
<span data-ttu-id="49a9a-130">Diesem Haustür zugeordnete Routing Regeln</span><span class="sxs-lookup"><span data-stu-id="49a9a-130">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-tag"></a><span data-ttu-id="49a9a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="49a9a-131">-Tag</span></span>
<span data-ttu-id="49a9a-132">Die Tags werden dem Haustür zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="49a9a-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="49a9a-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49a9a-133">-Confirm</span></span>
<span data-ttu-id="49a9a-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49a9a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="49a9a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a9a-135">-WhatIf</span></span>
<span data-ttu-id="49a9a-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49a9a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a9a-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49a9a-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="49a9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a9a-138">CommonParameters</span></span>
<span data-ttu-id="49a9a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a9a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a9a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="49a9a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49a9a-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="49a9a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="49a9a-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="49a9a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49a9a-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="49a9a-144">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="49a9a-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="49a9a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="49a9a-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="49a9a-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49a9a-146">RELATED LINKS</span></span>

<span data-ttu-id="49a9a-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Neu – AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Neu – AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Neu – AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Neu – AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="49a9a-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
