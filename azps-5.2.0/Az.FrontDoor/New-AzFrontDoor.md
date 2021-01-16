---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305216"
---
# <span data-ttu-id="fd772-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="fd772-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="fd772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd772-102">SYNOPSIS</span></span>
<span data-ttu-id="fd772-103">Erstellen eines neuen Azure Front Door Load Balancers</span><span class="sxs-lookup"><span data-stu-id="fd772-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="fd772-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd772-104">SYNTAX</span></span>

### <span data-ttu-id="fd772-105">ByFieldsWithBackendPoolsSettingParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd772-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd772-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd772-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd772-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd772-107">DESCRIPTION</span></span>
<span data-ttu-id="fd772-108">Das **Cmdlet "New-AzFrontDsource"** erstellt einen neuen Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter dem aktuellen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd772-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="fd772-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd772-109">EXAMPLES</span></span>

### <span data-ttu-id="fd772-110">Beispiel 1: Erstellen einer Eingangstür basierend auf bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="fd772-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="fd772-111">Erstellen Sie eine Eingangstür basierend auf bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="fd772-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="fd772-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd772-112">PARAMETERS</span></span>

### <span data-ttu-id="fd772-113">-Back-EndPool</span><span class="sxs-lookup"><span data-stu-id="fd772-113">-BackendPool</span></span>
<span data-ttu-id="fd772-114">Für Routingregel verfügbare Back-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="fd772-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="fd772-115">-Back-EndPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="fd772-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="fd772-116">Einstellungen für alle Back-End-Pools</span><span class="sxs-lookup"><span data-stu-id="fd772-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd772-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd772-117">-DefaultProfile</span></span>
<span data-ttu-id="fd772-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd772-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd772-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="fd772-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="fd772-120">Gibt an, ob die Überprüfung des Zertifikatnamens für https-Anforderungen an alle Back-End-Pools deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd772-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="fd772-121">Keine Auswirkung auf Nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="fd772-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd772-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="fd772-122">-EnabledState</span></span>
<span data-ttu-id="fd772-123">EnabledState des Lastenausgleichs von Front Door.</span><span class="sxs-lookup"><span data-stu-id="fd772-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="fd772-124">Der Standardwert ist "Enabled".</span><span class="sxs-lookup"><span data-stu-id="fd772-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="fd772-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="fd772-125">-FrontendEndpoint</span></span>
<span data-ttu-id="fd772-126">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="fd772-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="fd772-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="fd772-127">-HealthProbeSetting</span></span>
<span data-ttu-id="fd772-128">Integritätstesteinstellungen, die dieser Instanz von Front Door zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fd772-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="fd772-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="fd772-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="fd772-130">Einstellungen für den Lastenausgleich, die dieser Front Door-Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fd772-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="fd772-131">-Name</span><span class="sxs-lookup"><span data-stu-id="fd772-131">-Name</span></span>
<span data-ttu-id="fd772-132">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="fd772-132">Front Door name.</span></span>

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

### <span data-ttu-id="fd772-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd772-133">-ResourceGroupName</span></span>
<span data-ttu-id="fd772-134">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd772-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="fd772-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="fd772-135">-RoutingRule</span></span>
<span data-ttu-id="fd772-136">Diesem FrontDrouting zugeordnete Routingregeln</span><span class="sxs-lookup"><span data-stu-id="fd772-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="fd772-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd772-137">-Tag</span></span>
<span data-ttu-id="fd772-138">Die Tags werden der FrontDasso zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="fd772-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="fd772-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd772-139">-Confirm</span></span>
<span data-ttu-id="fd772-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd772-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd772-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd772-141">-WhatIf</span></span>
<span data-ttu-id="fd772-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd772-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd772-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd772-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd772-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd772-144">CommonParameters</span></span>
<span data-ttu-id="fd772-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd772-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd772-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd772-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd772-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd772-147">INPUTS</span></span>

### <span data-ttu-id="fd772-148">Keine</span><span class="sxs-lookup"><span data-stu-id="fd772-148">None</span></span>
## <span data-ttu-id="fd772-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd772-149">OUTPUTS</span></span>

### <span data-ttu-id="fd772-150">Microsoft.Azure.Commands.Frontdando.Models.PSFrontDando</span><span class="sxs-lookup"><span data-stu-id="fd772-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="fd772-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd772-151">NOTES</span></span>

## <span data-ttu-id="fd772-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd772-152">RELATED LINKS</span></span>

<span data-ttu-id="fd772-153">[Get-AzFrontD verankert](./Get-AzFrontDoor.md) 
 [Set-AzFrontD verankert](./Set-AzFrontDoor.md) 
 [Remove-AzFrontD verankert](./Remove-AzFrontDoor.md) 
 [New-AzFrontDroutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDhealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDobjectLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDobjectFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDobjectBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="fd772-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>