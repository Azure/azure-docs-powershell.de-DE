---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: c8de559b6a2b6da9212cb6d9e2607392cf787bf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843632"
---
# <span data-ttu-id="8d1c4-101">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d1c4-101">Set-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8d1c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1c4-103">Legt eine eingehende NAT-Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8d1c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d1c4-104">SYNTAX</span></span>

### <span data-ttu-id="8d1c4-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d1c4-105">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d1c4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8d1c4-106">SetByResource</span></span>
```
Set-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d1c4-107">DESCRIPTION</span></span>
<span data-ttu-id="8d1c4-108">Das Cmdlet " **Set-AzLoadBalancerInboundNatRuleConfig** " legt eine eingehende NAT-Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-108">The **Set-AzLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8d1c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d1c4-109">EXAMPLES</span></span>

### <span data-ttu-id="8d1c4-110">Beispiel 1: Ändern der Konfiguration der eingehenden NAT-Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="8d1c4-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="8d1c4-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="8d1c4-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="8d1c4-113">Der dritte Befehl übergibt das Load Balancer an "AzLoadBalancerInboundNatRuleConfig", wodurch die eingehende NAT **-** Regelkonfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-113">The third command passes the load balancer to **Set-AzLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="8d1c4-114">Beachten Sie, dass die Regelkonfiguration so festgesetzt wurde, dass keine unverankerte IP-Adresse aktiviert wurde, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="8d1c4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d1c4-115">PARAMETERS</span></span>

### <span data-ttu-id="8d1c4-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8d1c4-116">-BackendPort</span></span>
<span data-ttu-id="8d1c4-117">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="8d1c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1c4-118">-DefaultProfile</span></span>
<span data-ttu-id="8d1c4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d1c4-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8d1c4-120">-EnableFloatingIP</span></span>
<span data-ttu-id="8d1c4-121">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8d1c4-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d1c4-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8d1c4-123">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="8d1c4-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8d1c4-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8d1c4-125">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8d1c4-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8d1c4-126">-FrontendPort</span></span>
<span data-ttu-id="8d1c4-127">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8d1c4-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8d1c4-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8d1c4-129">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8d1c4-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d1c4-130">-LoadBalancer</span></span>
<span data-ttu-id="8d1c4-131">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-131">Specifies a load balancer.</span></span>
<span data-ttu-id="8d1c4-132">Mit diesem Cmdlet wird eine eingehende NAT-Regelkonfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d1c4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="8d1c4-133">-Name</span></span>
<span data-ttu-id="8d1c4-134">Gibt den Namen einer eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="8d1c4-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8d1c4-135">-Protocol</span></span>
<span data-ttu-id="8d1c4-136">Gibt das Protokoll an, das einer eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="8d1c4-137">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d1c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1c4-138">CommonParameters</span></span>
<span data-ttu-id="8d1c4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1c4-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1c4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1c4-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d1c4-141">INPUTS</span></span>

### <span data-ttu-id="8d1c4-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d1c4-142">PSLoadBalancer</span></span>
<span data-ttu-id="8d1c4-143">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d1c4-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="8d1c4-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d1c4-144">OUTPUTS</span></span>

### <span data-ttu-id="8d1c4-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d1c4-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8d1c4-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d1c4-146">NOTES</span></span>

## <span data-ttu-id="8d1c4-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d1c4-147">RELATED LINKS</span></span>

[<span data-ttu-id="8d1c4-148">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d1c4-148">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8d1c4-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8d1c4-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8d1c4-150">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d1c4-150">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8d1c4-151">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d1c4-151">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8d1c4-152">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8d1c4-152">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)


