---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 44f8304ce1ee79c114dc4054c8dd7fff3dcd22fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946025"
---
# <span data-ttu-id="79aa1-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79aa1-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="79aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa1-103">Fügt einem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="79aa1-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="79aa1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79aa1-104">SYNTAX</span></span>

### <span data-ttu-id="79aa1-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="79aa1-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79aa1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79aa1-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79aa1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79aa1-107">DESCRIPTION</span></span>
<span data-ttu-id="79aa1-108">Das **Add-AzLoadBalancerInboundNatRuleConfig-Cmdlet** fügt einem Azure Load Balancer eine Nat-Regelkonfiguration (Inbound Network Address Translation) hinzu.</span><span class="sxs-lookup"><span data-stu-id="79aa1-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="79aa1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79aa1-109">EXAMPLES</span></span>

### <span data-ttu-id="79aa1-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Load Balancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="79aa1-111">Der erste Befehl ruft den Load Balancer mit dem Namen MyloadBalancer ab und speichert ihn dann in der Variablen $slb.</span><span class="sxs-lookup"><span data-stu-id="79aa1-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="79aa1-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an **Add-AzLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="79aa1-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>
<span data-ttu-id="79aa1-113">Mit dem letzten Befehl wird die Konfiguration auf das Loadbalancer festgelegt. Wenn Sie Set-AzLoadBalancer nicht ausführen, werden Ihre Änderungen nicht auf das Loadbalancer angewendet.</span><span class="sxs-lookup"><span data-stu-id="79aa1-113">The last command sets the configuration to the loadbalancer, if you don't perform Set-AzLoadBalancer, your changes will not be applied to the loadbalancer.</span></span>

## <span data-ttu-id="79aa1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="79aa1-114">PARAMETERS</span></span>

### <span data-ttu-id="79aa1-115">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="79aa1-115">-BackendPort</span></span>
<span data-ttu-id="79aa1-116">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="79aa1-116">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="79aa1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79aa1-117">-DefaultProfile</span></span>
<span data-ttu-id="79aa1-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79aa1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79aa1-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="79aa1-119">-EnableFloatingIP</span></span>
<span data-ttu-id="79aa1-120">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="79aa1-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="79aa1-121">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="79aa1-121">-EnableTcpReset</span></span>
<span data-ttu-id="79aa1-122">Empfangen eines bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="79aa1-122">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="79aa1-123">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79aa1-123">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="79aa1-124">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="79aa1-124">-FrontendIpConfiguration</span></span>
<span data-ttu-id="79aa1-125">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="79aa1-125">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="79aa1-126">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="79aa1-126">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="79aa1-127">Gibt eine ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="79aa1-127">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="79aa1-128">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="79aa1-128">-FrontendPort</span></span>
<span data-ttu-id="79aa1-129">Gibt den Front-End-Port an, der mit einer Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="79aa1-129">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="79aa1-130">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="79aa1-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="79aa1-131">Gibt die Dauer in Minuten an, die der Zustand der Unterhaltungen in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="79aa1-131">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="79aa1-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-132">-LoadBalancer</span></span>
<span data-ttu-id="79aa1-133">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="79aa1-133">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="79aa1-134">Dieses Cmdlet fügt dem load balancer, den dieser Parameter angibt, eine eingehende NAT-Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="79aa1-134">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="79aa1-135">-Name</span><span class="sxs-lookup"><span data-stu-id="79aa1-135">-Name</span></span>
<span data-ttu-id="79aa1-136">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79aa1-136">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="79aa1-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="79aa1-137">-Protocol</span></span>
<span data-ttu-id="79aa1-138">Gibt das Protokoll an, das mit einer eingehenden NAT-Regel übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="79aa1-138">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="79aa1-139">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="79aa1-139">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="79aa1-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79aa1-140">-Confirm</span></span>
<span data-ttu-id="79aa1-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79aa1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79aa1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79aa1-142">-WhatIf</span></span>
<span data-ttu-id="79aa1-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79aa1-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79aa1-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79aa1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79aa1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa1-145">CommonParameters</span></span>
<span data-ttu-id="79aa1-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79aa1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa1-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79aa1-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa1-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79aa1-148">INPUTS</span></span>

### <span data-ttu-id="79aa1-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="79aa1-150">System.String</span><span class="sxs-lookup"><span data-stu-id="79aa1-150">System.String</span></span>

### <span data-ttu-id="79aa1-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="79aa1-151">System.Int32</span></span>

### <span data-ttu-id="79aa1-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="79aa1-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="79aa1-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79aa1-153">OUTPUTS</span></span>

### <span data-ttu-id="79aa1-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79aa1-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="79aa1-155">NOTES</span></span>

## <span data-ttu-id="79aa1-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="79aa1-156">RELATED LINKS</span></span>

[<span data-ttu-id="79aa1-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="79aa1-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79aa1-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="79aa1-159">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79aa1-159">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="79aa1-160">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79aa1-160">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="79aa1-161">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79aa1-161">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="79aa1-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="79aa1-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


