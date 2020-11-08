---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 0a23cec7a2006e2e30a60a722deef14704a4d2c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178741"
---
# <span data-ttu-id="b9a65-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9a65-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b9a65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9a65-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a65-103">Erstellt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="b9a65-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b9a65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9a65-104">SYNTAX</span></span>

### <span data-ttu-id="b9a65-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9a65-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9a65-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9a65-106">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9a65-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9a65-107">DESCRIPTION</span></span>
<span data-ttu-id="b9a65-108">Das Cmdlet **New-AzLoadBalancerRuleConfig** erstellt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="b9a65-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b9a65-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9a65-109">EXAMPLES</span></span>

### <span data-ttu-id="b9a65-110">Beispiel 1: Erstellen einer Regelkonfiguration für ein Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="b9a65-110">Example 1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="b9a65-111">Die ersten drei Befehle richten eine öffentliche IP-Adresse, ein Front-End und eine Sonde für die Regelkonfiguration im Befehl Forth ein.</span><span class="sxs-lookup"><span data-stu-id="b9a65-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="b9a65-112">Der Befehl Forth erstellt eine neue Regel namens MyLBrule mit bestimmten Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b9a65-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="b9a65-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9a65-113">PARAMETERS</span></span>

### <span data-ttu-id="b9a65-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9a65-114">-BackendAddressPool</span></span>
<span data-ttu-id="b9a65-115">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a65-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b9a65-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="b9a65-117">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a65-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b9a65-118">-BackendPort</span></span>
<span data-ttu-id="b9a65-119">Gibt den Back-End-Port für Datenverkehr an, der von dieser Load Balancer-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9a65-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a65-120">-DefaultProfile</span></span>
<span data-ttu-id="b9a65-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9a65-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a65-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="b9a65-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="b9a65-123">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9a65-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="b9a65-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b9a65-124">-EnableFloatingIP</span></span>
<span data-ttu-id="b9a65-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9a65-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b9a65-126">-EnableTcpReset</span></span>
<span data-ttu-id="b9a65-127">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="b9a65-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b9a65-128">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="b9a65-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b9a65-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a65-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="b9a65-130">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9a65-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b9a65-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="b9a65-132">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b9a65-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="b9a65-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b9a65-133">-FrontendPort</span></span>
<span data-ttu-id="b9a65-134">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="b9a65-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b9a65-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b9a65-136">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b9a65-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="b9a65-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="b9a65-137">-LoadDistribution</span></span>
<span data-ttu-id="b9a65-138">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="b9a65-138">Specifies a load distribution.</span></span>
<span data-ttu-id="b9a65-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b9a65-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b9a65-140">Standard</span><span class="sxs-lookup"><span data-stu-id="b9a65-140">Default</span></span>
- <span data-ttu-id="b9a65-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="b9a65-141">SourceIP</span></span>
- <span data-ttu-id="b9a65-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="b9a65-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="b9a65-143">-Name</span><span class="sxs-lookup"><span data-stu-id="b9a65-143">-Name</span></span>
<span data-ttu-id="b9a65-144">Gibt den Namen der vom Cmdlet erstellten Lastenausgleichs Regel an.</span><span class="sxs-lookup"><span data-stu-id="b9a65-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b9a65-145">-Sonde</span><span class="sxs-lookup"><span data-stu-id="b9a65-145">-Probe</span></span>
<span data-ttu-id="b9a65-146">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a65-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-147">-Sonde</span><span class="sxs-lookup"><span data-stu-id="b9a65-147">-ProbeId</span></span>
<span data-ttu-id="b9a65-148">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9a65-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="b9a65-149">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b9a65-149">-Protocol</span></span>
<span data-ttu-id="b9a65-150">Gibt das Protokoll an, das mit einer Konfiguration des Lastenausgleichsmoduls übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b9a65-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="b9a65-151">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="b9a65-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="b9a65-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9a65-152">-Confirm</span></span>
<span data-ttu-id="b9a65-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9a65-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9a65-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9a65-154">-WhatIf</span></span>
<span data-ttu-id="b9a65-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9a65-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9a65-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9a65-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9a65-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a65-157">CommonParameters</span></span>
<span data-ttu-id="b9a65-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a65-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a65-159">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a65-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a65-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9a65-160">INPUTS</span></span>

### <span data-ttu-id="b9a65-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b9a65-161">System.String</span></span>

### <span data-ttu-id="b9a65-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b9a65-162">System.Int32</span></span>

### <span data-ttu-id="b9a65-163">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9a65-163">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="b9a65-164">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9a65-164">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="b9a65-165">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="b9a65-165">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="b9a65-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9a65-166">OUTPUTS</span></span>

### <span data-ttu-id="b9a65-167">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="b9a65-167">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="b9a65-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9a65-168">NOTES</span></span>

## <span data-ttu-id="b9a65-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9a65-169">RELATED LINKS</span></span>

[<span data-ttu-id="b9a65-170">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9a65-170">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b9a65-171">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9a65-171">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b9a65-172">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9a65-172">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b9a65-173">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9a65-173">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


