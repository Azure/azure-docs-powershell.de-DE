---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301256"
---
# <span data-ttu-id="b2cd2-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2cd2-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b2cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cd2-103">Erstellt eine eingehende NAT-Poolkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b2cd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2cd2-104">SYNTAX</span></span>

### <span data-ttu-id="b2cd2-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2cd2-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2cd2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b2cd2-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2cd2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2cd2-107">DESCRIPTION</span></span>
<span data-ttu-id="b2cd2-108">Das **Cmdlet "New-AzLoadBalancerInboundNatPoolConfig"** erstellt eine eingehende NAT-Poolkonfiguration für einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="b2cd2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2cd2-109">EXAMPLES</span></span>

### <span data-ttu-id="b2cd2-110">Beispiel 1: Neu</span><span class="sxs-lookup"><span data-stu-id="b2cd2-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="b2cd2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2cd2-111">PARAMETERS</span></span>

### <span data-ttu-id="b2cd2-112">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="b2cd2-112">-BackendPort</span></span>
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

### <span data-ttu-id="b2cd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cd2-113">-DefaultProfile</span></span>
<span data-ttu-id="b2cd2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2cd2-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="b2cd2-115">-EnableFloatingIP</span></span>
<span data-ttu-id="b2cd2-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-Verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="b2cd2-117">Diese Einstellung ist erforderlich, wenn Sie SQL "AlwaysOn-Verfügbarkeitsgruppen" auf einem SQL verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="b2cd2-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="b2cd2-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="b2cd2-119">-EnableTcpReset</span></span>
<span data-ttu-id="b2cd2-120">Empfangen der bidirektionalen TCP-Zurücksetzung für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="b2cd2-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b2cd2-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2cd2-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="b2cd2-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b2cd2-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="b2cd2-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="b2cd2-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="b2cd2-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="b2cd2-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="b2cd2-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="b2cd2-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="b2cd2-127">Der Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="b2cd2-128">Der Wert kann zwischen 4 und 30 Minuten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="b2cd2-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-129">The default value is 4 minutes.</span></span> <span data-ttu-id="b2cd2-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="b2cd2-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b2cd2-131">-Name</span></span>
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

### <span data-ttu-id="b2cd2-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b2cd2-132">-Protocol</span></span>
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

### <span data-ttu-id="b2cd2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2cd2-133">-Confirm</span></span>
<span data-ttu-id="b2cd2-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2cd2-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b2cd2-135">-WhatIf</span></span>
<span data-ttu-id="b2cd2-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2cd2-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2cd2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cd2-138">CommonParameters</span></span>
<span data-ttu-id="b2cd2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cd2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cd2-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cd2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cd2-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cd2-141">INPUTS</span></span>

### <span data-ttu-id="b2cd2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b2cd2-142">System.String</span></span>

### <span data-ttu-id="b2cd2-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b2cd2-143">System.Int32</span></span>

### <span data-ttu-id="b2cd2-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2cd2-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="b2cd2-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cd2-145">OUTPUTS</span></span>

### <span data-ttu-id="b2cd2-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="b2cd2-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="b2cd2-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2cd2-147">NOTES</span></span>

## <span data-ttu-id="b2cd2-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2cd2-148">RELATED LINKS</span></span>

[<span data-ttu-id="b2cd2-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2cd2-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2cd2-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2cd2-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2cd2-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2cd2-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b2cd2-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b2cd2-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
