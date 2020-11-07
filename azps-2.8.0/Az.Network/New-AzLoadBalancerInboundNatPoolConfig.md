---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 1abb410ad89a0e92cd8a4f460bccef21c2a57d77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821564"
---
# <span data-ttu-id="1552c-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1552c-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="1552c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1552c-102">SYNOPSIS</span></span>
<span data-ttu-id="1552c-103">Erstellt eine eingehende NAT-Poolkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="1552c-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="1552c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1552c-104">SYNTAX</span></span>

### <span data-ttu-id="1552c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1552c-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1552c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1552c-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1552c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1552c-107">DESCRIPTION</span></span>
<span data-ttu-id="1552c-108">Das Cmdlet **New-AzLoadBalancerInboundNatPoolConfig** erstellt eine eingehende NAT-Poolkonfiguration für ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="1552c-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="1552c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1552c-109">EXAMPLES</span></span>

### <span data-ttu-id="1552c-110">1: neu</span><span class="sxs-lookup"><span data-stu-id="1552c-110">1: New</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="1552c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1552c-111">PARAMETERS</span></span>

### <span data-ttu-id="1552c-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="1552c-112">-BackendPort</span></span>
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

### <span data-ttu-id="1552c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1552c-113">-DefaultProfile</span></span>
<span data-ttu-id="1552c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1552c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1552c-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="1552c-115">-EnableFloatingIP</span></span>
<span data-ttu-id="1552c-116">Konfiguriert den Endpunkt eines virtuellen Computers für die unverankerte IP-Funktion, die zum Konfigurieren einer SQL AlwaysOn-verfügbarkeitsgruppe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1552c-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="1552c-117">Diese Einstellung ist bei Verwendung der SQL AlwaysOn-Verfügbarkeitsgruppen in SQL Server erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1552c-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="1552c-118">Diese Einstellung kann nach dem Erstellen des Endpunkts nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="1552c-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="1552c-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1552c-119">-EnableTcpReset</span></span>
<span data-ttu-id="1552c-120">Bidirektionaler TCP-Reset für TCP-Fluss-Leerlauftimeout oder unerwartete Verbindungs Beendigung empfangen.</span><span class="sxs-lookup"><span data-stu-id="1552c-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="1552c-121">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="1552c-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1552c-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1552c-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="1552c-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1552c-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="1552c-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="1552c-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="1552c-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="1552c-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="1552c-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1552c-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1552c-127">Das Timeout für die TCP-Leerlaufverbindung.</span><span class="sxs-lookup"><span data-stu-id="1552c-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="1552c-128">Der Wert kann zwischen 4 und 30 Minuten eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1552c-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="1552c-129">Der Standardwert ist 4 Minuten.</span><span class="sxs-lookup"><span data-stu-id="1552c-129">The default value is 4 minutes.</span></span> <span data-ttu-id="1552c-130">Dieses Element wird nur verwendet, wenn das Protokoll auf TCP eingestellt ist.</span><span class="sxs-lookup"><span data-stu-id="1552c-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1552c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1552c-131">-Name</span></span>
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

### <span data-ttu-id="1552c-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1552c-132">-Protocol</span></span>
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

### <span data-ttu-id="1552c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1552c-133">-Confirm</span></span>
<span data-ttu-id="1552c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1552c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1552c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1552c-135">-WhatIf</span></span>
<span data-ttu-id="1552c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1552c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1552c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1552c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1552c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1552c-138">CommonParameters</span></span>
<span data-ttu-id="1552c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1552c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1552c-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1552c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1552c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1552c-141">INPUTS</span></span>

### <span data-ttu-id="1552c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1552c-142">System.String</span></span>

### <span data-ttu-id="1552c-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1552c-143">System.Int32</span></span>

### <span data-ttu-id="1552c-144">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1552c-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="1552c-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1552c-145">OUTPUTS</span></span>

### <span data-ttu-id="1552c-146">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="1552c-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="1552c-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="1552c-147">NOTES</span></span>

## <span data-ttu-id="1552c-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1552c-148">RELATED LINKS</span></span>

[<span data-ttu-id="1552c-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1552c-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1552c-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1552c-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1552c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1552c-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="1552c-152">Satz-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1552c-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
