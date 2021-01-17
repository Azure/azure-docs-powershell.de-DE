---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467476"
---
# <span data-ttu-id="e52cd-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e52cd-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="e52cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e52cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e52cd-103">Fügt eine ausgehende Regelkonfiguration zu einem Lastenausgleich hinzu.</span><span class="sxs-lookup"><span data-stu-id="e52cd-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="e52cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e52cd-104">SYNTAX</span></span>

### <span data-ttu-id="e52cd-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e52cd-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e52cd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e52cd-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e52cd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e52cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e52cd-108">Das **Cmdlet "Add-AzLoadBalancerOutboundRuleConfig"** fügt einem Azure Load Balancer eine ausgehende Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="e52cd-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="e52cd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e52cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e52cd-110">Beispiel 1: Hinzufügen einer ausgehenden Regelkonfiguration zu einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="e52cd-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="e52cd-111">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="e52cd-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e52cd-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an **Add-AzLoadBalancerOutboundRuleConfig** zu übergeben, wodurch dem Lastenausgleich eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e52cd-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig**, which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="e52cd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e52cd-113">PARAMETERS</span></span>

### <span data-ttu-id="e52cd-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="e52cd-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="e52cd-115">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e52cd-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="e52cd-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e52cd-116">-BackendAddressPool</span></span>
<span data-ttu-id="e52cd-117">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="e52cd-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e52cd-118">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="e52cd-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="e52cd-119">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e52cd-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="e52cd-120">Ein Verweis auf einen Pool von DIPs.</span><span class="sxs-lookup"><span data-stu-id="e52cd-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e52cd-121">Ausgehender Datenverkehr wird nach dem Zufallsprinzip für alle IPs in den Back-End-IPs geladen.</span><span class="sxs-lookup"><span data-stu-id="e52cd-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="e52cd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e52cd-122">-DefaultProfile</span></span>
<span data-ttu-id="e52cd-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e52cd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e52cd-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e52cd-124">-EnableTcpReset</span></span>
<span data-ttu-id="e52cd-125">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e52cd-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="e52cd-126">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e52cd-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e52cd-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e52cd-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e52cd-128">Die Frontend-IP-Adressen des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="e52cd-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="e52cd-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e52cd-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e52cd-130">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="e52cd-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="e52cd-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e52cd-131">-LoadBalancer</span></span>
<span data-ttu-id="e52cd-132">Der Verweis auf die Lastenausgleichsressource.</span><span class="sxs-lookup"><span data-stu-id="e52cd-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="e52cd-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e52cd-133">-Name</span></span>
<span data-ttu-id="e52cd-134">Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="e52cd-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="e52cd-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e52cd-135">-Protocol</span></span>
<span data-ttu-id="e52cd-136">Protokoll – TCP, UDP oder Alle</span><span class="sxs-lookup"><span data-stu-id="e52cd-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="e52cd-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e52cd-137">-Confirm</span></span>
<span data-ttu-id="e52cd-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e52cd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e52cd-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e52cd-139">-WhatIf</span></span>
<span data-ttu-id="e52cd-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e52cd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e52cd-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e52cd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e52cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52cd-142">CommonParameters</span></span>
<span data-ttu-id="e52cd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e52cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52cd-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e52cd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52cd-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e52cd-145">INPUTS</span></span>

### <span data-ttu-id="e52cd-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e52cd-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="e52cd-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e52cd-147">System.Int32</span></span>

### <span data-ttu-id="e52cd-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e52cd-148">System.String</span></span>

### <span data-ttu-id="e52cd-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="e52cd-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="e52cd-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e52cd-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e52cd-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e52cd-151">OUTPUTS</span></span>

### <span data-ttu-id="e52cd-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e52cd-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e52cd-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e52cd-153">NOTES</span></span>

## <span data-ttu-id="e52cd-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e52cd-154">RELATED LINKS</span></span>

[<span data-ttu-id="e52cd-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e52cd-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e52cd-156">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e52cd-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e52cd-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e52cd-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e52cd-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e52cd-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
