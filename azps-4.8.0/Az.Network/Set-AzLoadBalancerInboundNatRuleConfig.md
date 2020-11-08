---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 68b3043b67580dcc781badb7c1891444e97e281f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174527"
---
# <span data-ttu-id="a3d3a-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3d3a-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="a3d3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d3a-103">Legt eine eingehende NAT-Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="a3d3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d3a-104">SYNTAX</span></span>

### <span data-ttu-id="a3d3a-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3d3a-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d3a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3d3a-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d3a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3d3a-107">DESCRIPTION</span></span>
<span data-ttu-id="a3d3a-108">Das Cmdlet " **Set-AzLoadBalancerInboundNatRuleConfig** " legt eine eingehende NAT-Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a3d3a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3d3a-109">EXAMPLES</span></span>

### <span data-ttu-id="a3d3a-110">Beispiel 1: Ändern der Konfiguration der eingehenden NAT-Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="a3d3a-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="a3d3a-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a3d3a-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="a3d3a-113">Der dritte Befehl übergibt das Load Balancer an "AzLoadBalancerInboundNatRuleConfig", wodurch die eingehende NAT **-** Regelkonfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="a3d3a-114">Beachten Sie, dass die Regelkonfiguration so festgesetzt wurde, dass keine unverankerte IP-Adresse aktiviert wurde, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="a3d3a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3d3a-115">PARAMETERS</span></span>

### <span data-ttu-id="a3d3a-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a3d3a-116">-BackendPort</span></span>
<span data-ttu-id="a3d3a-117">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="a3d3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d3a-118">-DefaultProfile</span></span>
<span data-ttu-id="a3d3a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d3a-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a3d3a-120">-EnableFloatingIP</span></span>
<span data-ttu-id="a3d3a-121">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="a3d3a-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a3d3a-122">-EnableTcpReset</span></span>
<span data-ttu-id="a3d3a-123">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a3d3a-124">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a3d3a-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3d3a-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a3d3a-126">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a3d3a-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a3d3a-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="a3d3a-128">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="a3d3a-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a3d3a-129">-FrontendPort</span></span>
<span data-ttu-id="a3d3a-130">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="a3d3a-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a3d3a-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a3d3a-132">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="a3d3a-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3d3a-133">-LoadBalancer</span></span>
<span data-ttu-id="a3d3a-134">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-134">Specifies a load balancer.</span></span>
<span data-ttu-id="a3d3a-135">Mit diesem Cmdlet wird eine eingehende NAT-Regelkonfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a3d3a-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a3d3a-136">-Name</span></span>
<span data-ttu-id="a3d3a-137">Gibt den Namen einer eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="a3d3a-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a3d3a-138">-Protocol</span></span>
<span data-ttu-id="a3d3a-139">Gibt das Protokoll an, das einer eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="a3d3a-140">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="a3d3a-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3d3a-141">-Confirm</span></span>
<span data-ttu-id="a3d3a-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d3a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d3a-143">-WhatIf</span></span>
<span data-ttu-id="a3d3a-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3d3a-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d3a-146">CommonParameters</span></span>
<span data-ttu-id="a3d3a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d3a-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d3a-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d3a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3d3a-149">INPUTS</span></span>

### <span data-ttu-id="a3d3a-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3d3a-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a3d3a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d3a-151">System.String</span></span>

### <span data-ttu-id="a3d3a-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a3d3a-152">System.Int32</span></span>

### <span data-ttu-id="a3d3a-153">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3d3a-153">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a3d3a-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3d3a-154">OUTPUTS</span></span>

### <span data-ttu-id="a3d3a-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3d3a-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a3d3a-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3d3a-156">NOTES</span></span>

## <span data-ttu-id="a3d3a-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3d3a-157">RELATED LINKS</span></span>

[<span data-ttu-id="a3d3a-158">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3d3a-158">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a3d3a-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3d3a-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a3d3a-160">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3d3a-160">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a3d3a-161">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3d3a-161">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="a3d3a-162">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3d3a-162">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


