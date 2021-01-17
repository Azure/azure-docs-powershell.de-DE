---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365587"
---
# <span data-ttu-id="d0854-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0854-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d0854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0854-102">SYNOPSIS</span></span>
<span data-ttu-id="d0854-103">Fügt einem Lastenausgleich eine eingehende Konfiguration der NAT-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0854-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="d0854-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0854-104">SYNTAX</span></span>

### <span data-ttu-id="d0854-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0854-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0854-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0854-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0854-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0854-107">DESCRIPTION</span></span>
<span data-ttu-id="d0854-108">Das **Cmdlet "Add-AzLoadBalancerInboundNatRuleConfig"** fügt einem Azure Load Balancer eine Konfiguration der eingehenden Netzwerkadressenübersetzung (Nat) hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0854-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d0854-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0854-109">EXAMPLES</span></span>

### <span data-ttu-id="d0854-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="d0854-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="d0854-111">Der erste Befehl ruft den Lastenausgleich namens "MyloadBalancer" ab und speichert ihn dann im Variablenspeicher $slb.</span><span class="sxs-lookup"><span data-stu-id="d0854-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d0854-112">Der zweite Befehl verwendet den Pipelineoperator, um den Lastenausgleich in $slb an **Add-AzLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleich eine konfiguration der eingehenden NAT-Regel hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d0854-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig**, which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d0854-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0854-113">PARAMETERS</span></span>

### <span data-ttu-id="d0854-114">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="d0854-114">-BackendPort</span></span>
<span data-ttu-id="d0854-115">Gibt den Back-End-Port für den Datenverkehr an, der mit einer Regelkonfiguration übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="d0854-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d0854-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0854-116">-DefaultProfile</span></span>
<span data-ttu-id="d0854-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0854-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0854-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d0854-118">-EnableFloatingIP</span></span>
<span data-ttu-id="d0854-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d0854-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d0854-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d0854-120">-EnableTcpReset</span></span>
<span data-ttu-id="d0854-121">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d0854-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d0854-122">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d0854-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d0854-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0854-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d0854-124">Gibt eine Liste der Front-End-IP-Adressen an, die einer konfiguration für eingehende NAT-Regeln zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d0854-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d0854-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0854-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d0854-126">Gibt eine ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d0854-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d0854-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d0854-127">-FrontendPort</span></span>
<span data-ttu-id="d0854-128">Gibt den Front-End-Port an, der einer Regelkonfiguration entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="d0854-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d0854-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d0854-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d0854-130">Gibt die Dauer (in Minuten) an, für die der Unterhaltungszustand in einem Lastenausgleich beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d0854-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d0854-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0854-131">-LoadBalancer</span></span>
<span data-ttu-id="d0854-132">Gibt ein **LoadBalancer-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d0854-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d0854-133">Dieses Cmdlet fügt dem von diesem Parameter angegebenen Lastenausgleich eine Konfiguration der eingehenden NAT-Regel hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0854-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0854-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d0854-134">-Name</span></span>
<span data-ttu-id="d0854-135">Gibt den Namen der konfiguration der eingehenden NAT-Regel an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0854-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="d0854-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d0854-136">-Protocol</span></span>
<span data-ttu-id="d0854-137">Gibt das Protokoll an, das mit einer eingehenden NAT-Regel übereinstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="d0854-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="d0854-138">Die zulässigen Werte für diesen Parameter sind: Tcp oder Udp.</span><span class="sxs-lookup"><span data-stu-id="d0854-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d0854-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0854-139">-Confirm</span></span>
<span data-ttu-id="d0854-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0854-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0854-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d0854-141">-WhatIf</span></span>
<span data-ttu-id="d0854-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0854-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0854-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0854-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0854-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0854-144">CommonParameters</span></span>
<span data-ttu-id="d0854-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0854-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0854-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0854-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0854-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0854-147">INPUTS</span></span>

### <span data-ttu-id="d0854-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0854-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="d0854-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d0854-149">System.String</span></span>

### <span data-ttu-id="d0854-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d0854-150">System.Int32</span></span>

### <span data-ttu-id="d0854-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0854-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d0854-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0854-152">OUTPUTS</span></span>

### <span data-ttu-id="d0854-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0854-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d0854-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0854-154">NOTES</span></span>

## <span data-ttu-id="d0854-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0854-155">RELATED LINKS</span></span>

[<span data-ttu-id="d0854-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0854-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d0854-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0854-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0854-158">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0854-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0854-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0854-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0854-160">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0854-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="d0854-161">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0854-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


