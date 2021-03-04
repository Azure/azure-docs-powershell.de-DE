---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925136"
---
# <span data-ttu-id="e5387-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5387-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="e5387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5387-102">SYNOPSIS</span></span>
<span data-ttu-id="e5387-103">Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="e5387-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="e5387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5387-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5387-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5387-105">DESCRIPTION</span></span>
<span data-ttu-id="e5387-106">Das **Cmdlet New-AzVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines VmSS (Virtual Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e5387-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e5387-107">Geben Sie die Konfiguration aus diesem Cmdlet als *IPConfiguration-Parameter* des Add-AzVmssNetworkInterfaceConfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e5387-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="e5387-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5387-108">EXAMPLES</span></span>

### <span data-ttu-id="e5387-109">Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e5387-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="e5387-110">Mit diesem Befehl wird ein IP-Konfigurationsobjekt namens ContosoVmssInterface02 erstellt.</span><span class="sxs-lookup"><span data-stu-id="e5387-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="e5387-111">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="e5387-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e5387-112">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration für die spätere Verwendung mit **Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="e5387-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="e5387-113">Beispiel 2: Erstellen eines IP-Konfigurationsobjekts, das NAT-Pooleinstellungen enthält</span><span class="sxs-lookup"><span data-stu-id="e5387-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="e5387-114">Mit diesem Befehl wird ein IP-Konfigurationsobjekt namens ContosoVmssInterface03 erstellt und dann in der $IPConfiguration für die spätere Verwendung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e5387-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e5387-115">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="e5387-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="e5387-116">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e5387-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="e5387-117">Der Befehl gibt Werte für die *Parameter LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.</span><span class="sxs-lookup"><span data-stu-id="e5387-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="e5387-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e5387-118">PARAMETERS</span></span>

### <span data-ttu-id="e5387-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e5387-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="e5387-120">Gibt ein Array von Verweisen auf Back-End-Adresspools von Load Balancern an.</span><span class="sxs-lookup"><span data-stu-id="e5387-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="e5387-121">Ein Skalierungssatz kann auf Back-End-Adresspools eines öffentlichen und eines internen Lastenausgleichs verweisen.</span><span class="sxs-lookup"><span data-stu-id="e5387-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e5387-122">Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5387-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5387-123">-DefaultProfile</span></span>
<span data-ttu-id="e5387-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5387-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5387-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e5387-125">-DnsSetting</span></span>
<span data-ttu-id="e5387-126">Die dns-Einstellungen, die auf die öffentlichen IP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5387-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e5387-127">Die Domänennamenbeschriftung der Dns-Einstellungen, die auf die öffentlichen IP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e5387-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="e5387-128">Die Verkettung der Domänennamenbeschriftung und des VM-Indexes sind die Domänennamenbeschriftungen der Ressourcen für öffentliche IP-Adresse, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e5387-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-129">-ID</span><span class="sxs-lookup"><span data-stu-id="e5387-129">-Id</span></span>
<span data-ttu-id="e5387-130">Gibt eine ID an.</span><span class="sxs-lookup"><span data-stu-id="e5387-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e5387-131">-IpTag</span></span>
<span data-ttu-id="e5387-132">Gibt ein Array von Ip-Tag-Objekten an.</span><span class="sxs-lookup"><span data-stu-id="e5387-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="e5387-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="e5387-134">Gibt ein Array von Verweisen auf NAT(Incoming Network Address Translation)-Pools (Incoming Network Address Translation) der Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="e5387-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="e5387-135">Ein Skalierungssatz kann auf eingehende NAT-Pools von einem öffentlichen und einem internen Lastenausgleich verweisen.</span><span class="sxs-lookup"><span data-stu-id="e5387-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e5387-136">Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5387-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="e5387-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="e5387-138">Gibt ein Array von Verweisen auf eingehende NAT-Pools der Load Balancer an.</span><span class="sxs-lookup"><span data-stu-id="e5387-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="e5387-139">Ein Skalierungssatz kann auf eingehende NAT-Pools von einem öffentlichen und einem internen Lastenausgleich verweisen.</span><span class="sxs-lookup"><span data-stu-id="e5387-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="e5387-140">Für mehrere Skalierungssätze kann nicht derselbe Lastenausgleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5387-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-141">-Name</span><span class="sxs-lookup"><span data-stu-id="e5387-141">-Name</span></span>
<span data-ttu-id="e5387-142">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="e5387-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-143">-Primär</span><span class="sxs-lookup"><span data-stu-id="e5387-143">-Primary</span></span>
<span data-ttu-id="e5387-144">Gibt die primäre IP-Konfiguration für den Fall an, dass die Netzwerkschnittstelle über mehr als eine IP-Konfiguration verfügt.</span><span class="sxs-lookup"><span data-stu-id="e5387-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="e5387-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e5387-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="e5387-146">Geben Sie die IP-Konfiguration für private IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="e5387-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="e5387-147">Die Standardeinstellung wird als IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5387-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="e5387-148">Mögliche Werte sind: "IPv4" und "IPv6".</span><span class="sxs-lookup"><span data-stu-id="e5387-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="e5387-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e5387-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="e5387-150">Das Leerlauftimeout der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5387-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e5387-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="e5387-152">Der Name der Konfiguration der PublicIP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e5387-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e5387-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="e5387-154">Geben Sie die IP-Konfiguration für die öffentliche IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="e5387-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="e5387-155">Die Standardeinstellung wird als IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5387-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="e5387-156">Mögliche Werte sind: "IPv4" und "IPv6".</span><span class="sxs-lookup"><span data-stu-id="e5387-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="e5387-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="e5387-157">-PublicIPPrefix</span></span>
<span data-ttu-id="e5387-158">Die ID des öffentlichen IP-Präfixes</span><span class="sxs-lookup"><span data-stu-id="e5387-158">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="e5387-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e5387-159">-SubnetId</span></span>
<span data-ttu-id="e5387-160">Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="e5387-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5387-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5387-161">-Confirm</span></span>
<span data-ttu-id="e5387-162">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5387-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5387-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5387-163">-WhatIf</span></span>
<span data-ttu-id="e5387-164">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5387-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5387-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5387-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5387-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5387-166">CommonParameters</span></span>
<span data-ttu-id="e5387-167">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5387-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5387-168">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5387-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5387-169">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5387-169">INPUTS</span></span>

### <span data-ttu-id="e5387-170">System.String</span><span class="sxs-lookup"><span data-stu-id="e5387-170">System.String</span></span>

### <span data-ttu-id="e5387-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e5387-171">System.String[]</span></span>

### <span data-ttu-id="e5387-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e5387-172">System.Int32</span></span>

### <span data-ttu-id="e5387-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="e5387-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="e5387-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5387-174">OUTPUTS</span></span>

### <span data-ttu-id="e5387-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5387-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="e5387-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e5387-176">NOTES</span></span>

## <span data-ttu-id="e5387-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e5387-177">RELATED LINKS</span></span>

[<span data-ttu-id="e5387-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5387-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


