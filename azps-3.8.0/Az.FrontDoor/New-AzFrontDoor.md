---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845523"
---
# <span data-ttu-id="836b1-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="836b1-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="836b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="836b1-102">SYNOPSIS</span></span>
<span data-ttu-id="836b1-103">Erstellen eines neuen Azure Front Door Load Balancer</span><span class="sxs-lookup"><span data-stu-id="836b1-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="836b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="836b1-104">SYNTAX</span></span>

### <span data-ttu-id="836b1-105">ByFieldsWithBackendPoolsSettingParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="836b1-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="836b1-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="836b1-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="836b1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="836b1-107">DESCRIPTION</span></span>
<span data-ttu-id="836b1-108">Das Cmdlet **New-AzFrontDoor** erstellt ein neues Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter Aktuelles Abonnement.</span><span class="sxs-lookup"><span data-stu-id="836b1-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="836b1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="836b1-109">EXAMPLES</span></span>

### <span data-ttu-id="836b1-110">Beispiel 1: Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="836b1-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="836b1-111">Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="836b1-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="836b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="836b1-112">PARAMETERS</span></span>

### <span data-ttu-id="836b1-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="836b1-113">-BackendPool</span></span>
<span data-ttu-id="836b1-114">Backendpools ist für Routingregel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="836b1-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="836b1-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="836b1-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="836b1-116">Einstellungen für alle backendPools</span><span class="sxs-lookup"><span data-stu-id="836b1-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="836b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836b1-117">-DefaultProfile</span></span>
<span data-ttu-id="836b1-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="836b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="836b1-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="836b1-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="836b1-120">Ob die Zertifikatnamen Überprüfung für HTTPS-Anforderungen an alle Back-End-Pools deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="836b1-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="836b1-121">Keine Auswirkungen auf nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="836b1-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="836b1-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="836b1-122">-EnabledState</span></span>
<span data-ttu-id="836b1-123">EnabledState des Front Door Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="836b1-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="836b1-124">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="836b1-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="836b1-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="836b1-125">-FrontendEndpoint</span></span>
<span data-ttu-id="836b1-126">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="836b1-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="836b1-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="836b1-127">-HealthProbeSetting</span></span>
<span data-ttu-id="836b1-128">Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="836b1-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="836b1-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="836b1-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="836b1-130">Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="836b1-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="836b1-131">-Name</span><span class="sxs-lookup"><span data-stu-id="836b1-131">-Name</span></span>
<span data-ttu-id="836b1-132">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="836b1-132">Front Door name.</span></span>

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

### <span data-ttu-id="836b1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836b1-133">-ResourceGroupName</span></span>
<span data-ttu-id="836b1-134">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="836b1-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="836b1-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="836b1-135">-RoutingRule</span></span>
<span data-ttu-id="836b1-136">Diesem Haustür zugeordnete Routing Regeln</span><span class="sxs-lookup"><span data-stu-id="836b1-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="836b1-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="836b1-137">-Tag</span></span>
<span data-ttu-id="836b1-138">Die Tags werden dem Haustür zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="836b1-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="836b1-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="836b1-139">-Confirm</span></span>
<span data-ttu-id="836b1-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="836b1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="836b1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="836b1-141">-WhatIf</span></span>
<span data-ttu-id="836b1-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="836b1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="836b1-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="836b1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="836b1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836b1-144">CommonParameters</span></span>
<span data-ttu-id="836b1-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836b1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836b1-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="836b1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836b1-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="836b1-147">INPUTS</span></span>

### <span data-ttu-id="836b1-148">Keine</span><span class="sxs-lookup"><span data-stu-id="836b1-148">None</span></span>
## <span data-ttu-id="836b1-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="836b1-149">OUTPUTS</span></span>

### <span data-ttu-id="836b1-150">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="836b1-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="836b1-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="836b1-151">NOTES</span></span>

## <span data-ttu-id="836b1-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="836b1-152">RELATED LINKS</span></span>

<span data-ttu-id="836b1-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Neu – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Neu – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Neu – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Neu – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="836b1-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>