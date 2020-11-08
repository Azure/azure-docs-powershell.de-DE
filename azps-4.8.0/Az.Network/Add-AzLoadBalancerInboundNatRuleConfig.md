---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 3c0ce9d5038cb63c70d8c0c5f093077dedfb9ad4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166312"
---
# <span data-ttu-id="9be20-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9be20-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="9be20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9be20-102">SYNOPSIS</span></span>
<span data-ttu-id="9be20-103">Fügt eine eingehende NAT-Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="9be20-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="9be20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9be20-104">SYNTAX</span></span>

### <span data-ttu-id="9be20-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="9be20-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9be20-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9be20-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9be20-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9be20-107">DESCRIPTION</span></span>
<span data-ttu-id="9be20-108">Mit dem Cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** wird eine eingehende NAT-Regelkonfiguration (Netzwerkadressübersetzung) zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9be20-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="9be20-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9be20-109">EXAMPLES</span></span>

### <span data-ttu-id="9be20-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="9be20-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="9be20-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyloadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="9be20-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="9be20-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9be20-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="9be20-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9be20-113">PARAMETERS</span></span>

### <span data-ttu-id="9be20-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="9be20-114">-BackendPort</span></span>
<span data-ttu-id="9be20-115">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9be20-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="9be20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be20-116">-DefaultProfile</span></span>
<span data-ttu-id="9be20-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9be20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9be20-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="9be20-118">-EnableFloatingIP</span></span>
<span data-ttu-id="9be20-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9be20-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="9be20-120">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="9be20-120">-EnableTcpReset</span></span>
<span data-ttu-id="9be20-121">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="9be20-121">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="9be20-122">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="9be20-122">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="9be20-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9be20-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="9be20-124">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9be20-124">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="9be20-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9be20-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="9be20-126">Gibt eine ID für die Konfiguration einer Front-End-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="9be20-126">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="9be20-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9be20-127">-FrontendPort</span></span>
<span data-ttu-id="9be20-128">Gibt den Front-End-Port an, der einer Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9be20-128">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="9be20-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="9be20-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9be20-130">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9be20-130">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="9be20-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9be20-131">-LoadBalancer</span></span>
<span data-ttu-id="9be20-132">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="9be20-132">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="9be20-133">Dieses Cmdlet fügt dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9be20-133">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="9be20-134">-Name</span><span class="sxs-lookup"><span data-stu-id="9be20-134">-Name</span></span>
<span data-ttu-id="9be20-135">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9be20-135">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="9be20-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="9be20-136">-Protocol</span></span>
<span data-ttu-id="9be20-137">Gibt das Protokoll an, das einer eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9be20-137">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="9be20-138">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="9be20-138">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="9be20-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9be20-139">-Confirm</span></span>
<span data-ttu-id="9be20-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9be20-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9be20-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9be20-141">-WhatIf</span></span>
<span data-ttu-id="9be20-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9be20-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9be20-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9be20-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9be20-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be20-144">CommonParameters</span></span>
<span data-ttu-id="9be20-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be20-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be20-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be20-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be20-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9be20-147">INPUTS</span></span>

### <span data-ttu-id="9be20-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9be20-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="9be20-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9be20-149">System.String</span></span>

### <span data-ttu-id="9be20-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9be20-150">System.Int32</span></span>

### <span data-ttu-id="9be20-151">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9be20-151">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="9be20-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9be20-152">OUTPUTS</span></span>

### <span data-ttu-id="9be20-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9be20-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9be20-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="9be20-154">NOTES</span></span>

## <span data-ttu-id="9be20-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9be20-155">RELATED LINKS</span></span>

[<span data-ttu-id="9be20-156">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9be20-156">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="9be20-157">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9be20-157">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9be20-158">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9be20-158">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9be20-159">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9be20-159">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="9be20-160">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9be20-160">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="9be20-161">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9be20-161">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


