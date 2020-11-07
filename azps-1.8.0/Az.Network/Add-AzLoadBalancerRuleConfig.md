---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 580351ae3b46eb3f1c1d8bfd5c3562fdd208556e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660909"
---
# <span data-ttu-id="732f7-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="732f7-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="732f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="732f7-102">SYNOPSIS</span></span>
<span data-ttu-id="732f7-103">Fügt eine Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="732f7-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="732f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="732f7-104">SYNTAX</span></span>

### <span data-ttu-id="732f7-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="732f7-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="732f7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="732f7-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-LoadDistribution <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="732f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="732f7-107">DESCRIPTION</span></span>
<span data-ttu-id="732f7-108">Mit dem Cmdlet **Add-AzLoadBalancerRuleConfig** wird eine Regelkonfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="732f7-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="732f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="732f7-109">EXAMPLES</span></span>

### <span data-ttu-id="732f7-110">Beispiel 1: Hinzufügen einer Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="732f7-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\>$slb | Set-AzLoadBalancer
```

<span data-ttu-id="732f7-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="732f7-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="732f7-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzLoadBalancerRuleConfig** zu übergeben, wodurch die Regelkonfiguration mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="732f7-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>
<span data-ttu-id="732f7-113">Der dritte Befehl aktualisiert das Load Balancer in Azure mit der neuen Load Balancer-Regelkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="732f7-113">The third command will update the load balancer in azure with the new Load Balancer Rule Config.</span></span>

## <span data-ttu-id="732f7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="732f7-114">PARAMETERS</span></span>

### <span data-ttu-id="732f7-115">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="732f7-115">-BackendAddressPool</span></span>
<span data-ttu-id="732f7-116">Gibt den Back-End-Adresspool an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="732f7-116">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-117">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="732f7-117">-BackendAddressPoolId</span></span>
<span data-ttu-id="732f7-118">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="732f7-118">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-119">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="732f7-119">-BackendPort</span></span>
<span data-ttu-id="732f7-120">Gibt den Back-End-Port für Datenverkehr an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="732f7-120">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732f7-121">-DefaultProfile</span></span>
<span data-ttu-id="732f7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="732f7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="732f7-123">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="732f7-123">-DisableOutboundSNAT</span></span>
<span data-ttu-id="732f7-124">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="732f7-124">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="732f7-125">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="732f7-125">-EnableFloatingIP</span></span>
<span data-ttu-id="732f7-126">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="732f7-126">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="732f7-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="732f7-127">-EnableTcpReset</span></span>
<span data-ttu-id="732f7-128">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="732f7-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="732f7-129">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="732f7-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="732f7-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="732f7-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="732f7-131">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="732f7-131">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-132">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="732f7-132">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="732f7-133">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="732f7-133">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="732f7-134">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="732f7-134">-FrontendPort</span></span>
<span data-ttu-id="732f7-135">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="732f7-135">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-136">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="732f7-136">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="732f7-137">Gibt an, wie lange in Minuten der Status der Konversationen im Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="732f7-137">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="732f7-138">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="732f7-138">-LoadBalancer</span></span>
<span data-ttu-id="732f7-139">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="732f7-139">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="732f7-140">Dieses Cmdlet fügt dem Load Balancer eine Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="732f7-140">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="732f7-141">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="732f7-141">-LoadDistribution</span></span>
<span data-ttu-id="732f7-142">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="732f7-142">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="732f7-143">-Name</span><span class="sxs-lookup"><span data-stu-id="732f7-143">-Name</span></span>
<span data-ttu-id="732f7-144">Gibt den Namen der Load Balancer-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="732f7-144">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-145">-Sonde</span><span class="sxs-lookup"><span data-stu-id="732f7-145">-Probe</span></span>
<span data-ttu-id="732f7-146">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="732f7-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-147">-Sonde</span><span class="sxs-lookup"><span data-stu-id="732f7-147">-ProbeId</span></span>
<span data-ttu-id="732f7-148">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="732f7-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="732f7-149">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="732f7-149">-Protocol</span></span>
<span data-ttu-id="732f7-150">Gibt an Sie das Protokoll, das mit einer Load Balancer-Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="732f7-150">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="732f7-151">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="732f7-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="732f7-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="732f7-152">-Confirm</span></span>
<span data-ttu-id="732f7-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="732f7-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="732f7-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="732f7-154">-WhatIf</span></span>
<span data-ttu-id="732f7-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="732f7-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="732f7-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="732f7-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="732f7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732f7-157">CommonParameters</span></span>
<span data-ttu-id="732f7-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732f7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732f7-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732f7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732f7-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="732f7-160">INPUTS</span></span>

### <span data-ttu-id="732f7-161">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="732f7-161">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="732f7-162">System. String</span><span class="sxs-lookup"><span data-stu-id="732f7-162">System.String</span></span>

### <span data-ttu-id="732f7-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="732f7-163">System.Int32</span></span>

### <span data-ttu-id="732f7-164">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="732f7-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

### <span data-ttu-id="732f7-165">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="732f7-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

### <span data-ttu-id="732f7-166">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="732f7-166">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="732f7-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="732f7-167">OUTPUTS</span></span>

### <span data-ttu-id="732f7-168">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="732f7-168">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="732f7-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="732f7-169">NOTES</span></span>

## <span data-ttu-id="732f7-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="732f7-170">RELATED LINKS</span></span>

[<span data-ttu-id="732f7-171">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="732f7-171">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="732f7-172">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="732f7-172">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="732f7-173">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="732f7-173">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="732f7-174">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="732f7-174">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="732f7-175">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="732f7-175">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


