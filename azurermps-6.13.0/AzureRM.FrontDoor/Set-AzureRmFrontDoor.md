---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476050"
---
# <span data-ttu-id="d1e87-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1e87-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="d1e87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1e87-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e87-103">Aktualisieren eines Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="d1e87-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e87-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1e87-104">SYNTAX</span></span>

### <span data-ttu-id="d1e87-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1e87-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e87-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e87-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1e87-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1e87-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1e87-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1e87-108">DESCRIPTION</span></span>
<span data-ttu-id="d1e87-109">Das Cmdlet " **Satz-AzureRmFrontDoor** " aktualisiert ein Front-Load-Balancer.</span><span class="sxs-lookup"><span data-stu-id="d1e87-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="d1e87-110">Wenn keine Eingabeparameter angegeben werden, werden alte Parameter aus der vorhandenen Haustür verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1e87-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="d1e87-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1e87-111">EXAMPLES</span></span>

### <span data-ttu-id="d1e87-112">Beispiel 1: Aktualisieren einer vorhandenen Haustür mit FrontDoorName und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e87-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="d1e87-113">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="d1e87-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="d1e87-114">Beispiel 2: Aktualisieren einer vorhandenen Haustür mit dem PSFrontDoor-Objekt</span><span class="sxs-lookup"><span data-stu-id="d1e87-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="d1e87-115">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="d1e87-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="d1e87-116">Beispiel 3: Aktualisieren einer vorhandenen Haustür mit "Resourcen"</span><span class="sxs-lookup"><span data-stu-id="d1e87-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="d1e87-117">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="d1e87-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="d1e87-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1e87-118">PARAMETERS</span></span>

### <span data-ttu-id="d1e87-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="d1e87-119">-BackendPool</span></span>
<span data-ttu-id="d1e87-120">Backendpools ist für Routingregel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1e87-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e87-121">-DefaultProfile</span></span>
<span data-ttu-id="d1e87-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1e87-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e87-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d1e87-123">-EnabledState</span></span>
<span data-ttu-id="d1e87-124">Betriebsstatus des Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="d1e87-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="d1e87-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1e87-125">-FrontendEndpoint</span></span>
<span data-ttu-id="d1e87-126">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="d1e87-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d1e87-127">-HealthProbeSetting</span></span>
<span data-ttu-id="d1e87-128">Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1e87-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1e87-129">-InputObject</span></span>
<span data-ttu-id="d1e87-130">Das Haustür Objekt, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e87-130">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="d1e87-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="d1e87-132">Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1e87-132">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d1e87-133">-Name</span></span>
<span data-ttu-id="d1e87-134">Der Name der Haustür, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e87-134">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e87-135">-ResourceGroupName</span></span>
<span data-ttu-id="d1e87-136">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="d1e87-136">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1e87-137">-ResourceId</span></span>
<span data-ttu-id="d1e87-138">Ressourcen-ID der zu aktualisierende Haustür</span><span class="sxs-lookup"><span data-stu-id="d1e87-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d1e87-139">-RoutingRule</span></span>
<span data-ttu-id="d1e87-140">Diesem Haustür zugeordnete Routing Regeln</span><span class="sxs-lookup"><span data-stu-id="d1e87-140">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1e87-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1e87-141">-Tag</span></span>
<span data-ttu-id="d1e87-142">Die Tags werden dem Haustür zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d1e87-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="d1e87-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1e87-143">-Confirm</span></span>
<span data-ttu-id="d1e87-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1e87-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e87-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e87-145">-WhatIf</span></span>
<span data-ttu-id="d1e87-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e87-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e87-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1e87-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e87-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e87-148">CommonParameters</span></span>
<span data-ttu-id="d1e87-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1e87-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e87-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e87-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e87-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1e87-151">INPUTS</span></span>

### <span data-ttu-id="d1e87-152">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1e87-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="d1e87-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e87-153">System.String</span></span>

## <span data-ttu-id="d1e87-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1e87-154">OUTPUTS</span></span>

### <span data-ttu-id="d1e87-155">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d1e87-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="d1e87-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1e87-156">NOTES</span></span>

## <span data-ttu-id="d1e87-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1e87-157">RELATED LINKS</span></span>

<span data-ttu-id="d1e87-158">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Neu – AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Neu – AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Neu – AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Neu – AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="d1e87-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
