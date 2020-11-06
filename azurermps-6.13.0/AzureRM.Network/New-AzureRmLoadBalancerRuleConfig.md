---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 871982993492ba8eb06d818759e31d3c3500c1d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495898"
---
# <span data-ttu-id="c8b14-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8b14-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c8b14-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8b14-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b14-103">Erstellt eine Regelkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="c8b14-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8b14-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b14-104">SYNTAX</span></span>

### <span data-ttu-id="c8b14-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8b14-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b14-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c8b14-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-Protocol <String>] [-LoadDistribution <String>]
 [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-DisableOutboundSNAT] [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8b14-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8b14-107">DESCRIPTION</span></span>
<span data-ttu-id="c8b14-108">Das Cmdlet **New-AzureRmLoadBalancerRuleConfig** erstellt eine Regelkonfiguration für ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="c8b14-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c8b14-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8b14-109">EXAMPLES</span></span>

### <span data-ttu-id="c8b14-110">1: Erstellen einer Regelkonfiguration für ein Azure Load Balancer</span><span class="sxs-lookup"><span data-stu-id="c8b14-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
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

<span data-ttu-id="c8b14-111">Die ersten drei Befehle richten eine öffentliche IP-Adresse, ein Front-End und eine Sonde für die Regelkonfiguration im Befehl Forth ein.</span><span class="sxs-lookup"><span data-stu-id="c8b14-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="c8b14-112">Der Befehl Forth erstellt eine neue Regel namens MyLBrule mit bestimmten Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c8b14-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="c8b14-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b14-113">PARAMETERS</span></span>

### <span data-ttu-id="c8b14-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c8b14-114">-BackendAddressPool</span></span>
<span data-ttu-id="c8b14-115">Gibt ein **BackendAddressPool** -Objekt an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8b14-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c8b14-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="c8b14-117">Gibt die ID eines **BackendAddressPool** -Objekts an, das einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8b14-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c8b14-118">-BackendPort</span></span>
<span data-ttu-id="c8b14-119">Gibt den Back-End-Port für Datenverkehr an, der von dieser Load Balancer-Regelkonfiguration zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c8b14-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b14-120">-DefaultProfile</span></span>
<span data-ttu-id="c8b14-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8b14-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8b14-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c8b14-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c8b14-123">Konfiguriert SNAT für die VMs im Back-End-Pool, um die im Frontend der Load-Balancing-Regel angegebene publicIP-Adresse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8b14-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="c8b14-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c8b14-124">-EnableFloatingIP</span></span>
<span data-ttu-id="c8b14-125">Gibt an, dass dieses Cmdlet eine unverankerte IP-Adresse für eine Regelkonfiguration aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c8b14-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-126">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c8b14-126">-EnableTcpReset</span></span>
<span data-ttu-id="c8b14-127">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="c8b14-127">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="c8b14-128">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="c8b14-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c8b14-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8b14-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c8b14-130">Gibt eine Liste der Front-End-IP-Adressen an, die einer Load Balancer-Regelkonfiguration zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c8b14-130">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-131">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c8b14-131">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c8b14-132">Gibt die ID für eine Front-End-IP-Adresskonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c8b14-132">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="c8b14-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c8b14-133">-FrontendPort</span></span>
<span data-ttu-id="c8b14-134">Gibt den Front-End-Port an, der durch eine Load Balancer-Regelkonfiguration abgeglichen wird.</span><span class="sxs-lookup"><span data-stu-id="c8b14-134">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c8b14-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c8b14-136">Gibt den Zeitraum in Minuten an, in dem der Zustand der Konversationen in einem Lastenausgleichsmodul verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="c8b14-136">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c8b14-137">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c8b14-137">-LoadDistribution</span></span>
<span data-ttu-id="c8b14-138">Gibt eine Lastverteilung an.</span><span class="sxs-lookup"><span data-stu-id="c8b14-138">Specifies a load distribution.</span></span>
<span data-ttu-id="c8b14-139">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c8b14-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c8b14-140">Standard</span><span class="sxs-lookup"><span data-stu-id="c8b14-140">Default</span></span>
- <span data-ttu-id="c8b14-141">SourceIP</span><span class="sxs-lookup"><span data-stu-id="c8b14-141">SourceIP</span></span>
- <span data-ttu-id="c8b14-142">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="c8b14-142">SourceIPProtocol</span></span>

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

### <span data-ttu-id="c8b14-143">-Name</span><span class="sxs-lookup"><span data-stu-id="c8b14-143">-Name</span></span>
<span data-ttu-id="c8b14-144">Gibt den Namen der vom Cmdlet erstellten Lastenausgleichs Regel an.</span><span class="sxs-lookup"><span data-stu-id="c8b14-144">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c8b14-145">-Sonde</span><span class="sxs-lookup"><span data-stu-id="c8b14-145">-Probe</span></span>
<span data-ttu-id="c8b14-146">Gibt einen Prüfpunkt an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8b14-146">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b14-147">-Sonde</span><span class="sxs-lookup"><span data-stu-id="c8b14-147">-ProbeId</span></span>
<span data-ttu-id="c8b14-148">Gibt die ID des Prüfpunkts an, der einer Load Balancer-Regelkonfiguration zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8b14-148">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c8b14-149">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c8b14-149">-Protocol</span></span>
<span data-ttu-id="c8b14-150">Gibt das Protokoll an, das mit einer Konfiguration des Lastenausgleichsmoduls übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c8b14-150">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="c8b14-151">Die zulässigen Werte für diesen Parameter lauten: TCP oder UDP.</span><span class="sxs-lookup"><span data-stu-id="c8b14-151">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="c8b14-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8b14-152">-Confirm</span></span>
<span data-ttu-id="c8b14-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8b14-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8b14-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8b14-154">-WhatIf</span></span>
<span data-ttu-id="c8b14-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8b14-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8b14-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8b14-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8b14-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b14-157">CommonParameters</span></span>
<span data-ttu-id="c8b14-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b14-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b14-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b14-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b14-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8b14-160">INPUTS</span></span>

### <span data-ttu-id="c8b14-161">Keine</span><span class="sxs-lookup"><span data-stu-id="c8b14-161">None</span></span>

## <span data-ttu-id="c8b14-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8b14-162">OUTPUTS</span></span>

### <span data-ttu-id="c8b14-163">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="c8b14-163">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="c8b14-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8b14-164">NOTES</span></span>

## <span data-ttu-id="c8b14-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8b14-165">RELATED LINKS</span></span>

[<span data-ttu-id="c8b14-166">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8b14-166">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c8b14-167">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8b14-167">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c8b14-168">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8b14-168">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="c8b14-169">Satz-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8b14-169">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


