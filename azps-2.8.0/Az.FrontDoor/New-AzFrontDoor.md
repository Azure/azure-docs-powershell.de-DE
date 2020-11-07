---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651130"
---
# <span data-ttu-id="c3e33-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c3e33-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="c3e33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3e33-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e33-103">Erstellen eines neuen Azure Front Door Load Balancer</span><span class="sxs-lookup"><span data-stu-id="c3e33-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="c3e33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3e33-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e33-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3e33-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e33-106">Das Cmdlet **New-AzFrontDoor** erstellt ein neues Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter Aktuelles Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3e33-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="c3e33-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3e33-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e33-108">Beispiel 1: Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="c3e33-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="c3e33-109">Erstellen einer Haustür basierend auf bestimmten Parametern</span><span class="sxs-lookup"><span data-stu-id="c3e33-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="c3e33-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e33-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e33-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="c3e33-111">-BackendPool</span></span>
<span data-ttu-id="c3e33-112">Backendpools ist für Routingregel verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c3e33-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="c3e33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e33-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e33-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3e33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e33-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c3e33-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="c3e33-116">Ob die Zertifikatnamen Überprüfung für HTTPS-Anforderungen an alle Back-End-Pools deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3e33-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="c3e33-117">Keine Auswirkungen auf nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="c3e33-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="c3e33-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c3e33-118">-EnabledState</span></span>
<span data-ttu-id="c3e33-119">EnabledState des Front Door Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="c3e33-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="c3e33-120">Standardwert ist aktiviert</span><span class="sxs-lookup"><span data-stu-id="c3e33-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="c3e33-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3e33-121">-FrontendEndpoint</span></span>
<span data-ttu-id="c3e33-122">Für Routingregel verfügbare Frontend-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="c3e33-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="c3e33-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c3e33-123">-HealthProbeSetting</span></span>
<span data-ttu-id="c3e33-124">Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3e33-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c3e33-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="c3e33-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="c3e33-126">Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c3e33-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c3e33-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c3e33-127">-Name</span></span>
<span data-ttu-id="c3e33-128">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="c3e33-128">Front Door name.</span></span>

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

### <span data-ttu-id="c3e33-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e33-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3e33-130">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e33-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c3e33-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3e33-131">-RoutingRule</span></span>
<span data-ttu-id="c3e33-132">Diesem Haustür zugeordnete Routing Regeln</span><span class="sxs-lookup"><span data-stu-id="c3e33-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="c3e33-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3e33-133">-Tag</span></span>
<span data-ttu-id="c3e33-134">Die Tags werden dem Haustür zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c3e33-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="c3e33-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3e33-135">-Confirm</span></span>
<span data-ttu-id="c3e33-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3e33-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e33-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e33-137">-WhatIf</span></span>
<span data-ttu-id="c3e33-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3e33-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e33-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3e33-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e33-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e33-140">CommonParameters</span></span>
<span data-ttu-id="c3e33-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e33-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e33-142">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e33-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e33-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3e33-143">INPUTS</span></span>

### <span data-ttu-id="c3e33-144">Keine</span><span class="sxs-lookup"><span data-stu-id="c3e33-144">None</span></span>

## <span data-ttu-id="c3e33-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3e33-145">OUTPUTS</span></span>

### <span data-ttu-id="c3e33-146">Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c3e33-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="c3e33-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3e33-147">NOTES</span></span>

## <span data-ttu-id="c3e33-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3e33-148">RELATED LINKS</span></span>

<span data-ttu-id="c3e33-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [Neu – AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [Neu – AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [Neu – AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [Neu – AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="c3e33-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>