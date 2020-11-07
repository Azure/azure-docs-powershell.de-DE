---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6a699907b70256995973bfdbde4e11b08c594669
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841823"
---
# <span data-ttu-id="d7710-101">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7710-101">Add-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d7710-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7710-102">SYNOPSIS</span></span>
<span data-ttu-id="d7710-103">Fügt eine eingehende NAT-Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="d7710-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

## <span data-ttu-id="d7710-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7710-104">SYNTAX</span></span>

### <span data-ttu-id="d7710-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7710-105">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7710-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d7710-106">SetByResource</span></span>
```
Add-AzLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7710-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7710-107">DESCRIPTION</span></span>
<span data-ttu-id="d7710-108">Mit dem Cmdlet **Add-AzLoadBalancerInboundNatRuleConfig** wird eine eingehende NAT-Regelkonfiguration (Netzwerkadressübersetzung) zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d7710-108">The **Add-AzLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="d7710-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7710-109">EXAMPLES</span></span>

### <span data-ttu-id="d7710-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="d7710-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="d7710-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyloadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="d7710-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="d7710-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d7710-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="d7710-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7710-113">PARAMETERS</span></span>

### <span data-ttu-id="d7710-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d7710-114">-BackendPort</span></span>
<span data-ttu-id="d7710-115">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d7710-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d7710-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7710-116">-DefaultProfile</span></span>
<span data-ttu-id="d7710-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7710-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7710-118">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d7710-118">-EnableFloatingIP</span></span>
<span data-ttu-id="d7710-119">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d7710-119">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="d7710-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7710-120">-FrontendIpConfiguration</span></span>
<span data-ttu-id="d7710-121">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7710-121">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

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

### <span data-ttu-id="d7710-122">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d7710-122">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="d7710-123">Gibt eine ID für die Konfiguration einer Front-End-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="d7710-123">Specifies an ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="d7710-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="d7710-124">-FrontendPort</span></span>
<span data-ttu-id="d7710-125">Gibt den Front-End-Port an, der einer Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7710-125">Specifies the front-end port that is matched by a rule configuration.</span></span>

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

### <span data-ttu-id="d7710-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d7710-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d7710-127">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="d7710-127">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="d7710-128">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7710-128">-LoadBalancer</span></span>
<span data-ttu-id="d7710-129">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d7710-129">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="d7710-130">Dieses Cmdlet fügt dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d7710-130">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7710-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d7710-131">-Name</span></span>
<span data-ttu-id="d7710-132">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7710-132">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="d7710-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d7710-133">-Protocol</span></span>
<span data-ttu-id="d7710-134">Gibt das Protokoll an, das einer eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7710-134">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="d7710-135">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="d7710-135">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="d7710-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7710-136">CommonParameters</span></span>
<span data-ttu-id="d7710-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7710-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7710-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7710-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7710-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7710-139">INPUTS</span></span>

### <span data-ttu-id="d7710-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7710-140">PSLoadBalancer</span></span>
<span data-ttu-id="d7710-141">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7710-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d7710-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7710-142">OUTPUTS</span></span>

### <span data-ttu-id="d7710-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7710-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d7710-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7710-144">NOTES</span></span>

## <span data-ttu-id="d7710-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7710-145">RELATED LINKS</span></span>

[<span data-ttu-id="d7710-146">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7710-146">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d7710-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7710-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d7710-148">Neu – AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7710-148">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d7710-149">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7710-149">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d7710-150">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d7710-150">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="d7710-151">Satz-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7710-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


