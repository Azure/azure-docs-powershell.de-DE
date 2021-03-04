---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 58ee0531ea0671314e6f1e6d590b388c3f82ef34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933848"
---
# <span data-ttu-id="7b301-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b301-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="7b301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b301-102">SYNOPSIS</span></span>
<span data-ttu-id="7b301-103">Fügt einem Load Balancer einen eingehenden NAT-Pool hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b301-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7b301-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b301-104">SYNTAX</span></span>

### <span data-ttu-id="7b301-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b301-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b301-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b301-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b301-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b301-107">DESCRIPTION</span></span>
<span data-ttu-id="7b301-108">Das **Add-AzLoadBalancerInboundNatPoolConfig-Cmdlet** fügt einem Load Balancer einen eingehenden NAT-Pool hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b301-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="7b301-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b301-109">EXAMPLES</span></span>

### <span data-ttu-id="7b301-110">Beispiel 1: Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="7b301-110">Example 1: Add</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
PS C:\> $lb | Set-AzLoadBalancer
```

## <span data-ttu-id="7b301-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7b301-111">PARAMETERS</span></span>

### <span data-ttu-id="7b301-112">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="7b301-112">-BackendPort</span></span>
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

### <span data-ttu-id="7b301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b301-113">-DefaultProfile</span></span>
<span data-ttu-id="7b301-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b301-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b301-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="7b301-115">-EnableFloatingIP</span></span>
<span data-ttu-id="7b301-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-Verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7b301-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="7b301-117">Diese Einstellung ist erforderlich, wenn Sie SQL AlwaysOn-Verfügbarkeitsgruppen in einem SQL verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b301-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="7b301-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="7b301-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="7b301-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="7b301-119">-EnableTcpReset</span></span>
<span data-ttu-id="7b301-120">Empfangen eines bidirektionalen TCP-Reset für den TCP-Fluss-Leerlauftimeout oder unerwartetes Beenden der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="7b301-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="7b301-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7b301-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7b301-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b301-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="7b301-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7b301-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="7b301-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="7b301-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="7b301-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="7b301-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="7b301-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b301-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="7b301-127">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="7b301-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="7b301-128">Der Wert kann zwischen 4 und 30 Minuten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b301-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="7b301-129">Der Standardwert beträgt 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7b301-129">The default value is 4 minutes.</span></span> <span data-ttu-id="7b301-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7b301-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="7b301-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b301-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="7b301-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7b301-132">-Name</span></span>
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

### <span data-ttu-id="7b301-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7b301-133">-Protocol</span></span>
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

### <span data-ttu-id="7b301-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b301-134">-Confirm</span></span>
<span data-ttu-id="7b301-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b301-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b301-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b301-136">-WhatIf</span></span>
<span data-ttu-id="7b301-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b301-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b301-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b301-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b301-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b301-139">CommonParameters</span></span>
<span data-ttu-id="7b301-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b301-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b301-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b301-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b301-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b301-142">INPUTS</span></span>

### <span data-ttu-id="7b301-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b301-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7b301-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7b301-144">System.String</span></span>

### <span data-ttu-id="7b301-145">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7b301-145">System.Int32</span></span>

### <span data-ttu-id="7b301-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b301-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="7b301-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b301-147">OUTPUTS</span></span>

### <span data-ttu-id="7b301-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b301-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7b301-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7b301-149">NOTES</span></span>

## <span data-ttu-id="7b301-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7b301-150">RELATED LINKS</span></span>

[<span data-ttu-id="7b301-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b301-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b301-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b301-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b301-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b301-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="7b301-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="7b301-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
