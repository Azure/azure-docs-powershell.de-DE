---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 0b51e2b01fd194b0cb400e2d8547f7d7df78f0a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178463"
---
# <span data-ttu-id="a9fe5-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="a9fe5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe5-103">Erstellt ein Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-103">Creates a load balancer.</span></span>

## <span data-ttu-id="a9fe5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fe5-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fe5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="a9fe5-106">Das Cmdlet **New-AzLoadBalancer** erstellt ein Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="a9fe5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="a9fe5-108">Beispiel 1: Erstellen eines Load Balancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-108">Example 1: Create a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a9fe5-109">Zum Bereitstellen eines Load Balancer müssen Sie zunächst mehrere Objekte erstellen, und die ersten sieben Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="a9fe5-110">Mit dem achten Befehl wird ein Lastenausgleichsmodul mit dem Namen MyLoadBalancer in der Ressourcengruppe "myresourcegroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="a9fe5-111">Der neunte und letzte Befehl ruft das neue Lastenausgleichsmodul ab, um sicherzustellen, dass es erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="a9fe5-112">Beachten Sie, dass in diesem Beispiel nur gezeigt wird, wie ein Load Balancer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="a9fe5-113">Sie müssen es auch mit dem Add-AzNetworkInterfaceIpConfig-Cmdlet konfigurieren, um die NICs verschiedenen virtuellen Computern zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

## <span data-ttu-id="a9fe5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fe5-114">PARAMETERS</span></span>

### <span data-ttu-id="a9fe5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9fe5-115">-AsJob</span></span>
<span data-ttu-id="a9fe5-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a9fe5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9fe5-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a9fe5-117">-BackendAddressPool</span></span>
<span data-ttu-id="a9fe5-118">Gibt einen Back-End-Adresspool an, der einem Lastenausgleichsmodul zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-118">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe5-119">-DefaultProfile</span></span>
<span data-ttu-id="a9fe5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9fe5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a9fe5-121">-Force</span></span>
<span data-ttu-id="a9fe5-122">Gibt an, dass dieses Cmdlet ein Lastenausgleichsmodul erstellt, auch wenn bereits ein Lastenausgleichsmodul mit dem gleichen Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-122">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="a9fe5-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9fe5-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="a9fe5-124">Gibt eine Liste der Front-End-IP-Adressen an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-124">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-125">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="a9fe5-125">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-126">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="a9fe5-126">-InboundNatRule</span></span>
<span data-ttu-id="a9fe5-127">Gibt eine Liste der eingehenden NAT-Regeln (Network Address Translation) an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-127">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-128">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="a9fe5-128">-LoadBalancingRule</span></span>
<span data-ttu-id="a9fe5-129">Gibt eine Liste der Lastenausgleichs Regeln an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-129">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="a9fe5-130">-Location</span></span>
<span data-ttu-id="a9fe5-131">Gibt den Bereich an, in dem ein Lastenausgleichsmodul erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-131">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="a9fe5-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a9fe5-132">-Name</span></span>
<span data-ttu-id="a9fe5-133">Gibt den Namen des Load Balancer an, den dieser erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-133">Specifies the name of the load balancer that this creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-134">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="a9fe5-134">-OutboundRule</span></span>
<span data-ttu-id="a9fe5-135">Die ausgehenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-135">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="a9fe5-136">-Probe</span></span>
<span data-ttu-id="a9fe5-137">Gibt eine Liste der Prüfpunkte an, die einem Lastenausgleichsmodul zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-137">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe5-138">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe5-139">Gibt den Namen der Ressourcengruppe an, in der ein Lastenausgleichsmodul erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-139">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="a9fe5-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9fe5-140">-Sku</span></span>
<span data-ttu-id="a9fe5-141">Der SKU-Name des Lastenausgleichsmoduls.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-141">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="a9fe5-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9fe5-142">-Tag</span></span>
<span data-ttu-id="a9fe5-143">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a9fe5-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a9fe5-144">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="a9fe5-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9fe5-145">-Confirm</span></span>
<span data-ttu-id="a9fe5-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fe5-147">-WhatIf</span></span>
<span data-ttu-id="a9fe5-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fe5-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fe5-150">CommonParameters</span></span>
<span data-ttu-id="a9fe5-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fe5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fe5-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fe5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fe5-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9fe5-153">INPUTS</span></span>

### <span data-ttu-id="a9fe5-154">System. String</span><span class="sxs-lookup"><span data-stu-id="a9fe5-154">System.String</span></span>

### <span data-ttu-id="a9fe5-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9fe5-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9fe5-156">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-156">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="a9fe5-157">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-157">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="a9fe5-158">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="a9fe5-159">Microsoft. Azure. Commands. Network. Models. PSProbe []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-159">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="a9fe5-160">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-160">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="a9fe5-161">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-161">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="a9fe5-162">Microsoft. Azure. Commands. Network. Models. PSOutboundRule []</span><span class="sxs-lookup"><span data-stu-id="a9fe5-162">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="a9fe5-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9fe5-163">OUTPUTS</span></span>

### <span data-ttu-id="a9fe5-164">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-164">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9fe5-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9fe5-165">NOTES</span></span>

## <span data-ttu-id="a9fe5-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9fe5-166">RELATED LINKS</span></span>

[<span data-ttu-id="a9fe5-167">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a9fe5-167">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a9fe5-168">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-168">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a9fe5-169">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-169">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="a9fe5-170">Satz-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fe5-170">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
