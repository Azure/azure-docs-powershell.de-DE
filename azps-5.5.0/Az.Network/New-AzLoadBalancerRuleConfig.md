---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160881"
---
# <span data-ttu-id="72fe5-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72fe5-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="72fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="72fe5-103">Erstellt eine Regelkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="72fe5-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="72fe5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72fe5-104">SYNTAX</span></span>

### <span data-ttu-id="72fe5-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="72fe5-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72fe5-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="72fe5-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fe5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72fe5-107">DESCRIPTION</span></span>
<span data-ttu-id="72fe5-108">Das **Cmdlet "New-AzLoadBalancerRuleConfig"** erstellt eine Regelkonfiguration für einen Azure-Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="72fe5-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="72fe5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72fe5-109">EXAMPLES</span></span>

### <span data-ttu-id="72fe5-110">Beispiel 1: Erstellen einer Regelkonfiguration für einen Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="72fe5-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
```powershell
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" `
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd `
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port `
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration `
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp `
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP `
    -LoadDistribution SourceIP
```

<span data-ttu-id="72fe5-111">Die ersten drei Befehle richten eine öffentliche IP, ein Front-End und eine Sonde für die Regelkonfiguration im vierten Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="72fe5-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="72fe5-112">Der vierte Befehl erstellt eine neue Regel namens "MyLBrule" mit bestimmten Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="72fe5-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="72fe5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72fe5-113">PARAMETERS</span></span>

### <span data-ttu-id="72fe5-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72fe5-114">-BackendAddressPool</span></span>
<span data-ttu-id="72fe5-115">Gibt ein **Back-EndAddressPool-Objekt** an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-116">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="72fe5-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="72fe5-117">Gibt die ID eines **Back-EndAddressPool-Objekts** an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-118">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="72fe5-118">-BackendPort</span></span>
<span data-ttu-id="72fe5-119">Gibt den Back-End-Port für Datenverkehr an, der durch diese Konfiguration der Lastenausgleichsregel abgestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="72fe5-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fe5-120">-DefaultProfile</span></span>
<span data-ttu-id="72fe5-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72fe5-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72fe5-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="72fe5-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="72fe5-123">Konfiguriert SNAT für die VMs im Back-End-Pool so, dass die im Frontend der Lastenausgleichsregel angegebene publicIP-Adresse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72fe5-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="72fe5-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="72fe5-124">-EnableFloatingIP</span></span>
<span data-ttu-id="72fe5-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="72fe5-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="72fe5-126">-EnableTcpReset</span></span>
<span data-ttu-id="72fe5-127">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="72fe5-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="72fe5-128">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="72fe5-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="72fe5-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="72fe5-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="72fe5-130">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="72fe5-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="72fe5-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="72fe5-132">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="72fe5-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="72fe5-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="72fe5-133">-FrontendPort</span></span>
<span data-ttu-id="72fe5-134">Gibt den Front-End-Port an, der einer Load Balancer-Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="72fe5-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="72fe5-136">Gibt die Dauer (in Minuten) an, für die der Unterhaltungszustand in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="72fe5-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="72fe5-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="72fe5-137">-LoadDistribution</span></span>
<span data-ttu-id="72fe5-138">Gibt eine Lastenverteilung an.</span><span class="sxs-lookup"><span data-stu-id="72fe5-138">Specifies a load distribution.</span></span>
<span data-ttu-id="72fe5-139">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="72fe5-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72fe5-140">Standard</span><span class="sxs-lookup"><span data-stu-id="72fe5-140">Default</span></span>
- <span data-ttu-id="72fe5-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="72fe5-141">SourceIP</span></span>
- <span data-ttu-id="72fe5-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="72fe5-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="72fe5-143">-Name</span><span class="sxs-lookup"><span data-stu-id="72fe5-143">-Name</span></span>
<span data-ttu-id="72fe5-144">Gibt den Namen der Lastenausgleichsregel an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="72fe5-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="72fe5-145">-Probe</span><span class="sxs-lookup"><span data-stu-id="72fe5-145">-Probe</span></span>
<span data-ttu-id="72fe5-146">Gibt eine Sonde an, die einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-147">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="72fe5-147">-ProbeId</span></span>
<span data-ttu-id="72fe5-148">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="72fe5-149">-Protocol</span><span class="sxs-lookup"><span data-stu-id="72fe5-149">-Protocol</span></span>
<span data-ttu-id="72fe5-150">Gibt das Protokoll an, das einer Load Balancer-Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="72fe5-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="72fe5-151">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="72fe5-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="72fe5-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72fe5-152">-Confirm</span></span>
<span data-ttu-id="72fe5-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72fe5-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72fe5-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72fe5-154">-WhatIf</span></span>
<span data-ttu-id="72fe5-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72fe5-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72fe5-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72fe5-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72fe5-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fe5-157">CommonParameters</span></span>
<span data-ttu-id="72fe5-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72fe5-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fe5-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fe5-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fe5-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72fe5-160">INPUTS</span></span>

### <span data-ttu-id="72fe5-161">System.String</span><span class="sxs-lookup"><span data-stu-id="72fe5-161">System.String</span></span>

### <span data-ttu-id="72fe5-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="72fe5-162">System.Int32</span></span>

### <span data-ttu-id="72fe5-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="72fe5-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="72fe5-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="72fe5-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="72fe5-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span><span class="sxs-lookup"><span data-stu-id="72fe5-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="72fe5-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72fe5-166">OUTPUTS</span></span>

### <span data-ttu-id="72fe5-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="72fe5-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="72fe5-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72fe5-168">NOTES</span></span>

## <span data-ttu-id="72fe5-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72fe5-169">RELATED LINKS</span></span>

[<span data-ttu-id="72fe5-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72fe5-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72fe5-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72fe5-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72fe5-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72fe5-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="72fe5-173">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="72fe5-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


