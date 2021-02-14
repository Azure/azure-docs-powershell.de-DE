---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5965cd5e27c5e408f7b55ea5d181dc8670668168
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154492"
---
# <span data-ttu-id="c3aab-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3aab-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c3aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3aab-102">SYNOPSIS</span></span>
<span data-ttu-id="c3aab-103">Fügt einem Lastenausgleich eine Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3aab-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="c3aab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3aab-104">SYNTAX</span></span>

### <span data-ttu-id="c3aab-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3aab-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3aab-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3aab-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3aab-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3aab-107">DESCRIPTION</span></span>
<span data-ttu-id="c3aab-108">Das **Cmdlet "Add-AzLoadBalancerRuleConfig"** fügt einem Azure Load Balancer eine Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3aab-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c3aab-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3aab-109">EXAMPLES</span></span>

### <span data-ttu-id="c3aab-110">Beispiel 1: Hinzufügen einer Regelkonfiguration zu einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="c3aab-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="c3aab-111">Der erste Befehl ruft den Lastenausgleich namens "MyLoadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="c3aab-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c3aab-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an **Add-AzLoadBalancerRuleConfig** zu übergeben, wodurch die Regelkonfiguration "NewRule" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c3aab-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig**, which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="c3aab-113">Der dritte Befehl aktualisiert den Lastenausgleich in Azure mit der neuen Load Balancer Rule Config.</span><span class="sxs-lookup"><span data-stu-id="c3aab-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="c3aab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3aab-114">PARAMETERS</span></span>

### <span data-ttu-id="c3aab-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c3aab-115">-BackendAddressPool</span></span>
<span data-ttu-id="c3aab-116">Gibt den Back-End-Adresspool an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-117">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c3aab-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="c3aab-118">Gibt die ID eines **Back-EndAddressPool-Objekts** an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-119">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="c3aab-119">-BackendPort</span></span>
<span data-ttu-id="c3aab-120">Gibt den Back-End-Port für Datenverkehr an, der durch eine Load Balancer-Regelkonfiguration abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c3aab-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3aab-121">-DefaultProfile</span></span>
<span data-ttu-id="c3aab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3aab-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3aab-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c3aab-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c3aab-124">Konfiguriert SNAT für die VMs im Back-End-Pool so, dass die im Frontend der Lastenausgleichsregel angegebene publicIP-Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3aab-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c3aab-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c3aab-125">-EnableFloatingIP</span></span>
<span data-ttu-id="c3aab-126">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c3aab-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c3aab-127">-EnableTcpReset</span></span>
<span data-ttu-id="c3aab-128">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c3aab-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c3aab-129">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c3aab-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c3aab-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3aab-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c3aab-131">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c3aab-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c3aab-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c3aab-133">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c3aab-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c3aab-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c3aab-134">-FrontendPort</span></span>
<span data-ttu-id="c3aab-135">Gibt den Front-End-Port an, der einer Load Balancer-Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c3aab-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c3aab-137">Gibt die Dauer (in Minuten) an, für die der Unterhaltungsstatus im Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="c3aab-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="c3aab-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3aab-138">-LoadBalancer</span></span>
<span data-ttu-id="c3aab-139">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c3aab-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="c3aab-140">Dieses Cmdlet fügt dem Lastenausgleich, den dieser Parameter angibt, eine Regelkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="c3aab-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3aab-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c3aab-141">-LoadDistribution</span></span>
<span data-ttu-id="c3aab-142">Gibt eine Lastenverteilung an.</span><span class="sxs-lookup"><span data-stu-id="c3aab-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="c3aab-143">-Name</span><span class="sxs-lookup"><span data-stu-id="c3aab-143">-Name</span></span>
<span data-ttu-id="c3aab-144">Gibt den Namen der Load Balancer-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c3aab-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="c3aab-145">-Probe</span></span>
<span data-ttu-id="c3aab-146">Gibt eine Sonde an, die einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c3aab-147">-ProbeId</span></span>
<span data-ttu-id="c3aab-148">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c3aab-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c3aab-149">-Protocol</span></span>
<span data-ttu-id="c3aab-150">Gibt das Protokoll an, das einer Lastenausgleichsregel entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="c3aab-150">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="c3aab-151">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="c3aab-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c3aab-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3aab-152">-Confirm</span></span>
<span data-ttu-id="c3aab-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3aab-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3aab-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c3aab-154">-WhatIf</span></span>
<span data-ttu-id="c3aab-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3aab-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3aab-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3aab-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3aab-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3aab-157">CommonParameters</span></span>
<span data-ttu-id="c3aab-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3aab-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3aab-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3aab-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3aab-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3aab-160">INPUTS</span></span>

### <span data-ttu-id="c3aab-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3aab-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="c3aab-162">System.String</span><span class="sxs-lookup"><span data-stu-id="c3aab-162">System.String</span></span>

### <span data-ttu-id="c3aab-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c3aab-163">System.Int32</span></span>

### <span data-ttu-id="c3aab-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3aab-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="c3aab-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c3aab-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="c3aab-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="c3aab-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c3aab-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3aab-167">OUTPUTS</span></span>

### <span data-ttu-id="c3aab-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3aab-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3aab-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c3aab-169">NOTES</span></span>

## <span data-ttu-id="c3aab-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c3aab-170">RELATED LINKS</span></span>

[<span data-ttu-id="c3aab-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3aab-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c3aab-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3aab-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c3aab-173">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3aab-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c3aab-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3aab-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c3aab-175">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c3aab-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


