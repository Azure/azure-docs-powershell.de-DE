---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2AE5E9B8-7344-407B-9317-47709F10FCD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 52e1759f82ba6663215907a93f89f562df1b6afa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841811"
---
# <span data-ttu-id="63310-101">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63310-101">Add-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="63310-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63310-102">SYNOPSIS</span></span>
<span data-ttu-id="63310-103">Fügt eine Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="63310-103">Adds a rule configuration to a load balancer.</span></span>

## <span data-ttu-id="63310-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63310-104">SYNTAX</span></span>

### <span data-ttu-id="63310-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="63310-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-BackendAddressPoolId <String>] [-ProbeId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63310-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="63310-106">SetByResource</span></span>
```
Add-AzLoadBalancerRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-BackendAddressPool <PSBackendAddressPool>]
 [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP] [-DisableOutboundSNAT]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63310-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63310-107">DESCRIPTION</span></span>
<span data-ttu-id="63310-108">Mit dem Cmdlet **Add-AzLoadBalancerRuleConfig** wird eine Regelkonfiguration zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63310-108">The **Add-AzLoadBalancerRuleConfig** cmdlet adds a rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="63310-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63310-109">EXAMPLES</span></span>

### <span data-ttu-id="63310-110">Beispiel 1: Hinzufügen einer Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="63310-110">Example 1: Add a rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerRuleConfig -Name "NewRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
```

<span data-ttu-id="63310-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="63310-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="63310-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzLoadBalancerRuleConfig** zu übergeben, wodurch die Regelkonfiguration mit dem Namen "Neuregelung" hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="63310-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerRuleConfig** , which adds the rule configuration named NewRule.</span></span>

## <span data-ttu-id="63310-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="63310-113">PARAMETERS</span></span>

### <span data-ttu-id="63310-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="63310-114">-BackendAddressPool</span></span>
<span data-ttu-id="63310-115">Gibt den Back-End-Adresspool an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63310-115">Specifies the backend address pool to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="63310-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="63310-117">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63310-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="63310-118">-BackendPort</span></span>
<span data-ttu-id="63310-119">Gibt den Back-End-Port für Datenverkehr an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="63310-119">Specifies the backend port for traffic that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63310-120">-DefaultProfile</span></span>
<span data-ttu-id="63310-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63310-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63310-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="63310-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="63310-123">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="63310-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="63310-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="63310-124">-EnableFloatingIP</span></span>
<span data-ttu-id="63310-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="63310-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="63310-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="63310-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="63310-127">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63310-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="63310-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="63310-129">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="63310-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="63310-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="63310-130">-FrontendPort</span></span>
<span data-ttu-id="63310-131">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="63310-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="63310-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="63310-133">Gibt an, wie lange in Minuten der Status der Konversationen im Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="63310-133">Specifies the length of time, in minutes, that the state of conversations is maintained in the load balancer.</span></span>

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

### <span data-ttu-id="63310-134">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63310-134">-LoadBalancer</span></span>
<span data-ttu-id="63310-135">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="63310-135">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="63310-136">Dieses Cmdlet fügt dem Load Balancer eine Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="63310-136">This cmdlet adds a rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="63310-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="63310-137">-LoadDistribution</span></span>
<span data-ttu-id="63310-138">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="63310-138">Specifies a load distribution.</span></span>

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

### <span data-ttu-id="63310-139">-Name</span><span class="sxs-lookup"><span data-stu-id="63310-139">-Name</span></span>
<span data-ttu-id="63310-140">Gibt den Namen der Load Balancer-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="63310-140">Specifies the name of the load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-141">-Sonde</span><span class="sxs-lookup"><span data-stu-id="63310-141">-Probe</span></span>
<span data-ttu-id="63310-142">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63310-142">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-143">-Sonde</span><span class="sxs-lookup"><span data-stu-id="63310-143">-ProbeId</span></span>
<span data-ttu-id="63310-144">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="63310-144">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="63310-145">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="63310-145">-Protocol</span></span>
<span data-ttu-id="63310-146">Gibt an Sie das Protokoll, das mit einer Load Balancer-Regel übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="63310-146">Specfies the protocol that is matched by a load balancer rule.</span></span>
<span data-ttu-id="63310-147">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="63310-147">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="63310-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63310-148">CommonParameters</span></span>
<span data-ttu-id="63310-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63310-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63310-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63310-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63310-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63310-151">INPUTS</span></span>

### <span data-ttu-id="63310-152">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63310-152">PSLoadBalancer</span></span>
<span data-ttu-id="63310-153">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="63310-153">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="63310-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63310-154">OUTPUTS</span></span>

### <span data-ttu-id="63310-155">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63310-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="63310-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="63310-156">NOTES</span></span>

## <span data-ttu-id="63310-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63310-157">RELATED LINKS</span></span>

[<span data-ttu-id="63310-158">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="63310-158">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="63310-159">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63310-159">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="63310-160">Neu – AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63310-160">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="63310-161">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63310-161">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="63310-162">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="63310-162">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


