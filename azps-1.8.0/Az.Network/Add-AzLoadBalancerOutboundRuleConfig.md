---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 79a8442d28d6e04d4e6e013e536663a19faaf3f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660911"
---
# <span data-ttu-id="9a166-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a166-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="9a166-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a166-102">SYNOPSIS</span></span>
<span data-ttu-id="9a166-103">Fügt eine ausgehende Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="9a166-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="9a166-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a166-104">SYNTAX</span></span>

### <span data-ttu-id="9a166-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a166-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a166-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a166-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a166-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a166-107">DESCRIPTION</span></span>
<span data-ttu-id="9a166-108">Mit dem Cmdlet **Add-AzLoadBalancerOutboundRuleConfig** wird eine ausgehende Regelkonfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9a166-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="9a166-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a166-109">EXAMPLES</span></span>

### <span data-ttu-id="9a166-110">Beispiel 1: Hinzufügen einer ausgehenden Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="9a166-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="9a166-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="9a166-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="9a166-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzLoadBalancerOutboundRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine ausgehende Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9a166-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="9a166-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a166-113">PARAMETERS</span></span>

### <span data-ttu-id="9a166-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="9a166-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="9a166-115">Die Anzahl der ausgehenden Ports, die für NAT verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a166-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="9a166-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9a166-116">-BackendAddressPool</span></span>
<span data-ttu-id="9a166-117">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="9a166-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9a166-118">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="9a166-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9a166-119">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9a166-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="9a166-120">Ein Verweis auf einen Pool von Dips.</span><span class="sxs-lookup"><span data-stu-id="9a166-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="9a166-121">Der ausgehende Datenverkehr wird nach dem Zufallsprinzip auf IPS im Back-End-IPS geladen.</span><span class="sxs-lookup"><span data-stu-id="9a166-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="9a166-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a166-122">-DefaultProfile</span></span>
<span data-ttu-id="9a166-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a166-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a166-124">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9a166-124">-EnableTcpReset</span></span>
<span data-ttu-id="9a166-125">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="9a166-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="9a166-126">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9a166-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9a166-127">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a166-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9a166-128">Die Frontend-IP-Adressen des Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="9a166-128">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="9a166-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9a166-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9a166-130">Timeout für die TCP-Leerlaufverbindung</span><span class="sxs-lookup"><span data-stu-id="9a166-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="9a166-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a166-131">-LoadBalancer</span></span>
<span data-ttu-id="9a166-132">Der Verweis der Load Balancer-Ressource.</span><span class="sxs-lookup"><span data-stu-id="9a166-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="9a166-133">-Name</span><span class="sxs-lookup"><span data-stu-id="9a166-133">-Name</span></span>
<span data-ttu-id="9a166-134">Der Name der ausgehenden Regel.</span><span class="sxs-lookup"><span data-stu-id="9a166-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="9a166-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9a166-135">-Protocol</span></span>
<span data-ttu-id="9a166-136">Protokoll – TCP, UDP oder alle</span><span class="sxs-lookup"><span data-stu-id="9a166-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="9a166-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a166-137">-Confirm</span></span>
<span data-ttu-id="9a166-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a166-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a166-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a166-139">-WhatIf</span></span>
<span data-ttu-id="9a166-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a166-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a166-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a166-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a166-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a166-142">CommonParameters</span></span>
<span data-ttu-id="9a166-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a166-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a166-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a166-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a166-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a166-145">INPUTS</span></span>

### <span data-ttu-id="9a166-146">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a166-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9a166-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9a166-147">System.Int32</span></span>

### <span data-ttu-id="9a166-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9a166-148">System.String</span></span>

### <span data-ttu-id="9a166-149">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="9a166-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="9a166-150">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9a166-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="9a166-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a166-151">OUTPUTS</span></span>

### <span data-ttu-id="9a166-152">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9a166-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9a166-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a166-153">NOTES</span></span>

## <span data-ttu-id="9a166-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a166-154">RELATED LINKS</span></span>

[<span data-ttu-id="9a166-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a166-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a166-156">Neu – AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a166-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a166-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a166-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="9a166-158">Satz-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9a166-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
