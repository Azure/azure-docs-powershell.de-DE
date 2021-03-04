---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931176"
---
# <span data-ttu-id="afe60-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="afe60-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="afe60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe60-102">SYNOPSIS</span></span>
<span data-ttu-id="afe60-103">Erstellen eines neuen Azure Front Door Load Balancers</span><span class="sxs-lookup"><span data-stu-id="afe60-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="afe60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afe60-104">SYNTAX</span></span>

### <span data-ttu-id="afe60-105">ByFieldsWithBackendPoolsSettingParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="afe60-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe60-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe60-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe60-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afe60-107">DESCRIPTION</span></span>
<span data-ttu-id="afe60-108">Das **Cmdlet New-AzFrontDoor** erstellt einen neuen Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter dem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="afe60-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="afe60-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afe60-109">EXAMPLES</span></span>

### <span data-ttu-id="afe60-110">Beispiel 1: Erstellen einer Eingangstür basierend auf bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="afe60-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="afe60-111">Erstellen Sie eine Eingangstür basierend auf bestimmten Parametern.</span><span class="sxs-lookup"><span data-stu-id="afe60-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="afe60-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afe60-112">PARAMETERS</span></span>

### <span data-ttu-id="afe60-113">-Back-EndPool</span><span class="sxs-lookup"><span data-stu-id="afe60-113">-BackendPool</span></span>
<span data-ttu-id="afe60-114">Für die Routingregel verfügbare Back-Endpools.</span><span class="sxs-lookup"><span data-stu-id="afe60-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="afe60-115">-Back-EndPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="afe60-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="afe60-116">Einstellungen für alle Back-EndPools</span><span class="sxs-lookup"><span data-stu-id="afe60-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="afe60-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe60-117">-DefaultProfile</span></span>
<span data-ttu-id="afe60-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afe60-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe60-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="afe60-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="afe60-120">Ob die Zertifikatnamensprüfung für HTTPS-Anforderungen an alle Back-End-Pools deaktiviert werden soll</span><span class="sxs-lookup"><span data-stu-id="afe60-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="afe60-121">Keine Auswirkung auf Nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="afe60-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="afe60-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="afe60-122">-EnabledState</span></span>
<span data-ttu-id="afe60-123">EnabledState des Lastenausgleichs für die Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="afe60-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="afe60-124">Standardwert ist Aktiviert</span><span class="sxs-lookup"><span data-stu-id="afe60-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="afe60-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="afe60-125">-FrontendEndpoint</span></span>
<span data-ttu-id="afe60-126">Für die Routingregel verfügbare Frontendendpunkte.</span><span class="sxs-lookup"><span data-stu-id="afe60-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="afe60-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="afe60-127">-HealthProbeSetting</span></span>
<span data-ttu-id="afe60-128">Integritätstesteinstellungen, die dieser Front Door-Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="afe60-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="afe60-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="afe60-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="afe60-130">Lastenausgleichseinstellungen, die dieser Front Door-Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="afe60-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="afe60-131">-Name</span><span class="sxs-lookup"><span data-stu-id="afe60-131">-Name</span></span>
<span data-ttu-id="afe60-132">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="afe60-132">Front Door name.</span></span>

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

### <span data-ttu-id="afe60-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe60-133">-ResourceGroupName</span></span>
<span data-ttu-id="afe60-134">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="afe60-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="afe60-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="afe60-135">-RoutingRule</span></span>
<span data-ttu-id="afe60-136">Routingregeln, die diesem FrontDoor zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="afe60-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="afe60-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="afe60-137">-Tag</span></span>
<span data-ttu-id="afe60-138">Die Tags werden dem FrontDoor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="afe60-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="afe60-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afe60-139">-Confirm</span></span>
<span data-ttu-id="afe60-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afe60-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe60-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe60-141">-WhatIf</span></span>
<span data-ttu-id="afe60-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afe60-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe60-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afe60-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe60-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe60-144">CommonParameters</span></span>
<span data-ttu-id="afe60-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe60-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe60-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="afe60-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe60-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afe60-147">INPUTS</span></span>

### <span data-ttu-id="afe60-148">Keine</span><span class="sxs-lookup"><span data-stu-id="afe60-148">None</span></span>
## <span data-ttu-id="afe60-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afe60-149">OUTPUTS</span></span>

### <span data-ttu-id="afe60-150">Microsoft.Azure.Commands.Frontdoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="afe60-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="afe60-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afe60-151">NOTES</span></span>

## <span data-ttu-id="afe60-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afe60-152">RELATED LINKS</span></span>

<span data-ttu-id="afe60-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="afe60-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>