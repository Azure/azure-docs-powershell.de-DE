---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c7d0d5879b4c0ca7ee92a9f22d062241e1cb89a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495850"
---
# <span data-ttu-id="2ba79-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ba79-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2ba79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ba79-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba79-103">Legt eine eingehende NAT-Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="2ba79-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ba79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba79-104">SYNTAX</span></span>

### <span data-ttu-id="2ba79-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ba79-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba79-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba79-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba79-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ba79-107">DESCRIPTION</span></span>
<span data-ttu-id="2ba79-108">Das Cmdlet " **Set-AzureRmLoadBalancerInboundNatRuleConfig** " legt eine eingehende NAT-Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="2ba79-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2ba79-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ba79-109">EXAMPLES</span></span>

### <span data-ttu-id="2ba79-110">Beispiel 1: Ändern der Konfiguration der eingehenden NAT-Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="2ba79-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="2ba79-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2ba79-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="2ba79-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>
<span data-ttu-id="2ba79-113">Der dritte Befehl übergibt das Load Balancer an "AzureRmLoadBalancerInboundNatRuleConfig", wodurch die eingehende NAT **-** Regelkonfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="2ba79-114">Beachten Sie, dass die Regelkonfiguration so festgesetzt wurde, dass keine unverankerte IP-Adresse aktiviert wurde, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="2ba79-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="2ba79-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ba79-115">PARAMETERS</span></span>

### <span data-ttu-id="2ba79-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="2ba79-116">-BackendPort</span></span>
<span data-ttu-id="2ba79-117">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="2ba79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba79-118">-DefaultProfile</span></span>
<span data-ttu-id="2ba79-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ba79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba79-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="2ba79-120">-EnableFloatingIP</span></span>
<span data-ttu-id="2ba79-121">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2ba79-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="2ba79-122">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="2ba79-122">-EnableTcpReset</span></span>
<span data-ttu-id="2ba79-123">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="2ba79-123">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="2ba79-124">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="2ba79-124">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="2ba79-125">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ba79-125">-FrontendIpConfiguration</span></span>
<span data-ttu-id="2ba79-126">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ba79-126">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="2ba79-127">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2ba79-127">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="2ba79-128">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="2ba79-128">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="2ba79-129">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="2ba79-129">-FrontendPort</span></span>
<span data-ttu-id="2ba79-130">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-130">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="2ba79-131">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2ba79-131">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="2ba79-132">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-132">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="2ba79-133">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ba79-133">-LoadBalancer</span></span>
<span data-ttu-id="2ba79-134">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="2ba79-134">Specifies a load balancer.</span></span>
<span data-ttu-id="2ba79-135">Mit diesem Cmdlet wird eine eingehende NAT-Regelkonfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="2ba79-135">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2ba79-136">-Name</span><span class="sxs-lookup"><span data-stu-id="2ba79-136">-Name</span></span>
<span data-ttu-id="2ba79-137">Gibt den Namen einer eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="2ba79-137">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="2ba79-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2ba79-138">-Protocol</span></span>
<span data-ttu-id="2ba79-139">Gibt das Protokoll an, das einer eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2ba79-139">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="2ba79-140">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="2ba79-140">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="2ba79-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ba79-141">-Confirm</span></span>
<span data-ttu-id="2ba79-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ba79-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba79-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba79-143">-WhatIf</span></span>
<span data-ttu-id="2ba79-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ba79-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ba79-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ba79-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba79-146">CommonParameters</span></span>
<span data-ttu-id="2ba79-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ba79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba79-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba79-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba79-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ba79-149">INPUTS</span></span>

### <span data-ttu-id="2ba79-150">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ba79-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="2ba79-151">Parameter: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ba79-151">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="2ba79-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ba79-152">OUTPUTS</span></span>

### <span data-ttu-id="2ba79-153">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ba79-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2ba79-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ba79-154">NOTES</span></span>

## <span data-ttu-id="2ba79-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ba79-155">RELATED LINKS</span></span>

[<span data-ttu-id="2ba79-156">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ba79-156">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2ba79-157">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2ba79-157">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2ba79-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ba79-158">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2ba79-159">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ba79-159">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2ba79-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2ba79-160">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


