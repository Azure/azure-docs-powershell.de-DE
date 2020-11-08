---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 5c9a70399cc50b773e492410b951b7959e8ade60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995735"
---
# <span data-ttu-id="a92eb-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a92eb-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="a92eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a92eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a92eb-103">Fügt einen eingehenden NAT-Pool zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a92eb-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="a92eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a92eb-104">SYNTAX</span></span>

### <span data-ttu-id="a92eb-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a92eb-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a92eb-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a92eb-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a92eb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a92eb-107">DESCRIPTION</span></span>
<span data-ttu-id="a92eb-108">Das Cmdlet **Add-AzLoadBalancerInboundNatPoolConfig** fügt einen eingehenden NAT-Pool zu einem Lastenausgleichsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="a92eb-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="a92eb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a92eb-109">EXAMPLES</span></span>

### <span data-ttu-id="a92eb-110">1: Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="a92eb-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="a92eb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a92eb-111">PARAMETERS</span></span>

### <span data-ttu-id="a92eb-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a92eb-112">-BackendPort</span></span>
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

### <span data-ttu-id="a92eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92eb-113">-DefaultProfile</span></span>
<span data-ttu-id="a92eb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a92eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a92eb-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="a92eb-115">-EnableFloatingIP</span></span>
<span data-ttu-id="a92eb-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a92eb-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="a92eb-117">Diese Einstellung ist bei Verwendung der SQL AlwaysOn-Verfügbarkeitsgruppen in SQL Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a92eb-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="a92eb-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a92eb-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="a92eb-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="a92eb-119">-EnableTcpReset</span></span>
<span data-ttu-id="a92eb-120">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="a92eb-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="a92eb-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="a92eb-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a92eb-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="a92eb-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a92eb-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="a92eb-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="a92eb-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="a92eb-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="a92eb-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="a92eb-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a92eb-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a92eb-127">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="a92eb-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="a92eb-128">Der Wert kann zwischen 4 und 30 Minuten eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a92eb-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="a92eb-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="a92eb-129">The default value is 4 minutes.</span></span> <span data-ttu-id="a92eb-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="a92eb-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="a92eb-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a92eb-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="a92eb-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a92eb-132">-Name</span></span>
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

### <span data-ttu-id="a92eb-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a92eb-133">-Protocol</span></span>
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

### <span data-ttu-id="a92eb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a92eb-134">-Confirm</span></span>
<span data-ttu-id="a92eb-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a92eb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a92eb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a92eb-136">-WhatIf</span></span>
<span data-ttu-id="a92eb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a92eb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a92eb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a92eb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a92eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92eb-139">CommonParameters</span></span>
<span data-ttu-id="a92eb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92eb-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92eb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92eb-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a92eb-142">INPUTS</span></span>

### <span data-ttu-id="a92eb-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a92eb-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="a92eb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a92eb-144">System.String</span></span>

### <span data-ttu-id="a92eb-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a92eb-145">System.Int32</span></span>

### <span data-ttu-id="a92eb-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a92eb-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="a92eb-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a92eb-147">OUTPUTS</span></span>

### <span data-ttu-id="a92eb-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a92eb-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a92eb-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a92eb-149">NOTES</span></span>

## <span data-ttu-id="a92eb-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a92eb-150">RELATED LINKS</span></span>

[<span data-ttu-id="a92eb-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a92eb-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a92eb-152">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a92eb-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a92eb-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a92eb-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a92eb-154">Satz-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a92eb-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
