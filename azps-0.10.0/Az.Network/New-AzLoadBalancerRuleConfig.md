---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841327"
---
# <span data-ttu-id="8865c-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8865c-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="8865c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8865c-102">SYNOPSIS</span></span>
<span data-ttu-id="8865c-103">Erstellt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="8865c-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="8865c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8865c-104">SYNTAX</span></span>

### <span data-ttu-id="8865c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8865c-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8865c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8865c-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8865c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8865c-107">DESCRIPTION</span></span>
<span data-ttu-id="8865c-108">Das Cmdlet **New-AzLoadBalancerRuleConfig** erstellt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="8865c-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8865c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8865c-109">EXAMPLES</span></span>

### <span data-ttu-id="8865c-110">1: Erstellen einer Regelkonfiguration für ein Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="8865c-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="8865c-111">Die ersten drei Befehle richten eine öffentliche IP-Adresse, ein Front-End und eine Sonde für die Regelkonfiguration im Befehl Forth ein.</span><span class="sxs-lookup"><span data-stu-id="8865c-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="8865c-112">Der Befehl Forth erstellt eine neue Regel namens MyLBrule mit bestimmten Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="8865c-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="8865c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8865c-113">PARAMETERS</span></span>

### <span data-ttu-id="8865c-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8865c-114">-BackendAddressPool</span></span>
<span data-ttu-id="8865c-115">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8865c-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8865c-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="8865c-117">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8865c-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8865c-118">-BackendPort</span></span>
<span data-ttu-id="8865c-119">Gibt den Back-End-Port für Datenverkehr an, der von dieser Load Balancer-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8865c-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8865c-120">-DefaultProfile</span></span>
<span data-ttu-id="8865c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8865c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8865c-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="8865c-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="8865c-123">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8865c-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="8865c-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8865c-124">-EnableFloatingIP</span></span>
<span data-ttu-id="8865c-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8865c-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8865c-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8865c-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8865c-127">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8865c-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8865c-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8865c-129">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="8865c-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8865c-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8865c-130">-FrontendPort</span></span>
<span data-ttu-id="8865c-131">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="8865c-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8865c-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8865c-133">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="8865c-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8865c-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="8865c-134">-LoadDistribution</span></span>
<span data-ttu-id="8865c-135">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="8865c-135">Specifies a load distribution.</span></span>
<span data-ttu-id="8865c-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8865c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8865c-137">Standard</span><span class="sxs-lookup"><span data-stu-id="8865c-137">Default</span></span>
- <span data-ttu-id="8865c-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="8865c-138">SourceIP</span></span>
- <span data-ttu-id="8865c-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="8865c-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="8865c-140">-Name</span><span class="sxs-lookup"><span data-stu-id="8865c-140">-Name</span></span>
<span data-ttu-id="8865c-141">Gibt den Namen der vom Cmdlet erstellten Lastenausgleichs Regel an.</span><span class="sxs-lookup"><span data-stu-id="8865c-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8865c-142">-Sonde</span><span class="sxs-lookup"><span data-stu-id="8865c-142">-Probe</span></span>
<span data-ttu-id="8865c-143">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8865c-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-144">-Sonde</span><span class="sxs-lookup"><span data-stu-id="8865c-144">-ProbeId</span></span>
<span data-ttu-id="8865c-145">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8865c-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8865c-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8865c-146">-Protocol</span></span>
<span data-ttu-id="8865c-147">Gibt das Protokoll an, das mit einer Konfiguration des Lastenausgleichsmoduls übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8865c-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="8865c-148">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="8865c-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="8865c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8865c-149">CommonParameters</span></span>
<span data-ttu-id="8865c-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8865c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8865c-151">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8865c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8865c-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8865c-152">INPUTS</span></span>

## <span data-ttu-id="8865c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8865c-153">OUTPUTS</span></span>

### <span data-ttu-id="8865c-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="8865c-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="8865c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="8865c-155">NOTES</span></span>

## <span data-ttu-id="8865c-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8865c-156">RELATED LINKS</span></span>

[<span data-ttu-id="8865c-157">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8865c-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8865c-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8865c-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8865c-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8865c-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="8865c-160">Satz-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8865c-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


