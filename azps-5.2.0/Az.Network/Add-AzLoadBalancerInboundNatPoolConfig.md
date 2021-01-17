---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 993b1a3987427f096ecd061199663b35b6577b08
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365614"
---
# <span data-ttu-id="58626-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58626-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="58626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58626-102">SYNOPSIS</span></span>
<span data-ttu-id="58626-103">Fügt einem Lastenausgleich einen eingehenden NAT-Pool hinzu.</span><span class="sxs-lookup"><span data-stu-id="58626-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="58626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58626-104">SYNTAX</span></span>

### <span data-ttu-id="58626-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="58626-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58626-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58626-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58626-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58626-107">DESCRIPTION</span></span>
<span data-ttu-id="58626-108">Das **Cmdlet "Add-AzLoadBalancerInboundNatPoolConfig"** fügt einem Lastenausgleich einen eingehenden NAT-Pool hinzu.</span><span class="sxs-lookup"><span data-stu-id="58626-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="58626-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58626-109">EXAMPLES</span></span>

### <span data-ttu-id="58626-110">Beispiel 1: Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="58626-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="58626-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58626-111">PARAMETERS</span></span>

### <span data-ttu-id="58626-112">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="58626-112">-BackendPort</span></span>
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

### <span data-ttu-id="58626-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58626-113">-DefaultProfile</span></span>
<span data-ttu-id="58626-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58626-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58626-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="58626-115">-EnableFloatingIP</span></span>
<span data-ttu-id="58626-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-Verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="58626-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="58626-117">Diese Einstellung ist erforderlich, wenn Sie SQL "AlwaysOn-Verfügbarkeitsgruppen" auf einem SQL verwenden.</span><span class="sxs-lookup"><span data-stu-id="58626-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="58626-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="58626-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="58626-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="58626-119">-EnableTcpReset</span></span>
<span data-ttu-id="58626-120">Empfangen der bidirektionalen TCP-Zurücksetzung für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="58626-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="58626-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="58626-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="58626-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="58626-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="58626-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="58626-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="58626-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="58626-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="58626-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="58626-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="58626-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="58626-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="58626-127">Der Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="58626-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="58626-128">Der Wert kann zwischen 4 und 30 Minuten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="58626-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="58626-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="58626-129">The default value is 4 minutes.</span></span> <span data-ttu-id="58626-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="58626-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="58626-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58626-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="58626-132">-Name</span><span class="sxs-lookup"><span data-stu-id="58626-132">-Name</span></span>
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

### <span data-ttu-id="58626-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="58626-133">-Protocol</span></span>
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

### <span data-ttu-id="58626-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58626-134">-Confirm</span></span>
<span data-ttu-id="58626-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58626-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58626-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="58626-136">-WhatIf</span></span>
<span data-ttu-id="58626-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58626-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58626-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58626-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58626-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58626-139">CommonParameters</span></span>
<span data-ttu-id="58626-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58626-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58626-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58626-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58626-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58626-142">INPUTS</span></span>

### <span data-ttu-id="58626-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58626-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="58626-144">System.String</span><span class="sxs-lookup"><span data-stu-id="58626-144">System.String</span></span>

### <span data-ttu-id="58626-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="58626-145">System.Int32</span></span>

### <span data-ttu-id="58626-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="58626-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="58626-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58626-147">OUTPUTS</span></span>

### <span data-ttu-id="58626-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="58626-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="58626-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58626-149">NOTES</span></span>

## <span data-ttu-id="58626-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58626-150">RELATED LINKS</span></span>

[<span data-ttu-id="58626-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58626-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58626-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58626-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58626-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58626-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="58626-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="58626-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
