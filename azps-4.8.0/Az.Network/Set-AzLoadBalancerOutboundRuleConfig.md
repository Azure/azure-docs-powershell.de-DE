---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009640"
---
# <span data-ttu-id="56fa3-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56fa3-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="56fa3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="56fa3-103">Legt eine ausgehende Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="56fa3-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="56fa3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56fa3-104">SYNTAX</span></span>

### <span data-ttu-id="56fa3-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="56fa3-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56fa3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56fa3-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56fa3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56fa3-107">DESCRIPTION</span></span>
<span data-ttu-id="56fa3-108">Das Cmdlet " **Set-AzLoadBalancerOutboundRuleConfig** " legt eine ausgehende Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="56fa3-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="56fa3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56fa3-109">EXAMPLES</span></span>

### <span data-ttu-id="56fa3-110">Beispiel 1: Ändern der Konfiguration der ausgehenden Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="56fa3-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="56fa3-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="56fa3-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerOutboundRuleConfig zu übergeben, wodurch eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="56fa3-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="56fa3-113">Der dritte Befehl übergibt das Load Balancer an " **AzLoadBalancerOutboundRuleConfig** ", wodurch die Konfiguration der ausgehenden Regel gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="56fa3-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="56fa3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="56fa3-114">PARAMETERS</span></span>

### <span data-ttu-id="56fa3-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="56fa3-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="56fa3-116">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="56fa3-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="56fa3-117">-BackendAddressPool</span></span>
<span data-ttu-id="56fa3-118">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="56fa3-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="56fa3-119">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="56fa3-120">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="56fa3-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="56fa3-121">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="56fa3-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="56fa3-122">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="56fa3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fa3-123">-DefaultProfile</span></span>
<span data-ttu-id="56fa3-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56fa3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fa3-125">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="56fa3-125">-EnableTcpReset</span></span>
<span data-ttu-id="56fa3-126">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="56fa3-127">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="56fa3-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="56fa3-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56fa3-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="56fa3-129">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="56fa3-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="56fa3-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="56fa3-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="56fa3-131">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="56fa3-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="56fa3-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56fa3-132">-LoadBalancer</span></span>
<span data-ttu-id="56fa3-133">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="56fa3-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="56fa3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="56fa3-134">-Name</span></span>
<span data-ttu-id="56fa3-135">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="56fa3-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="56fa3-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="56fa3-136">-Protocol</span></span>
<span data-ttu-id="56fa3-137">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="56fa3-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="56fa3-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="56fa3-138">-Confirm</span></span>
<span data-ttu-id="56fa3-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="56fa3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56fa3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56fa3-140">-WhatIf</span></span>
<span data-ttu-id="56fa3-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="56fa3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56fa3-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="56fa3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56fa3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fa3-143">CommonParameters</span></span>
<span data-ttu-id="56fa3-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56fa3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fa3-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56fa3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fa3-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56fa3-146">INPUTS</span></span>

### <span data-ttu-id="56fa3-147">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56fa3-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="56fa3-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="56fa3-148">System.Int32</span></span>

### <span data-ttu-id="56fa3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="56fa3-149">System.String</span></span>

### <span data-ttu-id="56fa3-150">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="56fa3-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="56fa3-151">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="56fa3-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="56fa3-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56fa3-152">OUTPUTS</span></span>

### <span data-ttu-id="56fa3-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56fa3-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="56fa3-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="56fa3-154">NOTES</span></span>

## <span data-ttu-id="56fa3-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56fa3-155">RELATED LINKS</span></span>

[<span data-ttu-id="56fa3-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56fa3-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="56fa3-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56fa3-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="56fa3-158">Neu – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56fa3-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="56fa3-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56fa3-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)
