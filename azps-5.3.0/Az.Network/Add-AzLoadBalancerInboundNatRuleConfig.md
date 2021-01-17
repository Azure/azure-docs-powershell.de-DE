---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467475"
---
# <span data-ttu-id="0c1ed-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c1ed-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="0c1ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1ed-103">Fügt einem Lastenausgleich eine eingehende Konfiguration der NAT-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="0c1ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c1ed-104">SYNTAX</span></span>

### <span data-ttu-id="0c1ed-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c1ed-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c1ed-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c1ed-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c1ed-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c1ed-107">DESCRIPTION</span></span>
<span data-ttu-id="0c1ed-108">Das **Cmdlet "Add-AzLoadBalancerInboundNatRuleConfig"** fügt einem Azure Load Balancer eine Konfiguration der eingehenden Netzwerkadressenübersetzung (Nat) hinzu.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="0c1ed-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c1ed-109">EXAMPLES</span></span>

### <span data-ttu-id="0c1ed-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="0c1ed-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="0c1ed-111">Der erste Befehl ruft den Lastenausgleich namens "MyloadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="0c1ed-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an **Add-AzLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleich eine konfiguration der eingehenden NAT-Regel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="0c1ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c1ed-113">PARAMETERS</span></span>

### <span data-ttu-id="0c1ed-114">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="0c1ed-114">-BackendPort</span></span>
<span data-ttu-id="0c1ed-115">Gibt den Back-End-Port für den Datenverkehr an, der mit einer Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0c1ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1ed-116">-DefaultProfile</span></span>
<span data-ttu-id="0c1ed-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c1ed-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0c1ed-118">-EnableFloatingIP</span></span>
<span data-ttu-id="0c1ed-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="0c1ed-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0c1ed-120">-EnableTcpReset</span></span>
<span data-ttu-id="0c1ed-121">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0c1ed-122">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0c1ed-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c1ed-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="0c1ed-124">Gibt eine Liste der Front-End-IP-Adressen an, die einer konfiguration der eingehenden NAT-Regel zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="0c1ed-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0c1ed-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="0c1ed-126">Gibt eine ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="0c1ed-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="0c1ed-127">-FrontendPort</span></span>
<span data-ttu-id="0c1ed-128">Gibt den Front-End-Port an, der einer Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="0c1ed-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0c1ed-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0c1ed-130">Gibt die Dauer (in Minuten) an, für die der Unterhaltungszustand in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="0c1ed-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c1ed-131">-LoadBalancer</span></span>
<span data-ttu-id="0c1ed-132">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="0c1ed-133">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Lastenausgleich eine Konfiguration der eingehenden NAT-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c1ed-134">-Name</span><span class="sxs-lookup"><span data-stu-id="0c1ed-134">-Name</span></span>
<span data-ttu-id="0c1ed-135">Gibt den Namen der konfiguration der eingehenden NAT-Regel an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="0c1ed-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0c1ed-136">-Protocol</span></span>
<span data-ttu-id="0c1ed-137">Gibt das Protokoll an, das mit einer eingehenden NAT-Regel übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="0c1ed-138">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="0c1ed-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c1ed-139">-Confirm</span></span>
<span data-ttu-id="0c1ed-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c1ed-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0c1ed-141">-WhatIf</span></span>
<span data-ttu-id="0c1ed-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c1ed-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c1ed-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1ed-144">CommonParameters</span></span>
<span data-ttu-id="0c1ed-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c1ed-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1ed-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1ed-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1ed-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c1ed-147">INPUTS</span></span>

### <span data-ttu-id="0c1ed-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c1ed-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0c1ed-149">System.String</span><span class="sxs-lookup"><span data-stu-id="0c1ed-149">System.String</span></span>

### <span data-ttu-id="0c1ed-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0c1ed-150">System.Int32</span></span>

### <span data-ttu-id="0c1ed-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c1ed-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0c1ed-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c1ed-152">OUTPUTS</span></span>

### <span data-ttu-id="0c1ed-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c1ed-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0c1ed-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c1ed-154">NOTES</span></span>

## <span data-ttu-id="0c1ed-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c1ed-155">RELATED LINKS</span></span>

[<span data-ttu-id="0c1ed-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c1ed-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0c1ed-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c1ed-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c1ed-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c1ed-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c1ed-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c1ed-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0c1ed-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0c1ed-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="0c1ed-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0c1ed-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


