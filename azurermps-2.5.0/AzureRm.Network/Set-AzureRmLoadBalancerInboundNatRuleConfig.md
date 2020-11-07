---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 87818605-EFA6-422E-9ECD-0A0BF269DCFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: e79ff19e23d7e599dd783e4bb9c4c12d13f943f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850324"
---
# <span data-ttu-id="65352-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65352-101">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="65352-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65352-102">SYNOPSIS</span></span>
<span data-ttu-id="65352-103">Legt eine eingehende NAT-Regelkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="65352-103">Sets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65352-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65352-104">SYNTAX</span></span>

### <span data-ttu-id="65352-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65352-105">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65352-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="65352-106">SetByResource</span></span>
```
Set-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65352-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65352-107">DESCRIPTION</span></span>
<span data-ttu-id="65352-108">Das Cmdlet " **Set-AzureRmLoadBalancerInboundNatRuleConfig** " legt eine eingehende NAT-Regelkonfiguration für ein Azure Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="65352-108">The **Set-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet sets an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="65352-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65352-109">EXAMPLES</span></span>

### <span data-ttu-id="65352-110">Beispiel 1: Ändern der Konfiguration der eingehenden NAT-Regel auf einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="65352-110">Example 1: Modify the inbound NAT rule configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350 -EnableFloatingIP
PS C:\> $slb | Set-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350
```

<span data-ttu-id="65352-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyLoadBalancer ab und speichert es dann in der $SLB-Variablen.</span><span class="sxs-lookup"><span data-stu-id="65352-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="65352-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an Add-AzureRmLoadBalancerInboundNatRuleConfig zu übergeben, wodurch eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="65352-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule configuration to it.</span></span>

<span data-ttu-id="65352-113">Der dritte Befehl übergibt das Load Balancer an "AzureRmLoadBalancerInboundNatRuleConfig", wodurch die eingehende NAT **-** Regelkonfiguration gespeichert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="65352-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerInboundNatRuleConfig** , which saves and updates the inbound NAT rule configuration.</span></span>
<span data-ttu-id="65352-114">Beachten Sie, dass die Regelkonfiguration so festgesetzt wurde, dass keine unverankerte IP-Adresse aktiviert wurde, die vom vorherigen Befehl aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="65352-114">Note that the rule configuration was set without enabling floating IP, which had been enabled by the previous command.</span></span>

## <span data-ttu-id="65352-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="65352-115">PARAMETERS</span></span>

### <span data-ttu-id="65352-116">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="65352-116">-BackendPort</span></span>
<span data-ttu-id="65352-117">Gibt den Back-End-Port für Datenverkehr an, der von dieser Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="65352-117">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="65352-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65352-118">-DefaultProfile</span></span>
<span data-ttu-id="65352-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65352-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65352-120">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="65352-120">-EnableFloatingIP</span></span>
<span data-ttu-id="65352-121">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="65352-121">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="65352-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="65352-122">-FrontendIpConfiguration</span></span>
<span data-ttu-id="65352-123">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65352-123">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="65352-124">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="65352-124">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="65352-125">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="65352-125">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="65352-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="65352-126">-FrontendPort</span></span>
<span data-ttu-id="65352-127">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="65352-127">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="65352-128">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="65352-128">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="65352-129">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="65352-129">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="65352-130">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65352-130">-LoadBalancer</span></span>
<span data-ttu-id="65352-131">Gibt ein Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="65352-131">Specifies a load balancer.</span></span>
<span data-ttu-id="65352-132">Mit diesem Cmdlet wird eine eingehende NAT-Regelkonfiguration für das Load Balancer festgelegt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="65352-132">This cmdlet sets an inbound NAT rule configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="65352-133">-Name</span><span class="sxs-lookup"><span data-stu-id="65352-133">-Name</span></span>
<span data-ttu-id="65352-134">Gibt den Namen einer eingehenden NAT-Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="65352-134">Specifies the name of an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="65352-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="65352-135">-Protocol</span></span>
<span data-ttu-id="65352-136">Gibt das Protokoll an, das einer eingehenden NAT-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65352-136">Specifies the protocol that is matched by an inbound NAT rule configuration.</span></span>
<span data-ttu-id="65352-137">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="65352-137">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="65352-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65352-138">CommonParameters</span></span>
<span data-ttu-id="65352-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65352-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65352-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65352-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65352-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65352-141">INPUTS</span></span>

### <span data-ttu-id="65352-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65352-142">PSLoadBalancer</span></span>
<span data-ttu-id="65352-143">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="65352-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="65352-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65352-144">OUTPUTS</span></span>

### <span data-ttu-id="65352-145">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65352-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="65352-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="65352-146">NOTES</span></span>

## <span data-ttu-id="65352-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65352-147">RELATED LINKS</span></span>

[<span data-ttu-id="65352-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65352-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="65352-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="65352-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="65352-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65352-150">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="65352-151">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65352-151">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="65352-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="65352-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)


