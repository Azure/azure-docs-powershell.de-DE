---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 2bc63fb21de63dc35855acad53c7e42a13caf215
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948536"
---
# <span data-ttu-id="5294b-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5294b-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="5294b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5294b-102">SYNOPSIS</span></span>
<span data-ttu-id="5294b-103">Erstellt einen Lastenausgleich.</span><span class="sxs-lookup"><span data-stu-id="5294b-103">Creates a load balancer.</span></span>

## <span data-ttu-id="5294b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5294b-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5294b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5294b-105">DESCRIPTION</span></span>
<span data-ttu-id="5294b-106">Das **Cmdlet New-AzLoadBalancer** erstellt einen Azure Load Balancer.</span><span class="sxs-lookup"><span data-stu-id="5294b-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="5294b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5294b-107">EXAMPLES</span></span>

### <span data-ttu-id="5294b-108">Beispiel 1: Erstellen eines Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="5294b-108">Example 1: Create a load balancer</span></span>
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

<span data-ttu-id="5294b-109">Für die Bereitstellung eines Lastenausgleichs müssen Sie zuerst mehrere Objekte erstellen, und die ersten sieben Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5294b-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="5294b-110">Mit dem achten Befehl wird ein Lastenausgleich mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "MyResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5294b-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="5294b-111">Der neunte und letzte Befehl ruft den neuen Load Balancer ab, um sicherzustellen, dass er erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5294b-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="5294b-112">Beachten Sie, dass in diesem Beispiel nur das Erstellen eines Lastenausgleichs veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="5294b-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="5294b-113">Sie müssen es auch mithilfe des cmdlets Add-AzNetworkInterfaceIpConfig konfigurieren, um die NICs verschiedenen virtuellen Computern zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5294b-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="5294b-114">Beispiel 2: Erstellen eines globalen Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="5294b-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5294b-115">Für die Bereitstellung eines globalen Lastenausgleichs müssen Sie zuerst mehrere Objekte erstellen, und die ersten fünf Befehle zeigen, wie diese Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5294b-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="5294b-116">Mit dem sechsten Befehl wird ein Lastenausgleich mit dem Namen "MyLoadBalancer" in der Ressourcengruppe "MyResourceGroup" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5294b-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="5294b-117">Der siebte und letzte Befehl ruft den neuen Load Balancer ab, um sicherzustellen, dass er erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5294b-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="5294b-118">Beachten Sie, dass in diesem Beispiel nur gezeigt wird, wie ein globaler Lastenausgleich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5294b-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="5294b-119">Sie müssen es auch mithilfe des New-AzLoadBalancerBackendAddressConfig-Cmdlets konfigurieren, um seinem Back-End-Adresspool ipconfig-IDs für den regionalen Load Balancer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="5294b-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="5294b-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5294b-120">PARAMETERS</span></span>

### <span data-ttu-id="5294b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5294b-121">-AsJob</span></span>
<span data-ttu-id="5294b-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5294b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5294b-123">-Back-EndAddressPool</span><span class="sxs-lookup"><span data-stu-id="5294b-123">-BackendAddressPool</span></span>
<span data-ttu-id="5294b-124">Gibt einen Back-End-Adresspool an, der einem Load Balancer zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5294b-124">Specifies a backend address pool to associate with a load balancer.</span></span>

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

### <span data-ttu-id="5294b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5294b-125">-DefaultProfile</span></span>
<span data-ttu-id="5294b-126">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5294b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5294b-127">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="5294b-127">-Force</span></span>
<span data-ttu-id="5294b-128">Gibt an, dass dieses Cmdlet einen Lastenausgleich erstellt, auch wenn bereits ein Load Balancer mit demselben Namen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5294b-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="5294b-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5294b-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="5294b-130">Gibt eine Liste der Front-End-IP-Adressen an, die einem Load Balancer zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5294b-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

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

### <span data-ttu-id="5294b-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="5294b-131">-InboundNatPool</span></span>
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

### <span data-ttu-id="5294b-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="5294b-132">-InboundNatRule</span></span>
<span data-ttu-id="5294b-133">Gibt eine Liste der NAT(Inbound Network Address Translation)-Regeln an, die einem Load Balancer zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5294b-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="5294b-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="5294b-134">-LoadBalancingRule</span></span>
<span data-ttu-id="5294b-135">Gibt eine Liste der Lastenausgleichsregeln an, die einem Lastenausgleich zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5294b-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

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

### <span data-ttu-id="5294b-136">-Location</span><span class="sxs-lookup"><span data-stu-id="5294b-136">-Location</span></span>
<span data-ttu-id="5294b-137">Gibt den Bereich an, in dem ein Lastenausgleich erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5294b-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="5294b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="5294b-138">-Name</span></span>
<span data-ttu-id="5294b-139">Gibt den Namen des dadurch erstellten Lastenausgleichs an.</span><span class="sxs-lookup"><span data-stu-id="5294b-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="5294b-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="5294b-140">-OutboundRule</span></span>
<span data-ttu-id="5294b-141">Die ausgehenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="5294b-141">The outbound rules.</span></span>

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

### <span data-ttu-id="5294b-142">-Probe</span><span class="sxs-lookup"><span data-stu-id="5294b-142">-Probe</span></span>
<span data-ttu-id="5294b-143">Gibt eine Liste der Prüfpunkte an, die einem Lastenausgleich zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5294b-143">Specifies a list of probes to associate with a load balancer.</span></span>

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

### <span data-ttu-id="5294b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5294b-144">-ResourceGroupName</span></span>
<span data-ttu-id="5294b-145">Gibt den Namen der Ressourcengruppe an, in der ein Lastenausgleich erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5294b-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="5294b-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="5294b-146">-Sku</span></span>
<span data-ttu-id="5294b-147">Der Name der Load Balancer-Sku.</span><span class="sxs-lookup"><span data-stu-id="5294b-147">The load balancer Sku name.</span></span>

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

### <span data-ttu-id="5294b-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="5294b-148">-Tag</span></span>
<span data-ttu-id="5294b-149">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5294b-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5294b-150">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5294b-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5294b-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="5294b-151">-Tier</span></span>
<span data-ttu-id="5294b-152">Die Load Balancer-Sku-Ebene.</span><span class="sxs-lookup"><span data-stu-id="5294b-152">The load balancer Sku Tier.</span></span>

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

### <span data-ttu-id="5294b-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5294b-153">-Confirm</span></span>
<span data-ttu-id="5294b-154">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5294b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5294b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5294b-155">-WhatIf</span></span>
<span data-ttu-id="5294b-156">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5294b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5294b-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5294b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5294b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5294b-158">CommonParameters</span></span>
<span data-ttu-id="5294b-159">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5294b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5294b-160">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5294b-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5294b-161">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5294b-161">INPUTS</span></span>

### <span data-ttu-id="5294b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="5294b-162">System.String</span></span>

### <span data-ttu-id="5294b-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5294b-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5294b-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="5294b-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="5294b-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="5294b-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="5294b-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="5294b-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="5294b-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="5294b-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="5294b-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="5294b-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="5294b-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="5294b-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="5294b-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="5294b-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="5294b-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5294b-171">OUTPUTS</span></span>

### <span data-ttu-id="5294b-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5294b-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5294b-173">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5294b-173">NOTES</span></span>

## <span data-ttu-id="5294b-174">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5294b-174">RELATED LINKS</span></span>

[<span data-ttu-id="5294b-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5294b-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5294b-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5294b-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5294b-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5294b-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="5294b-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5294b-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)
