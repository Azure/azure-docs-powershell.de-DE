---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: acb4496cc9413d6b056b56fe4dbb80a99dee0706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820652"
---
# <span data-ttu-id="f54a8-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="f54a8-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="f54a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f54a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f54a8-103">Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="f54a8-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="f54a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f54a8-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f54a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f54a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f54a8-106">Das Cmdlet **New-AzVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f54a8-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f54a8-107">Geben Sie die Konfiguration dieses Cmdlets als *IPKonfigurationsdateiAddress* -Parameter des Add-AzVmssNetworkInterfaceConfiguration-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="f54a8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f54a8-108">EXAMPLES</span></span>

### <span data-ttu-id="f54a8-109">Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f54a8-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="f54a8-110">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="f54a8-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="f54a8-111">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f54a8-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f54a8-112">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung mit **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f54a8-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="f54a8-113">Beispiel 2: Erstellen eines IP-Konfigurationsobjekts mit NAT-Pooleinstellungen</span><span class="sxs-lookup"><span data-stu-id="f54a8-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="f54a8-114">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface03 und speichert es dann zur späteren Verwendung in der $IPConfiguration-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f54a8-115">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f54a8-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="f54a8-116">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="f54a8-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="f54a8-117">Der Befehl gibt Werte für die Parameter *LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="f54a8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f54a8-118">PARAMETERS</span></span>

### <span data-ttu-id="f54a8-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f54a8-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="f54a8-120">Gibt ein Array von Verweisen auf die Back-End-Adresspools von Load-Balancern an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="f54a8-121">Ein Skalierungs Satz kann auf Back-End-Adresspools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f54a8-122">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="f54a8-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="f54a8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54a8-123">-DefaultProfile</span></span>
<span data-ttu-id="f54a8-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f54a8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54a8-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f54a8-125">-DnsSetting</span></span>
<span data-ttu-id="f54a8-126">Die DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f54a8-127">Die Domänennamen Beschriftung der DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="f54a8-128">Bei der Verkettung der Domänennamen Beschriftung und des VM-Index handelt es sich um die Domänennamen Bezeichnungen der öffentlichen IP-Adress Ressourcen, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f54a8-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="f54a8-129">-ID</span><span class="sxs-lookup"><span data-stu-id="f54a8-129">-Id</span></span>
<span data-ttu-id="f54a8-130">Gibt eine ID an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="f54a8-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="f54a8-131">-IpTag</span></span>
<span data-ttu-id="f54a8-132">Gibt ein Array von IP-Tag-Objekten an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="f54a8-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="f54a8-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="f54a8-134">Gibt ein Array von Verweisen auf eingehende Netzwerkadressübersetzung (NAT)-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="f54a8-135">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f54a8-136">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="f54a8-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="f54a8-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="f54a8-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="f54a8-138">Gibt ein Array von Verweisen auf eingehende NAT-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="f54a8-139">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="f54a8-140">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="f54a8-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="f54a8-141">-Name</span><span class="sxs-lookup"><span data-stu-id="f54a8-141">-Name</span></span>
<span data-ttu-id="f54a8-142">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="f54a8-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="f54a8-143">– Primär</span><span class="sxs-lookup"><span data-stu-id="f54a8-143">-Primary</span></span>
<span data-ttu-id="f54a8-144">Gibt die primäre IP-Konfiguration an, wenn die Netzwerkschnittstelle mehr als eine IP-Konfiguration aufweist.</span><span class="sxs-lookup"><span data-stu-id="f54a8-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="f54a8-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f54a8-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="f54a8-146">Geben Sie an, dass die IP-Konfiguration entweder IPv4 oder IPv6 ist.</span><span class="sxs-lookup"><span data-stu-id="f54a8-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="f54a8-147">Standard wird als IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="f54a8-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="f54a8-148">Mögliche Werte sind: "IPv4" und "IPv6".</span><span class="sxs-lookup"><span data-stu-id="f54a8-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="f54a8-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f54a8-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="f54a8-150">Das Leerlauftimeout der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f54a8-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="f54a8-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f54a8-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="f54a8-152">Der Konfigurationsname der publicIP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f54a8-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="f54a8-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="f54a8-153">-PublicIPPrefix</span></span>
<span data-ttu-id="f54a8-154">Die ID des öffentlichen IP-Präfixes</span><span class="sxs-lookup"><span data-stu-id="f54a8-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="f54a8-155">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="f54a8-155">-SubnetId</span></span>
<span data-ttu-id="f54a8-156">Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="f54a8-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="f54a8-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f54a8-157">-Confirm</span></span>
<span data-ttu-id="f54a8-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f54a8-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f54a8-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f54a8-159">-WhatIf</span></span>
<span data-ttu-id="f54a8-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f54a8-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f54a8-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f54a8-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f54a8-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54a8-162">CommonParameters</span></span>
<span data-ttu-id="f54a8-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54a8-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54a8-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54a8-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54a8-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f54a8-165">INPUTS</span></span>

### <span data-ttu-id="f54a8-166">System. String</span><span class="sxs-lookup"><span data-stu-id="f54a8-166">System.String</span></span>

### <span data-ttu-id="f54a8-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="f54a8-167">System.String[]</span></span>

### <span data-ttu-id="f54a8-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f54a8-168">System.Int32</span></span>

### <span data-ttu-id="f54a8-169">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="f54a8-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="f54a8-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f54a8-170">OUTPUTS</span></span>

### <span data-ttu-id="f54a8-171">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f54a8-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="f54a8-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="f54a8-172">NOTES</span></span>

## <span data-ttu-id="f54a8-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f54a8-173">RELATED LINKS</span></span>

[<span data-ttu-id="f54a8-174">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f54a8-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


