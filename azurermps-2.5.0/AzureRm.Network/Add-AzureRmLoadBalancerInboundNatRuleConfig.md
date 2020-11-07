---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: 65861e86f0852d0002a7c4aa6f2c7f925eabf5bc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850799"
---
# <span data-ttu-id="ce251-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce251-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="ce251-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce251-102">SYNOPSIS</span></span>
<span data-ttu-id="ce251-103">Fügt eine eingehende NAT-Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="ce251-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce251-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce251-104">SYNTAX</span></span>

### <span data-ttu-id="ce251-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce251-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce251-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ce251-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce251-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce251-107">DESCRIPTION</span></span>
<span data-ttu-id="ce251-108">Mit dem Cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** wird eine eingehende NAT-Regelkonfiguration (Netzwerkadressübersetzung) zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce251-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="ce251-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce251-109">EXAMPLES</span></span>

### <span data-ttu-id="ce251-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="ce251-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="ce251-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyloadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="ce251-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="ce251-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzureRmLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ce251-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="ce251-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce251-113">PARAMETERS</span></span>

### <span data-ttu-id="ce251-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ce251-114">-BackendPort</span></span>
<span data-ttu-id="ce251-115">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="ce251-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ce251-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce251-116">-DefaultProfile</span></span>
<span data-ttu-id="ce251-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce251-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce251-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="ce251-118">-EnableFloatingIP</span></span>
<span data-ttu-id="ce251-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ce251-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="ce251-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce251-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="ce251-121">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce251-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="ce251-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ce251-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="ce251-123">Gibt eine ID für die Konfiguration einer Front-End-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="ce251-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="ce251-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ce251-124">-FrontendPort</span></span>
<span data-ttu-id="ce251-125">Gibt den Front-End-Port an, der einer Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce251-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="ce251-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ce251-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ce251-127">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="ce251-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="ce251-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce251-128">-LoadBalancer</span></span>
<span data-ttu-id="ce251-129">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ce251-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="ce251-130">Dieses Cmdlet fügt dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ce251-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce251-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ce251-131">-Name</span></span>
<span data-ttu-id="ce251-132">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce251-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="ce251-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="ce251-133">-Protocol</span></span>
<span data-ttu-id="ce251-134">Gibt das Protokoll an, das einer eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce251-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="ce251-135">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="ce251-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="ce251-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce251-136">CommonParameters</span></span>
<span data-ttu-id="ce251-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce251-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce251-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce251-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce251-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce251-139">INPUTS</span></span>

### <span data-ttu-id="ce251-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce251-140">PSLoadBalancer</span></span>
<span data-ttu-id="ce251-141">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce251-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ce251-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce251-142">OUTPUTS</span></span>

### <span data-ttu-id="ce251-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce251-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ce251-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce251-144">NOTES</span></span>

## <span data-ttu-id="ce251-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce251-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce251-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce251-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="ce251-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce251-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ce251-148">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce251-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ce251-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce251-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="ce251-150">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ce251-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="ce251-151">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce251-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


