---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 9c49fd381e1f63d60332eb42759cfb9dd187fbf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480454"
---
# <span data-ttu-id="a3455-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a3455-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="a3455-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3455-102">SYNOPSIS</span></span>
<span data-ttu-id="a3455-103">Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="a3455-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3455-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3455-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3455-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3455-105">DESCRIPTION</span></span>
<span data-ttu-id="a3455-106">Das Cmdlet **New-AzureRmVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="a3455-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="a3455-107">Geben Sie die Konfiguration dieses Cmdlets als *IPKonfigurationsdateiAddress* -Parameter des Add-AzureRmVmssNetworkInterfaceConfiguration-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="a3455-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="a3455-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3455-108">EXAMPLES</span></span>

### <span data-ttu-id="a3455-109">Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a3455-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="a3455-110">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="a3455-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="a3455-111">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a3455-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a3455-112">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung mit **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="a3455-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="a3455-113">Beispiel 2: Erstellen eines IP-Konfigurationsobjekts mit NAT-Pooleinstellungen</span><span class="sxs-lookup"><span data-stu-id="a3455-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="a3455-114">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface03 und speichert es dann zur späteren Verwendung in der $IPConfiguration-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3455-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a3455-115">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a3455-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="a3455-116">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="a3455-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="a3455-117">Der Befehl gibt Werte für die Parameter *LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.</span><span class="sxs-lookup"><span data-stu-id="a3455-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="a3455-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3455-118">PARAMETERS</span></span>

### <span data-ttu-id="a3455-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a3455-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="a3455-120">Gibt ein Array von Verweisen auf die Back-End-Adresspools von Load-Balancern an.</span><span class="sxs-lookup"><span data-stu-id="a3455-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="a3455-121">Ein Skalierungs Satz kann auf Back-End-Adresspools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="a3455-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a3455-122">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3455-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a3455-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3455-123">-DefaultProfile</span></span>
<span data-ttu-id="a3455-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3455-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3455-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="a3455-125">-DnsSetting</span></span>
<span data-ttu-id="a3455-126">Die DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3455-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a3455-127">Die Domänennamen Beschriftung der DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a3455-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="a3455-128">Bei der Verkettung der Domänennamen Beschriftung und des VM-Index handelt es sich um die Domänennamen Bezeichnungen der öffentlichen IP-Adress Ressourcen, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a3455-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="a3455-129">-ID</span><span class="sxs-lookup"><span data-stu-id="a3455-129">-Id</span></span>
<span data-ttu-id="a3455-130">Gibt eine ID an.</span><span class="sxs-lookup"><span data-stu-id="a3455-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="a3455-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="a3455-131">-IpTag</span></span>
<span data-ttu-id="a3455-132">Gibt ein Array von IP-Tag-Objekten an.</span><span class="sxs-lookup"><span data-stu-id="a3455-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="a3455-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="a3455-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="a3455-134">Gibt ein Array von Verweisen auf eingehende Netzwerkadressübersetzung (NAT)-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="a3455-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="a3455-135">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="a3455-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a3455-136">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3455-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a3455-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="a3455-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="a3455-138">Gibt ein Array von Verweisen auf eingehende NAT-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="a3455-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="a3455-139">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="a3455-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="a3455-140">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3455-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="a3455-141">-Name</span><span class="sxs-lookup"><span data-stu-id="a3455-141">-Name</span></span>
<span data-ttu-id="a3455-142">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a3455-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="a3455-143">– Primär</span><span class="sxs-lookup"><span data-stu-id="a3455-143">-Primary</span></span>
<span data-ttu-id="a3455-144">Gibt die primäre IP-Konfiguration an, wenn die Netzwerkschnittstelle mehr als eine IP-Konfiguration aufweist.</span><span class="sxs-lookup"><span data-stu-id="a3455-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="a3455-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a3455-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="a3455-146">Geben Sie an, dass die IP-Konfiguration entweder IPv4 oder IPv6 ist.</span><span class="sxs-lookup"><span data-stu-id="a3455-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="a3455-147">Standard wird als IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3455-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="a3455-148">Mögliche Werte sind: "IPv4" und "IPv6".</span><span class="sxs-lookup"><span data-stu-id="a3455-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="a3455-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a3455-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="a3455-150">Das Leerlauftimeout der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a3455-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="a3455-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a3455-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="a3455-152">Der Konfigurationsname der publicIP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a3455-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="a3455-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="a3455-153">-PublicIPPrefix</span></span>
<span data-ttu-id="a3455-154">Die ID des öffentlichen IP-Präfixes</span><span class="sxs-lookup"><span data-stu-id="a3455-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="a3455-155">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a3455-155">-SubnetId</span></span>
<span data-ttu-id="a3455-156">Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3455-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="a3455-157">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3455-157">-Confirm</span></span>
<span data-ttu-id="a3455-158">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3455-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3455-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3455-159">-WhatIf</span></span>
<span data-ttu-id="a3455-160">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3455-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3455-161">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3455-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3455-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3455-162">CommonParameters</span></span>
<span data-ttu-id="a3455-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3455-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3455-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3455-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3455-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3455-165">INPUTS</span></span>

### <span data-ttu-id="a3455-166">System. String</span><span class="sxs-lookup"><span data-stu-id="a3455-166">System.String</span></span>

### <span data-ttu-id="a3455-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="a3455-167">System.String[]</span></span>

### <span data-ttu-id="a3455-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a3455-168">System.Int32</span></span>

### <span data-ttu-id="a3455-169">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="a3455-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="a3455-170">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3455-170">OUTPUTS</span></span>

### <span data-ttu-id="a3455-171">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3455-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="a3455-172">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3455-172">NOTES</span></span>

## <span data-ttu-id="a3455-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3455-173">RELATED LINKS</span></span>

[<span data-ttu-id="a3455-174">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3455-174">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


