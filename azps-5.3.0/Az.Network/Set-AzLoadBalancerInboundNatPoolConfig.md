---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: ac57c65f670734be6638e71179147490b41085f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473389"
---
# <span data-ttu-id="df927-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="df927-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="df927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df927-102">SYNOPSIS</span></span>
<span data-ttu-id="df927-103">Legt eine eingehende Konfiguration des NAT-Pools für einen Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="df927-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="df927-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df927-104">SYNTAX</span></span>

### <span data-ttu-id="df927-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="df927-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df927-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df927-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df927-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df927-107">DESCRIPTION</span></span>
<span data-ttu-id="df927-108">Das **Cmdlet "Set-AzLoadBalancerInboundNatPoolConfig"** legt eine Konfiguration des eingehenden NAT-Pools für einen Lastenausgleich fest.</span><span class="sxs-lookup"><span data-stu-id="df927-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="df927-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df927-109">EXAMPLES</span></span>

### <span data-ttu-id="df927-110">Beispiel 1: Festlegen</span><span class="sxs-lookup"><span data-stu-id="df927-110">Example 1: Set</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
PS C:\> $slb | Set-AzLoadBalancer
```

## <span data-ttu-id="df927-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df927-111">PARAMETERS</span></span>

### <span data-ttu-id="df927-112">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="df927-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df927-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df927-113">-DefaultProfile</span></span>
<span data-ttu-id="df927-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df927-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df927-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="df927-115">-EnableFloatingIP</span></span>
<span data-ttu-id="df927-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-Verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="df927-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="df927-117">Diese Einstellung ist erforderlich, wenn Sie SQL "AlwaysOn-Verfügbarkeitsgruppen" auf einem SQL verwenden.</span><span class="sxs-lookup"><span data-stu-id="df927-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="df927-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="df927-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="df927-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="df927-119">-EnableTcpReset</span></span>
<span data-ttu-id="df927-120">Empfangen des bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="df927-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="df927-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df927-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="df927-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="df927-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="df927-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="df927-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="df927-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="df927-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df927-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="df927-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df927-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="df927-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="df927-127">Der Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="df927-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="df927-128">Der Wert kann zwischen 4 und 30 Minuten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="df927-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="df927-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="df927-129">The default value is 4 minutes.</span></span> <span data-ttu-id="df927-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="df927-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="df927-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df927-131">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df927-132">-Name</span><span class="sxs-lookup"><span data-stu-id="df927-132">-Name</span></span>
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

### <span data-ttu-id="df927-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="df927-133">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df927-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df927-134">-Confirm</span></span>
<span data-ttu-id="df927-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df927-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df927-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df927-136">-WhatIf</span></span>
<span data-ttu-id="df927-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df927-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df927-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df927-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df927-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df927-139">CommonParameters</span></span>
<span data-ttu-id="df927-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df927-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df927-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df927-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df927-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df927-142">INPUTS</span></span>

### <span data-ttu-id="df927-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df927-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="df927-144">System.String</span><span class="sxs-lookup"><span data-stu-id="df927-144">System.String</span></span>

### <span data-ttu-id="df927-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="df927-145">System.Int32</span></span>

### <span data-ttu-id="df927-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="df927-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="df927-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df927-147">OUTPUTS</span></span>

### <span data-ttu-id="df927-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="df927-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="df927-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df927-149">NOTES</span></span>

## <span data-ttu-id="df927-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df927-150">RELATED LINKS</span></span>

[<span data-ttu-id="df927-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="df927-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="df927-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="df927-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="df927-153">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="df927-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="df927-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="df927-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
