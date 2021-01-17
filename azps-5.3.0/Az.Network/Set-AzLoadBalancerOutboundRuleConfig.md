---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472164"
---
# <span data-ttu-id="8652e-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8652e-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="8652e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8652e-102">SYNOPSIS</span></span>
<span data-ttu-id="8652e-103">Legt eine ausgehende Regelkonfiguration für einen Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="8652e-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8652e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8652e-104">SYNTAX</span></span>

### <span data-ttu-id="8652e-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8652e-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8652e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8652e-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8652e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8652e-107">DESCRIPTION</span></span>
<span data-ttu-id="8652e-108">Das **Cmdlet "Set-AzLoadBalancerOutboundRuleConfig"** legt eine ausgehende Regelkonfiguration für einen Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="8652e-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8652e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8652e-109">EXAMPLES</span></span>

### <span data-ttu-id="8652e-110">Beispiel 1: Ändern der Konfiguration ausgehender Regeln für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="8652e-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="8652e-111">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="8652e-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="8652e-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerOutboundRuleConfig zu übergeben, wodurch eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8652e-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="8652e-113">Der dritte Befehl übergibt den Lastenausgleich an **Set-AzLoadBalancerOutboundRuleConfig,** wodurch die ausgehende Regelkonfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8652e-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig**, which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="8652e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8652e-114">PARAMETERS</span></span>

### <span data-ttu-id="8652e-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="8652e-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="8652e-116">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8652e-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="8652e-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8652e-117">-BackendAddressPool</span></span>
<span data-ttu-id="8652e-118">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="8652e-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8652e-119">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="8652e-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8652e-120">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8652e-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="8652e-121">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="8652e-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="8652e-122">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="8652e-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8652e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8652e-123">-DefaultProfile</span></span>
<span data-ttu-id="8652e-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8652e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8652e-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8652e-125">-EnableTcpReset</span></span>
<span data-ttu-id="8652e-126">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="8652e-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="8652e-127">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8652e-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="8652e-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8652e-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8652e-129">Die Frontend-IP-Adressen des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="8652e-129">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8652e-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8652e-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8652e-131">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="8652e-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="8652e-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8652e-132">-LoadBalancer</span></span>
<span data-ttu-id="8652e-133">Der Verweis auf die Lastenausgleichsressource.</span><span class="sxs-lookup"><span data-stu-id="8652e-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="8652e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8652e-134">-Name</span></span>
<span data-ttu-id="8652e-135">Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="8652e-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="8652e-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8652e-136">-Protocol</span></span>
<span data-ttu-id="8652e-137">Protokoll – TCP, UDP oder Alle</span><span class="sxs-lookup"><span data-stu-id="8652e-137">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8652e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8652e-138">-Confirm</span></span>
<span data-ttu-id="8652e-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8652e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8652e-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8652e-140">-WhatIf</span></span>
<span data-ttu-id="8652e-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8652e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8652e-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8652e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8652e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8652e-143">CommonParameters</span></span>
<span data-ttu-id="8652e-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8652e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8652e-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8652e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8652e-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8652e-146">INPUTS</span></span>

### <span data-ttu-id="8652e-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8652e-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="8652e-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8652e-148">System.Int32</span></span>

### <span data-ttu-id="8652e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8652e-149">System.String</span></span>

### <span data-ttu-id="8652e-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="8652e-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="8652e-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8652e-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8652e-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8652e-152">OUTPUTS</span></span>

### <span data-ttu-id="8652e-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8652e-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8652e-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8652e-154">NOTES</span></span>

## <span data-ttu-id="8652e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8652e-155">RELATED LINKS</span></span>

[<span data-ttu-id="8652e-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8652e-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8652e-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8652e-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8652e-158">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8652e-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="8652e-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8652e-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
