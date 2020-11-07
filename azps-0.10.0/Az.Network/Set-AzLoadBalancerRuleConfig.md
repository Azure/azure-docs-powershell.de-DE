---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2638B226-B974-43B6-ACC2-D67573CF6B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: f566c2b9ac771071a9eb72673edb7e5218656c9b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843619"
---
# <span data-ttu-id="477a6-101">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-101">Set-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="477a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="477a6-102">SYNOPSIS</span></span>
<span data-ttu-id="477a6-103">Legt den Zielstatus für eine Load Balancer-Regelkonfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="477a6-103">Sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="477a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="477a6-104">SYNTAX</span></span>

### <span data-ttu-id="477a6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="477a6-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477a6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="477a6-106">SetByResource</span></span>
```
Set-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="477a6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="477a6-107">DESCRIPTION</span></span>
<span data-ttu-id="477a6-108">Das Cmdlet " **Set-AzLoadBalancerRuleConfig** " legt den Zielstatus für eine Load Balancer-Regelkonfiguration fest.</span><span class="sxs-lookup"><span data-stu-id="477a6-108">The **Set-AzLoadBalancerRuleConfig** cmdlet sets the goal state for a load balancer rule configuration.</span></span>

## <span data-ttu-id="477a6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="477a6-109">EXAMPLES</span></span>

### <span data-ttu-id="477a6-110">Beispiel 1: Ändern einer Lastenausgleichs Regel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="477a6-110">Example 1: Modify a load balancing rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="477a6-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="477a6-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="477a6-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerRuleConfig zu übergeben, wodurch eine Regel mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="477a6-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerRuleConfig, which adds a rule named NewRule to it.</span></span>

<span data-ttu-id="477a6-113">Der dritte Befehl übergibt das Load Balancer an **Set-AzLoadBalancerRuleConfig** , wodurch die neue Regelkonfiguration festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="477a6-113">The third command passes the load balancer to **Set-AzLoadBalancerRuleConfig** , which sets the new rule configuration.</span></span>
<span data-ttu-id="477a6-114">Beachten Sie, dass die Konfiguration keine unverankerte IP-Adresse aktiviert, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="477a6-114">Note that the configuration does not enable a floating IP address, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="477a6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="477a6-115">PARAMETERS</span></span>

### <span data-ttu-id="477a6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="477a6-116">-BackendAddressPool</span></span>
<span data-ttu-id="477a6-117">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regel zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="477a6-117">Specifies a **BackendAddressPool** object to associate with a load balancer rule.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="477a6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="477a6-119">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="477a6-119">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-120">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="477a6-120">-BackendPort</span></span>
<span data-ttu-id="477a6-121">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="477a6-121">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477a6-122">-DefaultProfile</span></span>
<span data-ttu-id="477a6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="477a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-124">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="477a6-124">-DisableOutboundSNAT</span></span>
<span data-ttu-id="477a6-125">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="477a6-125">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-126">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="477a6-126">-EnableFloatingIP</span></span>
<span data-ttu-id="477a6-127">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="477a6-127">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-128">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="477a6-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="477a6-129">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="477a6-129">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-130">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="477a6-130">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="477a6-131">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="477a6-131">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-132">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="477a6-132">-FrontendPort</span></span>
<span data-ttu-id="477a6-133">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="477a6-133">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-134">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="477a6-134">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="477a6-135">Gibt die Zeitdauer in Minuten an, für die der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="477a6-135">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-136">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="477a6-136">-LoadBalancer</span></span>
<span data-ttu-id="477a6-137">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="477a6-137">Specifies a load balancer.</span></span>
<span data-ttu-id="477a6-138">Mit diesem Cmdlet wird die Zielzustands Regelkonfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="477a6-138">This cmdlet sets the goal state rule configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-139">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="477a6-139">-LoadDistribution</span></span>
<span data-ttu-id="477a6-140">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="477a6-140">Specifies a load distribution.</span></span>
<span data-ttu-id="477a6-141">Die zulässigen Werte für diesen Parameter sind: SourceIP und SourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="477a6-141">The acceptable values for this parameter are: SourceIP and SourceIPProtocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-142">-Name</span><span class="sxs-lookup"><span data-stu-id="477a6-142">-Name</span></span>
<span data-ttu-id="477a6-143">Gibt den Namen eines Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="477a6-143">Specifies the name of a load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-144">-Sonde</span><span class="sxs-lookup"><span data-stu-id="477a6-144">-Probe</span></span>
<span data-ttu-id="477a6-145">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="477a6-145">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-146">-Sonde</span><span class="sxs-lookup"><span data-stu-id="477a6-146">-ProbeId</span></span>
<span data-ttu-id="477a6-147">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="477a6-147">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-148">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="477a6-148">-Protocol</span></span>
<span data-ttu-id="477a6-149">Gibt das Protokoll an, das mit einer Load Balancer-Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="477a6-149">Specifies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="477a6-150">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="477a6-150">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="477a6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477a6-151">CommonParameters</span></span>
<span data-ttu-id="477a6-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477a6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477a6-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477a6-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477a6-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="477a6-154">INPUTS</span></span>

### <span data-ttu-id="477a6-155">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="477a6-155">PSLoadBalancer</span></span>
<span data-ttu-id="477a6-156">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="477a6-156">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="477a6-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="477a6-157">OUTPUTS</span></span>

### <span data-ttu-id="477a6-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="477a6-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="477a6-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="477a6-159">NOTES</span></span>

## <span data-ttu-id="477a6-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="477a6-160">RELATED LINKS</span></span>

[<span data-ttu-id="477a6-161">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-161">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="477a6-162">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-162">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="477a6-163">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-163">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="477a6-164">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-164">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="477a6-165">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="477a6-165">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)


