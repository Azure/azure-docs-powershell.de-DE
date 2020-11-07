---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819991"
---
# <span data-ttu-id="34a1a-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="34a1a-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="34a1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="34a1a-103">Aktualisieren eines Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="34a1a-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="34a1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34a1a-104">SYNTAX</span></span>

### <span data-ttu-id="34a1a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="34a1a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34a1a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a1a-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34a1a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34a1a-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34a1a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34a1a-108">DESCRIPTION</span></span>
<span data-ttu-id="34a1a-109">Das Cmdlet " **Satz-AzFrontDoor** " aktualisiert ein Front-Load-Balancer.</span><span class="sxs-lookup"><span data-stu-id="34a1a-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="34a1a-110">Wenn keine Eingabeparameter angegeben werden, werden alte Parameter aus der vorhandenen Haustür verwendet.</span><span class="sxs-lookup"><span data-stu-id="34a1a-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="34a1a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34a1a-111">EXAMPLES</span></span>

### <span data-ttu-id="34a1a-112">Beispiel 1: Aktualisieren einer vorhandenen Haustür mit FrontDoorName und ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a1a-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="34a1a-113">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="34a1a-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="34a1a-114">Beispiel 2: Aktualisieren einer vorhandenen Haustür mit dem PSFrontDoor-Objekt</span><span class="sxs-lookup"><span data-stu-id="34a1a-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="34a1a-115">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="34a1a-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="34a1a-116">Beispiel 3: Aktualisieren einer vorhandenen Haustür mit "Resourcen"</span><span class="sxs-lookup"><span data-stu-id="34a1a-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="34a1a-117">Aktualisieren einer vorhandenen Haustür</span><span class="sxs-lookup"><span data-stu-id="34a1a-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="34a1a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="34a1a-118">PARAMETERS</span></span>

### <span data-ttu-id="34a1a-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="34a1a-119">-BackendPool</span></span>
<span data-ttu-id="34a1a-120">Backendpools ist für Routingregel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34a1a-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="34a1a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a1a-121">-DefaultProfile</span></span>
<span data-ttu-id="34a1a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="34a1a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a1a-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="34a1a-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="34a1a-124">Ob die Zertifikatnamen Überprüfung für HTTPS-Anforderungen an alle Back-End-Pools deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a1a-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="34a1a-125">Keine Auswirkungen auf nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="34a1a-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="34a1a-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="34a1a-126">-EnabledState</span></span>
<span data-ttu-id="34a1a-127">Betriebsstatus des Front-Load-Balancer</span><span class="sxs-lookup"><span data-stu-id="34a1a-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="34a1a-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="34a1a-128">-FrontendEndpoint</span></span>
<span data-ttu-id="34a1a-129">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="34a1a-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="34a1a-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="34a1a-130">-HealthProbeSetting</span></span>
<span data-ttu-id="34a1a-131">Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34a1a-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="34a1a-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34a1a-132">-InputObject</span></span>
<span data-ttu-id="34a1a-133">Das Haustür Objekt, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a1a-133">The Front Door object to update.</span></span>

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

### <span data-ttu-id="34a1a-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="34a1a-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="34a1a-135">Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34a1a-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="34a1a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="34a1a-136">-Name</span></span>
<span data-ttu-id="34a1a-137">Der Name der Haustür, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="34a1a-137">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="34a1a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a1a-138">-ResourceGroupName</span></span>
<span data-ttu-id="34a1a-139">Die Ressourcengruppe, zu der die Haustür gehört.</span><span class="sxs-lookup"><span data-stu-id="34a1a-139">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="34a1a-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="34a1a-140">-ResourceId</span></span>
<span data-ttu-id="34a1a-141">Ressourcen-ID der zu aktualisierende Haustür</span><span class="sxs-lookup"><span data-stu-id="34a1a-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34a1a-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="34a1a-142">-RoutingRule</span></span>
<span data-ttu-id="34a1a-143">Diesem Haustür zugeordnete Routing Regeln</span><span class="sxs-lookup"><span data-stu-id="34a1a-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="34a1a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="34a1a-144">-Tag</span></span>
<span data-ttu-id="34a1a-145">Die Tags werden dem Haustür zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="34a1a-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="34a1a-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34a1a-146">-Confirm</span></span>
<span data-ttu-id="34a1a-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34a1a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a1a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a1a-148">-WhatIf</span></span>
<span data-ttu-id="34a1a-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34a1a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34a1a-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34a1a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a1a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a1a-151">CommonParameters</span></span>
<span data-ttu-id="34a1a-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a1a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a1a-153">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34a1a-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a1a-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34a1a-154">INPUTS</span></span>

### <span data-ttu-id="34a1a-155">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="34a1a-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="34a1a-156">System. String</span><span class="sxs-lookup"><span data-stu-id="34a1a-156">System.String</span></span>

## <span data-ttu-id="34a1a-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34a1a-157">OUTPUTS</span></span>

### <span data-ttu-id="34a1a-158">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="34a1a-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="34a1a-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="34a1a-159">NOTES</span></span>

## <span data-ttu-id="34a1a-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34a1a-160">RELATED LINKS</span></span>

<span data-ttu-id="34a1a-161">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Neu – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Neu – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Neu – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Neu – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="34a1a-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
