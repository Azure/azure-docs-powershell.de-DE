---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356668"
---
# <span data-ttu-id="980ed-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="980ed-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="980ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="980ed-102">SYNOPSIS</span></span>
<span data-ttu-id="980ed-103">Legt eine eingehende KONFIGURATION der NAT-Regel für einen Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="980ed-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="980ed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="980ed-104">SYNTAX</span></span>

### <span data-ttu-id="980ed-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="980ed-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="980ed-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="980ed-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="980ed-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="980ed-107">DESCRIPTION</span></span>
<span data-ttu-id="980ed-108">Das **Cmdlet "Set-AzLoadBalancerInboundNatRuleConfig"** legt eine Regelkonfiguration für die eingehende Netzwerkadressenübersetzung (Nat) für einen Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="980ed-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="980ed-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="980ed-109">EXAMPLES</span></span>

### <span data-ttu-id="980ed-110">Beispiel 1: Ändern der Konfiguration der eingehenden NAT-Regel für einen Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="980ed-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="980ed-111">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann in der $slb Variable.</span><span class="sxs-lookup"><span data-stu-id="980ed-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="980ed-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende KONFIGURATION der NAT-Regel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="980ed-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="980ed-113">Der dritte Befehl übergibt den Lastenausgleich an **Set-AzLoadBalancerInboundNatRuleConfig,** wodurch die Konfiguration der eingehenden NAT-Regel gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="980ed-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig**, which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="980ed-114">Beachten Sie, dass die Regelkonfiguration ohne Aktivierung der unverankerten IP festgelegt wurde, die durch den vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="980ed-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="980ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="980ed-115">PARAMETERS</span></span>

### <span data-ttu-id="980ed-116">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="980ed-116">-BackendPort</span></span>
<span data-ttu-id="980ed-117">Gibt den Back-End-Port für Datenverkehr an, der mit dieser Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="980ed-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="980ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980ed-118">-DefaultProfile</span></span>
<span data-ttu-id="980ed-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="980ed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="980ed-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="980ed-120">-EnableFloatingIP</span></span>
<span data-ttu-id="980ed-121">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="980ed-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="980ed-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="980ed-122">-EnableTcpReset</span></span>
<span data-ttu-id="980ed-123">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="980ed-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="980ed-124">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="980ed-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="980ed-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="980ed-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="980ed-126">Gibt eine Liste der Front-End-IP-Adressen an, die einer konfiguration der eingehenden NAT-Regel zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="980ed-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="980ed-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="980ed-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="980ed-128">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="980ed-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="980ed-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="980ed-129">-FrontendPort</span></span>
<span data-ttu-id="980ed-130">Gibt den Front-End-Port an, der einer Load Balancer-Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="980ed-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="980ed-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="980ed-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="980ed-132">Gibt die Dauer (in Minuten) an, für die der Unterhaltungszustand in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="980ed-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="980ed-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="980ed-133">-LoadBalancer</span></span>
<span data-ttu-id="980ed-134">Gibt einen Lastenausgleich an.</span><span class="sxs-lookup"><span data-stu-id="980ed-134">Specifies a load balancer.</span></span>
<span data-ttu-id="980ed-135">Dieses Cmdlet legt eine eingehende NAT-Regelkonfiguration für den Lastenausgleich fest, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="980ed-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="980ed-136">-Name</span><span class="sxs-lookup"><span data-stu-id="980ed-136">-Name</span></span>
<span data-ttu-id="980ed-137">Gibt den Namen einer eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="980ed-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="980ed-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="980ed-138">-Protocol</span></span>
<span data-ttu-id="980ed-139">Gibt das Protokoll an, das einer eingehenden KONFIGURATION einer NAT-Regel entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="980ed-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="980ed-140">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="980ed-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="980ed-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="980ed-141">-Confirm</span></span>
<span data-ttu-id="980ed-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="980ed-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="980ed-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="980ed-143">-WhatIf</span></span>
<span data-ttu-id="980ed-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="980ed-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="980ed-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="980ed-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="980ed-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980ed-146">CommonParameters</span></span>
<span data-ttu-id="980ed-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="980ed-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980ed-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="980ed-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980ed-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="980ed-149">INPUTS</span></span>

### <span data-ttu-id="980ed-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="980ed-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="980ed-151">System.String</span><span class="sxs-lookup"><span data-stu-id="980ed-151">System.String</span></span>

### <span data-ttu-id="980ed-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="980ed-152">System.Int32</span></span>

### <span data-ttu-id="980ed-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="980ed-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="980ed-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="980ed-154">OUTPUTS</span></span>

### <span data-ttu-id="980ed-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="980ed-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="980ed-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="980ed-156">NOTES</span></span>

## <span data-ttu-id="980ed-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="980ed-157">RELATED LINKS</span></span>

[<span data-ttu-id="980ed-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="980ed-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="980ed-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="980ed-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="980ed-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="980ed-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="980ed-161">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="980ed-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="980ed-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="980ed-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


