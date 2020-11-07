---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844448"
---
# <span data-ttu-id="53f7a-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f7a-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="53f7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="53f7a-103">Erstellt eine IP-Konfiguration für eine Netzwerkschnittstelle eines VMSS.</span><span class="sxs-lookup"><span data-stu-id="53f7a-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="53f7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53f7a-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="53f7a-106">Das Cmdlet **New-AzVmssIpConfig** erstellt ein IP-Konfigurationsobjekt für eine Netzwerkschnittstelle eines virtuellen Computer-Skalierungs Satzes (VMSS).</span><span class="sxs-lookup"><span data-stu-id="53f7a-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="53f7a-107">Geben Sie die Konfiguration dieses Cmdlets als *IPKonfigurationsdateiAddress* -Parameter des Add-AzVmssNetworkInterfaceConfiguration-Cmdlets an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="53f7a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53f7a-108">EXAMPLES</span></span>

### <span data-ttu-id="53f7a-109">Beispiel 1: Erstellen eines IP-Konfigurationsobjekts für eine VMSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="53f7a-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="53f7a-110">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="53f7a-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="53f7a-111">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="53f7a-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="53f7a-112">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung mit **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="53f7a-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="53f7a-113">Beispiel 2: Erstellen eines IP-Konfigurationsobjekts mit NAT-Pooleinstellungen</span><span class="sxs-lookup"><span data-stu-id="53f7a-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="53f7a-114">Dieser Befehl erstellt ein IP-Konfigurationsobjekt mit dem Namen ContosoVmssInterface03 und speichert es dann zur späteren Verwendung in der $IPConfiguration-Variablen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="53f7a-115">Der Befehl verwendet eine zuvor definierte Subnetz-ID, die in $SubnetId gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="53f7a-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="53f7a-116">Der Befehl speichert die Konfigurationseinstellungen in der $IPConfiguration-Variablen für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="53f7a-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="53f7a-117">Der Befehl gibt Werte für die Parameter *LoadBalancerInboundNatPoolsId* und *LoadBalancerBackendAddressPoolsId* an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="53f7a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="53f7a-118">PARAMETERS</span></span>

### <span data-ttu-id="53f7a-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="53f7a-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="53f7a-120">Gibt ein Array von Verweisen auf die Back-End-Adresspools von Load-Balancern an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="53f7a-121">Ein Skalierungs Satz kann auf Back-End-Adresspools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="53f7a-122">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="53f7a-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f7a-123">-DefaultProfile</span></span>
<span data-ttu-id="53f7a-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53f7a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="53f7a-125">-DnsSetting</span></span>
<span data-ttu-id="53f7a-126">Die DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="53f7a-127">Die Domänennamen Beschriftung der DNS-Einstellungen, die auf die publicIP-Adressen angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="53f7a-128">Bei der Verkettung der Domänennamen Beschriftung und des VM-Index handelt es sich um die Domänennamen Bezeichnungen der öffentlichen IP-Adress Ressourcen, die erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="53f7a-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-129">-ID</span><span class="sxs-lookup"><span data-stu-id="53f7a-129">-Id</span></span>
<span data-ttu-id="53f7a-130">Gibt eine ID an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-130">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="53f7a-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="53f7a-132">Gibt ein Array von Verweisen auf eingehende Netzwerkadressübersetzung (NAT)-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="53f7a-133">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="53f7a-134">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="53f7a-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="53f7a-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="53f7a-136">Gibt ein Array von Verweisen auf eingehende NAT-Pools der Lastenausgleichs Anlagen an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="53f7a-137">Ein Skalierungs Satz kann auf eingehende NAT-Pools eines öffentlichen und eines internen Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="53f7a-138">Mehrere Skalensätze können nicht dasselbe Lastenausgleichsmodul verwenden.</span><span class="sxs-lookup"><span data-stu-id="53f7a-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-139">-Name</span><span class="sxs-lookup"><span data-stu-id="53f7a-139">-Name</span></span>
<span data-ttu-id="53f7a-140">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="53f7a-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-141">– Primär</span><span class="sxs-lookup"><span data-stu-id="53f7a-141">-Primary</span></span>
<span data-ttu-id="53f7a-142">Gibt die primäre IP-Konfiguration an, wenn die Netzwerkschnittstelle mehr als eine IP-Konfiguration aufweist.</span><span class="sxs-lookup"><span data-stu-id="53f7a-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="53f7a-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="53f7a-144">Geben Sie an, dass die IP-Konfiguration entweder IPv4 oder IPv6 ist.</span><span class="sxs-lookup"><span data-stu-id="53f7a-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="53f7a-145">Standard wird als IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="53f7a-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="53f7a-146">Mögliche Werte sind: "IPv4" und "IPv6".</span><span class="sxs-lookup"><span data-stu-id="53f7a-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="53f7a-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="53f7a-148">Das Leerlauftimeout der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="53f7a-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="53f7a-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="53f7a-150">Der Konfigurationsname der publicIP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="53f7a-150">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-151">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="53f7a-151">-SubnetId</span></span>
<span data-ttu-id="53f7a-152">Gibt die Subnetz-ID an, in der die Konfiguration die VMSS-Netzwerkschnittstelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="53f7a-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-153">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53f7a-153">-Confirm</span></span>
<span data-ttu-id="53f7a-154">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53f7a-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f7a-155">-WhatIf</span></span>
<span data-ttu-id="53f7a-156">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53f7a-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53f7a-157">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53f7a-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f7a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f7a-158">CommonParameters</span></span>
<span data-ttu-id="53f7a-159">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f7a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f7a-160">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f7a-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f7a-161">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53f7a-161">INPUTS</span></span>

### <span data-ttu-id="53f7a-162">Keine</span><span class="sxs-lookup"><span data-stu-id="53f7a-162">None</span></span>
<span data-ttu-id="53f7a-163">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="53f7a-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="53f7a-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53f7a-164">OUTPUTS</span></span>

### <span data-ttu-id="53f7a-165">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f7a-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="53f7a-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="53f7a-166">NOTES</span></span>

## <span data-ttu-id="53f7a-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53f7a-167">RELATED LINKS</span></span>

[<span data-ttu-id="53f7a-168">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f7a-168">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


