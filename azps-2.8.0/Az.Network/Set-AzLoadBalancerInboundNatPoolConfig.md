---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3ea89cf0450a5cf24c4299f7eb9c5183195a9663
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822723"
---
# <span data-ttu-id="4f1cd-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f1cd-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="4f1cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1cd-103">Legt eine eingehende NAT-Poolkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4f1cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f1cd-104">SYNTAX</span></span>

### <span data-ttu-id="4f1cd-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f1cd-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f1cd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f1cd-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1cd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f1cd-107">DESCRIPTION</span></span>
<span data-ttu-id="4f1cd-108">Das Cmdlet " **Set-AzLoadBalancerInboundNatPoolConfig** " legt eine eingehende NAT-Poolkonfiguration für ein Load Balancer fest.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="4f1cd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f1cd-109">EXAMPLES</span></span>

### <span data-ttu-id="4f1cd-110">1: setzen Sie</span><span class="sxs-lookup"><span data-stu-id="4f1cd-110">1: Set</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="4f1cd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f1cd-111">PARAMETERS</span></span>

### <span data-ttu-id="4f1cd-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="4f1cd-112">-BackendPort</span></span>
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

### <span data-ttu-id="4f1cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1cd-113">-DefaultProfile</span></span>
<span data-ttu-id="4f1cd-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f1cd-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="4f1cd-115">-EnableFloatingIP</span></span>
<span data-ttu-id="4f1cd-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="4f1cd-117">Diese Einstellung ist bei Verwendung der SQL AlwaysOn-Verfügbarkeitsgruppen in SQL Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="4f1cd-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="4f1cd-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="4f1cd-119">-EnableTcpReset</span></span>
<span data-ttu-id="4f1cd-120">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="4f1cd-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4f1cd-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f1cd-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="4f1cd-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4f1cd-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="4f1cd-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="4f1cd-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="4f1cd-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="4f1cd-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="4f1cd-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4f1cd-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4f1cd-127">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="4f1cd-128">Der Wert kann zwischen 4 und 30 Minuten eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="4f1cd-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-129">The default value is 4 minutes.</span></span> <span data-ttu-id="4f1cd-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4f1cd-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f1cd-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="4f1cd-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4f1cd-132">-Name</span></span>
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

### <span data-ttu-id="4f1cd-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4f1cd-133">-Protocol</span></span>
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

### <span data-ttu-id="4f1cd-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f1cd-134">-Confirm</span></span>
<span data-ttu-id="4f1cd-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f1cd-136">-WhatIf</span></span>
<span data-ttu-id="4f1cd-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f1cd-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1cd-139">CommonParameters</span></span>
<span data-ttu-id="4f1cd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1cd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f1cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1cd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f1cd-142">INPUTS</span></span>

### <span data-ttu-id="4f1cd-143">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f1cd-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4f1cd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4f1cd-144">System.String</span></span>

### <span data-ttu-id="4f1cd-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4f1cd-145">System.Int32</span></span>

### <span data-ttu-id="4f1cd-146">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f1cd-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="4f1cd-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f1cd-147">OUTPUTS</span></span>

### <span data-ttu-id="4f1cd-148">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4f1cd-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4f1cd-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f1cd-149">NOTES</span></span>

## <span data-ttu-id="4f1cd-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f1cd-150">RELATED LINKS</span></span>

[<span data-ttu-id="4f1cd-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f1cd-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4f1cd-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f1cd-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4f1cd-153">Neu – AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f1cd-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="4f1cd-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4f1cd-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
