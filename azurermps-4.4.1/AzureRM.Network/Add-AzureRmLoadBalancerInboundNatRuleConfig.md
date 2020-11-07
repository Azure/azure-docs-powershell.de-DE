---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EE8F5D57-1ECE-4F23-9A5B-F226DD2C5ECB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee0a001894570c66145ac7f75d12451df5faaab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663312"
---
# <span data-ttu-id="4260a-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4260a-101">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4260a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4260a-102">SYNOPSIS</span></span>
<span data-ttu-id="4260a-103">Fügt eine eingehende NAT-Regelkonfiguration zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4260a-103">Adds an inbound NAT rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4260a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4260a-104">SYNTAX</span></span>

### <span data-ttu-id="4260a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4260a-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfigurationId <String>] [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>]
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4260a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4260a-106">SetByResource</span></span>
```
Add-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4260a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4260a-107">DESCRIPTION</span></span>
<span data-ttu-id="4260a-108">Mit dem Cmdlet **Add-AzureRmLoadBalancerInboundNatRuleConfig** wird eine eingehende NAT-Regelkonfiguration (Netzwerkadressübersetzung) zu einem Azure Load Balancer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4260a-108">The **Add-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet adds an inbound network address translation (NAT) rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4260a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4260a-109">EXAMPLES</span></span>

### <span data-ttu-id="4260a-110">Beispiel 1: Hinzufügen einer eingehenden NAT-Regelkonfiguration zu einem Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="4260a-110">Example 1: Add an inbound NAT rule configuration to a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewNatRule" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -Protocol "Tcp" -FrontendPort 3350 -BackendPort 3350  -EnableFloatingIP
```

<span data-ttu-id="4260a-111">Der erste Befehl ruft das Lastenausgleichsmodul mit dem Namen MyloadBalancer ab und speichert es dann in der Variablen $SLB.</span><span class="sxs-lookup"><span data-stu-id="4260a-111">The first command gets the load balancer named MyloadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="4260a-112">Der zweite Befehl verwendet den Pipelineoperator, um das Load Balancer in $SLB an **Add-AzureRmLoadBalancerInboundNatRuleConfig** zu übergeben, wodurch dem Lastenausgleichsmodul eine eingehende NAT-Regelkonfiguration hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4260a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerInboundNatRuleConfig** , which adds an inbound NAT rule configuration to the load balancer.</span></span>

## <span data-ttu-id="4260a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4260a-113">PARAMETERS</span></span>

### <span data-ttu-id="4260a-114">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4260a-114">-BackendPort</span></span>
<span data-ttu-id="4260a-115">Gibt den Back-End-Port für Datenverkehr an, der mit einer Regelkonfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4260a-115">Specifies the backend port for traffic matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-116">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4260a-116">-EnableFloatingIP</span></span>
<span data-ttu-id="4260a-117">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4260a-117">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="4260a-118">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4260a-118">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4260a-119">Gibt eine Liste der Front-End-IP-Adressen an, die einer eingehenden NAT-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4260a-119">Specifies a list of front-end IP addresses to associate with an inbound NAT rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-120">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4260a-120">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="4260a-121">Gibt eine ID für die Konfiguration einer Front-End-IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="4260a-121">Specifies an ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4260a-122">-FrontendPort</span></span>
<span data-ttu-id="4260a-123">Gibt den Front-End-Port an, der einer Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4260a-123">Specifies the front-end port that is matched by a rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4260a-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4260a-125">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4260a-125">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4260a-126">-LoadBalancer</span></span>
<span data-ttu-id="4260a-127">Gibt ein **LoadBalancer** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4260a-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4260a-128">Dieses Cmdlet fügt dem Load Balancer eine eingehende NAT-Regelkonfiguration hinzu, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4260a-128">This cmdlet adds an inbound NAT rule configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4260a-129">-Name</span></span>
<span data-ttu-id="4260a-130">Gibt den Namen der eingehenden NAT-Regelkonfiguration an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4260a-130">Specifies the name of the inbound NAT rule configuration to add.</span></span>

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

### <span data-ttu-id="4260a-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4260a-131">-Protocol</span></span>
<span data-ttu-id="4260a-132">Gibt das Protokoll an, das einer eingehenden NAT-Regel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4260a-132">Specifies the protocol that is matched by an inbound NAT rule.</span></span>
<span data-ttu-id="4260a-133">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="4260a-133">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260a-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4260a-134">-DefaultProfile</span></span>
<span data-ttu-id="4260a-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4260a-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4260a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4260a-136">CommonParameters</span></span>
<span data-ttu-id="4260a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4260a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4260a-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4260a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4260a-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4260a-139">INPUTS</span></span>

### <span data-ttu-id="4260a-140">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4260a-140">PSLoadBalancer</span></span>
<span data-ttu-id="4260a-141">Der Parameter "LoadBalancer" akzeptiert den Wert vom Typ "PSLoadBalancer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4260a-141">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4260a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4260a-142">OUTPUTS</span></span>

### <span data-ttu-id="4260a-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4260a-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4260a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="4260a-144">NOTES</span></span>

## <span data-ttu-id="4260a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4260a-145">RELATED LINKS</span></span>

[<span data-ttu-id="4260a-146">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4260a-146">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4260a-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4260a-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4260a-148">Neu – AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4260a-148">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4260a-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4260a-149">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4260a-150">Satz-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4260a-150">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="4260a-151">Satz-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4260a-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


