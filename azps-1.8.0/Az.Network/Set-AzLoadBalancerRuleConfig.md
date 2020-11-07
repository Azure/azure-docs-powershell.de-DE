---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 11baabe406180e92a4a6af0f62b5e3b285e016b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660206"
---
# <span data-ttu-id="44918-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="44918-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44918-102">SYNOPSIS</span></span>
<span data-ttu-id="44918-103">Aktualisiert eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="44918-103">Updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="44918-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44918-104">SYNTAX</span></span>

### <span data-ttu-id="44918-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="44918-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44918-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="44918-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44918-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44918-107">DESCRIPTION</span></span>
<span data-ttu-id="44918-108">Das Cmdlet " **Satz-AzLoadBalancerRuleConfig** " aktualisiert eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="44918-108">The **Set-AzLoadBalancerRuleConfig** cmdlet updates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="44918-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44918-109">EXAMPLES</span></span>

### <span data-ttu-id="44918-110">Beispiel 1: Ändern einer Lastenausgleichs Regel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="44918-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="44918-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="44918-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="44918-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerRuleConfig zu übergeben, wodurch eine Regel mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="44918-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>
<span data-ttu-id="44918-113">Der dritte Befehl übergibt das Load Balancer an **Set-AzLoadBalancerRuleConfig** , wodurch die neue Regelkonfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44918-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="44918-114">Beachten Sie, dass die Konfiguration keine unverankerte IP-Adresse aktiviert, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="44918-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="44918-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="44918-115">PARAMETERS</span></span>

### <span data-ttu-id="44918-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="44918-116">-BackendAddressPool</span></span>
<span data-ttu-id="44918-117">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regel zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44918-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

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

### <span data-ttu-id="44918-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="44918-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="44918-119">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44918-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="44918-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="44918-120">-BackendPort</span></span>
<span data-ttu-id="44918-121">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="44918-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="44918-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44918-122">-DefaultProfile</span></span>
<span data-ttu-id="44918-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44918-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44918-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="44918-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="44918-125">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="44918-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="44918-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="44918-126">-EnableFloatingIP</span></span>
<span data-ttu-id="44918-127">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="44918-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="44918-128">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="44918-128">-EnableTcpReset</span></span>
<span data-ttu-id="44918-129">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="44918-129">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="44918-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="44918-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="44918-131">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="44918-131">-FrontendIpConfiguration</span></span>
<span data-ttu-id="44918-132">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="44918-132">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="44918-133">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="44918-133">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="44918-134">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="44918-134">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="44918-135">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="44918-135">-FrontendPort</span></span>
<span data-ttu-id="44918-136">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="44918-136">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="44918-137">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="44918-137">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="44918-138">Gibt die Zeitdauer in Minuten an, für die der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="44918-138">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="44918-139">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44918-139">-LoadBalancer</span></span>
<span data-ttu-id="44918-140">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="44918-140">Specifies a load balancer.</span></span>
<span data-ttu-id="44918-141">Dieses Cmdlet aktualisiert eine Regelkonfiguration für das Load Balancer, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="44918-141">This cmdlet updates a rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="44918-142">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="44918-142">-LoadDistribution</span></span>
<span data-ttu-id="44918-143">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="44918-143">Specifies a load distribution.</span></span>
<span data-ttu-id="44918-144">Die zulässigen Werte für diesen Parameter sind: SourceIP und SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="44918-144">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

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

### <span data-ttu-id="44918-145">-Name</span><span class="sxs-lookup"><span data-stu-id="44918-145">-Name</span></span>
<span data-ttu-id="44918-146">Gibt den Namen eines Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="44918-146">Specifies the name of a load balancer.</span></span>

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

### <span data-ttu-id="44918-147">-Sonde</span><span class="sxs-lookup"><span data-stu-id="44918-147">-Probe</span></span>
<span data-ttu-id="44918-148">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44918-148">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="44918-149">-Sonde</span><span class="sxs-lookup"><span data-stu-id="44918-149">-ProbeId</span></span>
<span data-ttu-id="44918-150">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="44918-150">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="44918-151">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="44918-151">-Protocol</span></span>
<span data-ttu-id="44918-152">Gibt das Protokoll an, das mit einer Load Balancer-Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="44918-152">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="44918-153">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="44918-153">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="44918-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44918-154">-Confirm</span></span>
<span data-ttu-id="44918-155">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44918-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44918-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44918-156">-WhatIf</span></span>
<span data-ttu-id="44918-157">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44918-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44918-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44918-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44918-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44918-159">CommonParameters</span></span>
<span data-ttu-id="44918-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44918-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44918-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44918-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44918-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44918-162">INPUTS</span></span>

### <span data-ttu-id="44918-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44918-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="44918-164">System. String</span><span class="sxs-lookup"><span data-stu-id="44918-164">System.String</span></span>

### <span data-ttu-id="44918-165">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44918-165">System.Int32</span></span>

### <span data-ttu-id="44918-166">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="44918-166">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="44918-167">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="44918-167">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="44918-168">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="44918-168">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="44918-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44918-169">OUTPUTS</span></span>

### <span data-ttu-id="44918-170">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="44918-170">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="44918-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="44918-171">NOTES</span></span>

## <span data-ttu-id="44918-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44918-172">RELATED LINKS</span></span>

[<span data-ttu-id="44918-173">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-173">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="44918-174">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-174">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="44918-175">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-175">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="44918-176">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-176">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="44918-177">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44918-177">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


