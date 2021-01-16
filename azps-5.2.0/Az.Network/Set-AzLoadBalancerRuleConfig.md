---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d86af5e56b44526cdc717d91927193cfcb3fd444
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307160"
---
# <span data-ttu-id="569d8-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="569d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="569d8-102">SYNOPSIS</span></span>
<span data-ttu-id="569d8-103">Aktualisiert eine Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="569d8-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="569d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="569d8-104">SYNTAX</span></span>

### <span data-ttu-id="569d8-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="569d8-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="569d8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="569d8-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="569d8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="569d8-107">DESCRIPTION</span></span>
<span data-ttu-id="569d8-108">Das **Cmdlet "Set-AzLoadBalancerRuleConfig"** aktualisiert eine Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="569d8-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="569d8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="569d8-109">EXAMPLES</span></span>

### <span data-ttu-id="569d8-110">Beispiel 1: Ändern der Konfiguration einer Lastenausgleichsregel</span><span class="sxs-lookup"><span data-stu-id="569d8-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="569d8-111">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="569d8-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="569d8-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerRuleConfig zu übergeben, wodurch ihm eine Regel mit dem Namen "NewRule" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="569d8-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="569d8-113">Der dritte Befehl übergibt den Lastenausgleich an **Set-AzLoadBalancerRuleConfig,** wodurch die neue Regelkonfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="569d8-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig**, which sets the new rule configuration.</span></span>
<span data-ttu-id="569d8-114">Beachten Sie, dass die Konfiguration keine unverankerte IP-Adresse aktiviert, die mit dem vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="569d8-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="569d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="569d8-115">PARAMETERS</span></span>

### <span data-ttu-id="569d8-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="569d8-116">-BackendAddressPool</span></span>
<span data-ttu-id="569d8-117">Gibt ein **Back-EndAddressPool-Objekt** an, das einer Load Balancer-Regel zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="569d8-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="569d8-119">Gibt die ID eines **Back-EndAddressPool-Objekts** an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-120">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="569d8-120">-BackendPort</span></span>
<span data-ttu-id="569d8-121">Gibt den Back-End-Port für Datenverkehr an, der mit dieser Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569d8-122">-DefaultProfile</span></span>
<span data-ttu-id="569d8-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="569d8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="569d8-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="569d8-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="569d8-125">Konfiguriert SNAT für die VMs im Back-End-Pool so, dass die im Frontend der Lastenausgleichsregel angegebene publicIP-Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="569d8-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="569d8-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="569d8-126">-EnableFloatingIP</span></span>
<span data-ttu-id="569d8-127">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="569d8-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="569d8-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="569d8-128">-EnableTcpReset</span></span>
<span data-ttu-id="569d8-129">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="569d8-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="569d8-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="569d8-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="569d8-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="569d8-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="569d8-132">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="569d8-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="569d8-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="569d8-134">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="569d8-134">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="569d8-135">-FrontendPort</span></span>
<span data-ttu-id="569d8-136">Gibt den Front-End-Port an, der einer Load Balancer-Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="569d8-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="569d8-138">Gibt die Dauer in Minuten an, für die der Unterhaltungsstatus in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="569d8-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="569d8-139">-LoadBalancer</span></span>
<span data-ttu-id="569d8-140">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="569d8-140">Specifies a load balancer.</span></span>
<span data-ttu-id="569d8-141">Dieses Cmdlet aktualisiert eine Regelkonfiguration für den Lastenausgleich, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="569d8-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="569d8-142">-LoadDistribution</span></span>
<span data-ttu-id="569d8-143">Gibt eine Lastenverteilung an.</span><span class="sxs-lookup"><span data-stu-id="569d8-143">Specifies a load distribution.</span></span>
<span data-ttu-id="569d8-144">Für diesen Parameter sind die Werte "SourceIP" und "SourceIPProtocol" zulässig.</span><span class="sxs-lookup"><span data-stu-id="569d8-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-145">-Name</span><span class="sxs-lookup"><span data-stu-id="569d8-145">-Name</span></span>
<span data-ttu-id="569d8-146">Gibt den Namen eines Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="569d8-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="569d8-147">-Probe</span><span class="sxs-lookup"><span data-stu-id="569d8-147">-Probe</span></span>
<span data-ttu-id="569d8-148">Gibt eine Sonde an, die einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-149">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="569d8-149">-ProbeId</span></span>
<span data-ttu-id="569d8-150">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-151">-Protocol</span><span class="sxs-lookup"><span data-stu-id="569d8-151">-Protocol</span></span>
<span data-ttu-id="569d8-152">Gibt das Protokoll an, das einer Lastenausgleichsregel entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="569d8-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="569d8-153">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="569d8-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="569d8-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="569d8-154">-Confirm</span></span>
<span data-ttu-id="569d8-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="569d8-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="569d8-156">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="569d8-156">-WhatIf</span></span>
<span data-ttu-id="569d8-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="569d8-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="569d8-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="569d8-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="569d8-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569d8-159">CommonParameters</span></span>
<span data-ttu-id="569d8-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="569d8-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569d8-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569d8-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569d8-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="569d8-162">INPUTS</span></span>

### <span data-ttu-id="569d8-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="569d8-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="569d8-164">System.String</span><span class="sxs-lookup"><span data-stu-id="569d8-164">System.String</span></span>

### <span data-ttu-id="569d8-165">System.Int32</span><span class="sxs-lookup"><span data-stu-id="569d8-165">System.Int32</span></span>

### <span data-ttu-id="569d8-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="569d8-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="569d8-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="569d8-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="569d8-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="569d8-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="569d8-169">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="569d8-169">OUTPUTS</span></span>

### <span data-ttu-id="569d8-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="569d8-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="569d8-171">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="569d8-171">NOTES</span></span>

## <span data-ttu-id="569d8-172">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="569d8-172">RELATED LINKS</span></span>

[<span data-ttu-id="569d8-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="569d8-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="569d8-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="569d8-176">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="569d8-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="569d8-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


