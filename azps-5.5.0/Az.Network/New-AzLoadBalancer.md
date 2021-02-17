---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146924"
---
# <span data-ttu-id="95563-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95563-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="95563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95563-102">SYNOPSIS</span></span>
<span data-ttu-id="95563-103">Erstellt einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="95563-103">Creates a load balancer.</span></span>

## <span data-ttu-id="95563-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95563-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95563-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95563-105">DESCRIPTION</span></span>
<span data-ttu-id="95563-106">Das **Cmdlet "New-AzLoadBalancer"** erstellt einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="95563-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="95563-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95563-107">EXAMPLES</span></span>

### <span data-ttu-id="95563-108">Beispiel 1: Erstellen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="95563-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="95563-109">Zum Bereitstellen eines Lastenausgleichs müssen Sie zunächst mehrere Objekte erstellen. Die ersten sieben Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95563-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="95563-110">Der achte Befehl erstellt einen Lastenausgleich mit dem Namen "MyLoadBalancer" in der Ressourcengruppe mit dem Namen "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="95563-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="95563-111">Der neunte und der letzte Befehl ruft den neuen Lastenausgleich ab, um sicherzustellen, dass er erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95563-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="95563-112">Beachten Sie, dass in diesem Beispiel nur gezeigt wird, wie ein Lastenausgleich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95563-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="95563-113">Sie müssen es auch mit dem cmdlet Add-AzNetworkInterfaceIpConfig konfigurieren, um die NICs verschiedenen virtuellen Computern zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="95563-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="95563-114">Beispiel 2: Erstellen eines globalen Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="95563-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="95563-115">Zum Bereitstellen eines globalen Lastenausgleichs müssen Sie zunächst mehrere Objekte erstellen. Die ersten fünf Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95563-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="95563-116">Der sechste Befehl erstellt einen Lastenausgleich mit dem Namen "MyLoadBalancer" in der Ressourcengruppe mit dem Namen "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="95563-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="95563-117">Der siebte und der letzte Befehl ruft den neuen Lastenausgleich ab, um sicherzustellen, dass er erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95563-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="95563-118">Beachten Sie, dass in diesem Beispiel nur gezeigt wird, wie ein globaler Lastenausgleich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95563-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="95563-119">Sie müssen es auch mit dem cmdlet New-AzLoadBalancerBackendAddressConfig konfigurieren, um dem Back-End-Adresspool die ipconfig-ID des regionalen Lastenausgleichs zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="95563-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="95563-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95563-120">PARAMETERS</span></span>

### <span data-ttu-id="95563-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95563-121">-AsJob</span></span>
<span data-ttu-id="95563-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="95563-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95563-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="95563-123">-BackendAddressPool</span></span>
<span data-ttu-id="95563-124">Gibt einen Back-End-Adresspool an, der einem Lastenausgleich zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95563-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="95563-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95563-125">-DefaultProfile</span></span>
<span data-ttu-id="95563-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95563-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95563-127">-Force</span><span class="sxs-lookup"><span data-stu-id="95563-127">-Force</span></span>
<span data-ttu-id="95563-128">Gibt an, dass dieses Cmdlet einen Lastenausgleich erstellt, auch wenn bereits ein Lastenausgleich mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="95563-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="95563-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="95563-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="95563-130">Gibt eine Liste der Front-End-IP-Adressen an, die einem Lastenausgleich zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95563-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="95563-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="95563-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="95563-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="95563-132">-InboundNatRule</span></span>
<span data-ttu-id="95563-133">Gibt eine Liste der Regeln für die eingehende Netzwerkadressenübersetzung (NAT) an, die einem Lastenausgleich zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95563-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="95563-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="95563-134">-LoadBalancingRule</span></span>
<span data-ttu-id="95563-135">Gibt eine Liste von Lastenausgleichsregeln an, die einem Lastenausgleich zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95563-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="95563-136">-Location</span><span class="sxs-lookup"><span data-stu-id="95563-136">-Location</span></span>
<span data-ttu-id="95563-137">Gibt den Bereich an, in dem ein Lastenausgleich erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95563-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="95563-138">-Name</span><span class="sxs-lookup"><span data-stu-id="95563-138">-Name</span></span>
<span data-ttu-id="95563-139">Gibt den Namen des dadurch erstellten Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="95563-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="95563-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="95563-140">-OutboundRule</span></span>
<span data-ttu-id="95563-141">Die ausgehenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="95563-141">The outbound rules.</span></span>

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

### <span data-ttu-id="95563-142">-Probe</span><span class="sxs-lookup"><span data-stu-id="95563-142">-Probe</span></span>
<span data-ttu-id="95563-143">Gibt eine Liste von Sonden an, die einem Lastenausgleich zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95563-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="95563-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95563-144">-ResourceGroupName</span></span>
<span data-ttu-id="95563-145">Gibt den Namen der Ressourcengruppe an, in der ein Lastenausgleich erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95563-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="95563-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="95563-146">-Sku</span></span>
<span data-ttu-id="95563-147">Der Name der SKU für den Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="95563-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="95563-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="95563-148">-Tag</span></span>
<span data-ttu-id="95563-149">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="95563-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="95563-150">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="95563-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="95563-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="95563-151">-Tier</span></span>
<span data-ttu-id="95563-152">Die SKU-Stufe des Lastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="95563-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="95563-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95563-153">-Confirm</span></span>
<span data-ttu-id="95563-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95563-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95563-155">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95563-155">-WhatIf</span></span>
<span data-ttu-id="95563-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95563-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95563-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95563-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95563-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95563-158">CommonParameters</span></span>
<span data-ttu-id="95563-159">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95563-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95563-160">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95563-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95563-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95563-161">INPUTS</span></span>

### <span data-ttu-id="95563-162">System.String</span><span class="sxs-lookup"><span data-stu-id="95563-162">System.String</span></span>

### <span data-ttu-id="95563-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="95563-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="95563-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="95563-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="95563-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="95563-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="95563-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="95563-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="95563-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="95563-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="95563-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="95563-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="95563-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="95563-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="95563-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="95563-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="95563-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95563-171">OUTPUTS</span></span>

### <span data-ttu-id="95563-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95563-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="95563-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95563-173">NOTES</span></span>

## <span data-ttu-id="95563-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95563-174">RELATED LINKS</span></span>

[<span data-ttu-id="95563-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="95563-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="95563-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95563-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="95563-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95563-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="95563-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="95563-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
