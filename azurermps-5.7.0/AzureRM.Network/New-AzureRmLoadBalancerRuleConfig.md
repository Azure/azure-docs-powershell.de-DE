---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 076672dc8cb90126782b54c13ee99b41dff4ccbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663216"
---
# <span data-ttu-id="c7f37-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7f37-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c7f37-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7f37-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f37-103">Erstellt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="c7f37-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f37-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7f37-104">SYNTAX</span></span>

### <span data-ttu-id="c7f37-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f37-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f37-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c7f37-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f37-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7f37-107">DESCRIPTION</span></span>
<span data-ttu-id="c7f37-108">Das Cmdlet **New-AzureRmLoadBalancerRuleConfig** erstellt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="c7f37-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c7f37-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7f37-109">EXAMPLES</span></span>

### <span data-ttu-id="c7f37-110">1: Erstellen einer Regelkonfiguration für ein Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="c7f37-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="c7f37-111">Die ersten drei Befehle richten eine öffentliche IP-Adresse, ein Front-End und eine Sonde für die Regelkonfiguration im Befehl Forth ein.</span><span class="sxs-lookup"><span data-stu-id="c7f37-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="c7f37-112">Der Befehl Forth erstellt eine neue Regel namens MyLBrule mit bestimmten Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c7f37-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="c7f37-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7f37-113">PARAMETERS</span></span>

### <span data-ttu-id="c7f37-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c7f37-114">-BackendAddressPool</span></span>
<span data-ttu-id="c7f37-115">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7f37-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c7f37-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="c7f37-117">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7f37-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c7f37-118">-BackendPort</span></span>
<span data-ttu-id="c7f37-119">Gibt den Back-End-Port für Datenverkehr an, der von dieser Load Balancer-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c7f37-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f37-120">-DefaultProfile</span></span>
<span data-ttu-id="c7f37-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7f37-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f37-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c7f37-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c7f37-123">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7f37-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c7f37-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c7f37-124">-EnableFloatingIP</span></span>
<span data-ttu-id="c7f37-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7f37-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7f37-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c7f37-127">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7f37-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c7f37-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c7f37-129">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c7f37-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c7f37-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c7f37-130">-FrontendPort</span></span>
<span data-ttu-id="c7f37-131">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="c7f37-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c7f37-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c7f37-133">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c7f37-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c7f37-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c7f37-134">-LoadDistribution</span></span>
<span data-ttu-id="c7f37-135">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="c7f37-135">Specifies a load distribution.</span></span>
<span data-ttu-id="c7f37-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7f37-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7f37-137">Standard</span><span class="sxs-lookup"><span data-stu-id="c7f37-137">Default</span></span>
- <span data-ttu-id="c7f37-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="c7f37-138">SourceIP</span></span>
- <span data-ttu-id="c7f37-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="c7f37-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="c7f37-140">-Name</span><span class="sxs-lookup"><span data-stu-id="c7f37-140">-Name</span></span>
<span data-ttu-id="c7f37-141">Gibt den Namen der vom Cmdlet erstellten Lastenausgleichs Regel an.</span><span class="sxs-lookup"><span data-stu-id="c7f37-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c7f37-142">-Sonde</span><span class="sxs-lookup"><span data-stu-id="c7f37-142">-Probe</span></span>
<span data-ttu-id="c7f37-143">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7f37-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-144">-Sonde</span><span class="sxs-lookup"><span data-stu-id="c7f37-144">-ProbeId</span></span>
<span data-ttu-id="c7f37-145">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7f37-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c7f37-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c7f37-146">-Protocol</span></span>
<span data-ttu-id="c7f37-147">Gibt das Protokoll an, das mit einer Konfiguration des Lastenausgleichsmoduls übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c7f37-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="c7f37-148">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="c7f37-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c7f37-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f37-149">CommonParameters</span></span>
<span data-ttu-id="c7f37-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f37-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f37-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f37-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f37-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7f37-152">INPUTS</span></span>

### <span data-ttu-id="c7f37-153">Keine</span><span class="sxs-lookup"><span data-stu-id="c7f37-153">None</span></span>
<span data-ttu-id="c7f37-154">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c7f37-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7f37-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7f37-155">OUTPUTS</span></span>

### <span data-ttu-id="c7f37-156">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="c7f37-156">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="c7f37-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7f37-157">NOTES</span></span>

## <span data-ttu-id="c7f37-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7f37-158">RELATED LINKS</span></span>

[<span data-ttu-id="c7f37-159">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7f37-159">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7f37-160">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7f37-160">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7f37-161">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7f37-161">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c7f37-162">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7f37-162">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


