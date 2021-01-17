---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372642"
---
# <span data-ttu-id="13501-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-101">New-AzVmss</span></span>

## <span data-ttu-id="13501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13501-102">SYNOPSIS</span></span>
<span data-ttu-id="13501-103">Erstellt einen VMSS.</span><span class="sxs-lookup"><span data-stu-id="13501-103">Creates a VMSS.</span></span>

## <span data-ttu-id="13501-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13501-104">SYNTAX</span></span>

### <span data-ttu-id="13501-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="13501-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13501-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="13501-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13501-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13501-107">DESCRIPTION</span></span>
<span data-ttu-id="13501-108">Das **Cmdlet "New-AzVmss"** erstellt einen Virtual Machine Scale Set (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="13501-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="13501-109">Verwenden Sie den einfachen Parametersatz `SimpleParameterSet` () zum schnellen Erstellen eines vorkonsenten VMSS und zugeordneter Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="13501-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="13501-110">Verwenden Sie den Standardparametersatz ( ) für anspruchsvollere Szenarien, in denen Sie jede Komponente des VMSS und jede zugeordnete Ressource vor der Erstellung exakt `DefaultParameter` konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="13501-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="13501-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13501-111">EXAMPLES</span></span>

### <span data-ttu-id="13501-112">Beispiel 1: Erstellen Sie einen VMSS mithilfe der **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="13501-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="13501-113">Mit dem oben genannten Befehl wird Folgendes mit dem Namen `$vmssName` erstellt:</span><span class="sxs-lookup"><span data-stu-id="13501-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="13501-114">Eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="13501-114">A Resource Group</span></span>
* <span data-ttu-id="13501-115">Ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="13501-115">A virtual network</span></span>
* <span data-ttu-id="13501-116">Ein Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="13501-116">A load balancer</span></span>
* <span data-ttu-id="13501-117">Eine öffentliche IP</span><span class="sxs-lookup"><span data-stu-id="13501-117">A public IP</span></span>
* <span data-ttu-id="13501-118">vmSS mit 2 Instanzen</span><span class="sxs-lookup"><span data-stu-id="13501-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="13501-119">Das für die VMs in der VMSS ausgewählte Standardbild ist `2016-Datacenter Windows Server` und die SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="13501-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="13501-120">Beispiel 2: Erstellen Sie einen VMSS mithilfe der **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="13501-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="13501-121">Im komplexen Beispiel oben wird ein VMSS erstellt. Im Folgenden wird erläutert, was passiert:</span><span class="sxs-lookup"><span data-stu-id="13501-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="13501-122">Mit dem ersten Befehl wird eine Ressourcengruppe mit dem angegebenen Namen und Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="13501-123">Der zweite Befehl verwendet das **Cmdlet "New-AzStorageAccount",** um ein Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13501-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="13501-124">Der dritte Befehl verwendet dann das **Get-AzStorageAccount-Cmdlet,** um das im zweiten Befehl erstellte Speicherkonto zu erhalten, und speichert das Ergebnis in der $STOAccount Variable.</span><span class="sxs-lookup"><span data-stu-id="13501-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="13501-125">Der fünfte Befehl verwendet das **Cmdlet "New-AzVirtualNetworkSubnetConfig"** zum Erstellen eines Subnetzes und speichert das Ergebnis in der Variablen namens $SubNet.</span><span class="sxs-lookup"><span data-stu-id="13501-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="13501-126">Der sechste Befehl verwendet das **Cmdlet "New-AzVirtualNetwork",** um ein virtuelles Netzwerk zu erstellen, und speichert das Ergebnis in der Variablen namens $VNet.</span><span class="sxs-lookup"><span data-stu-id="13501-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="13501-127">Der siebte Befehl verwendet **"Get-AzVirtualNetwork",** um Informationen über das virtuelle Netzwerk zu erhalten, das im sechsten Befehl erstellt wurde, und speichert die Informationen in der Variablen namens $VNet.</span><span class="sxs-lookup"><span data-stu-id="13501-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="13501-128">Der achte und neunte Befehl verwendet **"New-AzPublicIpAddress"** und **"Get- AzureRmPublicIpAddress"** zum Erstellen und Erhalten von Informationen von dieser öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="13501-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="13501-129">Die Befehle speichern die Informationen in der Variablen namens $PubIP.</span><span class="sxs-lookup"><span data-stu-id="13501-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="13501-130">Der zehnte Befehl verwendet das Cmdlet **"New- AzureRmLoadBalancerFrontendIpConfig"** zum Erstellen eines frontend-Lastenausgleichs und speichert das Ergebnis in der Variablen namens $Frontend.</span><span class="sxs-lookup"><span data-stu-id="13501-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="13501-131">Der elfte Befehl verwendet **"New-AzLoadBalancerBackendAddressPoolConfig",** um eine Back-End-Adresspoolkonfiguration zu erstellen, und speichert das Ergebnis in der Variablen namens $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="13501-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="13501-132">Der zwölfte Befehl verwendet **"New-AzLoadBalancerProbeConfig",** um eine Sonde zu erstellen, und speichert die Probeinformationen in der Variablen namens $Probe.</span><span class="sxs-lookup"><span data-stu-id="13501-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="13501-133">Der zwölfte Befehl verwendet das **Cmdlet "New-AzLoadBalancerInboundNatPoolConfig",** um eine Konfiguration des NAT (Bound Network Address Translation) für den eingehenden Netzwerkadressenpool zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13501-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="13501-134">Der vierzehnte Befehl verwendet **"New-AzLoadBalancerRuleConfig",** um eine Load Balancer-Regelkonfiguration zu erstellen, und speichert das Ergebnis in der Variablen namens $LBRule.</span><span class="sxs-lookup"><span data-stu-id="13501-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="13501-135">Der fünfzehnte Befehl verwendet das **Cmdlet "New-AzLoadBalancer",** um einen Lastenausgleich zu erstellen, und speichert das Ergebnis in der Variablen namens $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="13501-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="13501-136">Der 16. Befehl verwendet **"Get-AzLoadBalancer",** um Informationen zum Lastenausgleich zu erhalten, der im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen namens $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="13501-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="13501-137">Der siebzehnte Befehl verwendet das **Cmdlet "New-AzVmssIPConfig"** zum Erstellen einer VMSS-IP-Konfiguration und speichert die Informationen in der Variablen namens $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="13501-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="13501-138">Der 18. Befehl verwendet das **Cmdlet "New-AzVmssConfig"** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="13501-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="13501-139">Der befehl "th" verwendet das **Cmdlet "New-AzVmss"** zum Erstellen der VMSS.</span><span class="sxs-lookup"><span data-stu-id="13501-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="13501-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13501-140">PARAMETERS</span></span>

### <span data-ttu-id="13501-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="13501-141">-AllocationMethod</span></span>
<span data-ttu-id="13501-142">Zuweisungsmethode für die öffentliche IP-Adresse des Skalierungssatzs (statisch oder dynamisch).</span><span class="sxs-lookup"><span data-stu-id="13501-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="13501-143">Wenn kein Wert angegeben wird, ist die Zuordnung statisch.</span><span class="sxs-lookup"><span data-stu-id="13501-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13501-144">-AsJob</span></span>
<span data-ttu-id="13501-145">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="13501-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="13501-146">-Back-EndPoolName</span><span class="sxs-lookup"><span data-stu-id="13501-146">-BackendPoolName</span></span>
<span data-ttu-id="13501-147">Der Name des Back-End-Adresspools, der im Lastenausgleich für diesen Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="13501-148">Wenn kein Wert angegeben wird, wird ein neuer Back-End-Pool mit demselben Namen wie der Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-149">-Back-EndPort</span><span class="sxs-lookup"><span data-stu-id="13501-149">-BackendPort</span></span>
<span data-ttu-id="13501-150">Back-End-Portnummern, die vom Lastensaldo für Skalierungssatz verwendet werden, um mit VMs im Skalierungssatz zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="13501-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="13501-151">Wenn keine Werte angegeben werden, werden die Ports 3389 und 5985 für Windows VMS und Port 22 für Linux-VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="13501-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="13501-152">-Credential</span></span>
<span data-ttu-id="13501-153">Die Administratoranmeldeinformationen (Benutzername und Kennwort) für VMs in diesem Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="13501-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="13501-155">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="13501-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13501-156">-DefaultProfile</span></span>
<span data-ttu-id="13501-157">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13501-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13501-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="13501-158">-DomainNameLabel</span></span>
<span data-ttu-id="13501-159">Die Domänennamenbezeichnung für den öffentlichen Fully-Qualified Domänennamen (FQDN) für diesen Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="13501-160">Dies ist die erste Komponente des Domänennamens, die dem Skalierungssatz automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="13501-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="13501-161">Automatisch zugewiesene Domänennamen verwenden das Formular ( <DomainNameLabel> <Location> . . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="13501-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="13501-162">Wenn kein Wert angegeben wird, ist die standardmäßige Domänennamensbezeichnung die Verkettung von <ScaleSetName> <ResourceGroupName> und.</span><span class="sxs-lookup"><span data-stu-id="13501-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="13501-163">-EnableUltraSSD</span></span>
<span data-ttu-id="13501-164">Verwenden Sie die UltraSSD-Datenträger für die VMs im Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="13501-165">-EncryptionAtHost</span></span>
<span data-ttu-id="13501-166">Dieser Parameter aktiviert die Verschlüsselung für alle Datenträger, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="13501-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="13501-167">Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="13501-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="13501-168">-EvictionPolicy</span></span>
<span data-ttu-id="13501-169">Die Entfernungsrichtlinie für den Skalierungssatz für virtuelle Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="13501-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="13501-170">Nur unterstützte Werte sind "Deallocate" und "Delete".</span><span class="sxs-lookup"><span data-stu-id="13501-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="13501-171">-FrontendPoolName</span></span>
<span data-ttu-id="13501-172">Der Name des Frontend-Adresspools, der im Lastenausgleichsmaßstab verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="13501-173">Wenn kein Wert angegeben wird, wird ein neuer Frontend-Adresspool mit demselben Namen wie der Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="13501-174">-HostGroupId</span></span>
<span data-ttu-id="13501-175">Gibt die dedizierte Hostgruppe an, in der sich der Skalierungssatz des virtuellen Computers befindet.</span><span class="sxs-lookup"><span data-stu-id="13501-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="13501-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="13501-176">-ImageName</span></span>
<span data-ttu-id="13501-177">Der Name des Bilds für VMs in diesem Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="13501-178">Wenn kein Wert angegeben wird, wird das Bild "Windows Server 2016 DataCenter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="13501-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="13501-179">-InstanceCount</span></span>
<span data-ttu-id="13501-180">Die Anzahl von VM-Bildern im Scale Set.</span><span class="sxs-lookup"><span data-stu-id="13501-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="13501-181">Wenn kein Wert angegeben wird, werden zwei Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="13501-182">-LoadBalancerName</span></span>
<span data-ttu-id="13501-183">Der Name des Lastenausgleichs, der mit diesem Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="13501-184">Wenn kein Wert angegeben ist, wird ein neuer Lastenausgleich mit demselben Namen wie der Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-185">-Location</span><span class="sxs-lookup"><span data-stu-id="13501-185">-Location</span></span>
<span data-ttu-id="13501-186">Der Azure-Speicherort, an dem dieser Skalierungssatz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="13501-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="13501-187">Wenn kein Wert angegeben wird, wird der Speicherort vom Speicherort anderer Ressourcen abgeleitet, auf die in den Parametern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="13501-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="13501-188">-MaxPrice</span></span>
<span data-ttu-id="13501-189">Der maximale Preis für die Abrechnung eines Skalierungssets für virtuelle Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="13501-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="13501-190">-NatBackendPort</span></span>
<span data-ttu-id="13501-191">Back-End-Port für die eingehende Netzwerkadressenübersetzung.</span><span class="sxs-lookup"><span data-stu-id="13501-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="13501-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="13501-193">Anzahl der Fehlerdomänen für jede Platzierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="13501-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13501-194">-Priority</span><span class="sxs-lookup"><span data-stu-id="13501-194">-Priority</span></span>
<span data-ttu-id="13501-195">Die Priorität für den virtuellen Computer im Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="13501-196">Nur unterstützte Werte sind "Regular", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="13501-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="13501-197">"Regular" ist für normale virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="13501-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="13501-198">"Spot" ist für virtuelle Spotcomputer.</span><span class="sxs-lookup"><span data-stu-id="13501-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="13501-199">"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="13501-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="13501-200">Verwenden Sie "Spot" anstelle von "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="13501-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="13501-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="13501-202">Die Ressourcen-ID der Näherungsplatzierungsgruppe, die für diesen Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="13501-203">-PublicIpAddressName</span></span>
<span data-ttu-id="13501-204">Der Name der öffentlichen IP-Adresse, die mit diesem Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="13501-205">Wenn kein Wert angegeben wird, wird eine neue öffentliche IPAddress mit demselben Namen wie der Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13501-206">-ResourceGroupName</span></span>
<span data-ttu-id="13501-207">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="13501-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="13501-208">Wenn kein Wert angegeben wird, wird eine neue Ressourcengruppe mit demselben Namen wie der Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13501-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="13501-209">-ScaleInPolicy</span></span>
<span data-ttu-id="13501-210">Die Regeln, die beim Skalieren in einem Skalierungssatz für einen virtuellen Computer zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="13501-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="13501-211">Mögliche Werte sind: "Default", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="13501-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="13501-212">"Standard", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen, wenn es sich um einen standardmäßigen Skalierungssatz handelt.</span><span class="sxs-lookup"><span data-stu-id="13501-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="13501-213">Anschließend wird sie so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="13501-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="13501-214">Innerhalb jeder Fault Domain sind die zum Entfernen ausgewählten virtuellen Computer die neuesten, die nicht vor scale-in geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="13501-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="13501-215">"OldestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor "scale-in" geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="13501-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="13501-216">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="13501-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="13501-217">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="13501-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="13501-218">"NewestVM", wenn ein Skalierungssatz für einen virtuellen Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor scale-in geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="13501-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="13501-219">Bei tiernalen Skalierungssätzen virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="13501-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="13501-220">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="13501-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="13501-221">-SecurityGroupName</span></span>
<span data-ttu-id="13501-222">Der Name der Netzwerksicherheitsgruppe, die auf diesen Skalierungssatz angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="13501-223">Wenn kein Wert angegeben wird, wird eine Standardmäßige Netzwerksicherheitsgruppe mit demselben Namen wie der Skalierungssatz erstellt und auf den Skalierungssatz angewendet.</span><span class="sxs-lookup"><span data-stu-id="13501-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="13501-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="13501-225">Verwenden Sie diese, um den Skalierungssatz in einer einzelnen Platzierungsgruppe zu erstellen. Der Standardwert ist mehrere Gruppen.</span><span class="sxs-lookup"><span data-stu-id="13501-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="13501-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="13501-227">Gibt an, dass die Erweiterungen nicht für die zusätzlichen überprovisionierten VMs ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="13501-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="13501-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="13501-229">Das Adresspräfix des Subnetzes, das von diesem ScaleSet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13501-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="13501-230">Die Standardeinstellungen für Subnetze (192.168.1.0/24) werden angewendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13501-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="13501-231">-SubnetName</span></span>
<span data-ttu-id="13501-232">Der Name des Subnetzes, das mit diesem Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="13501-233">Es wird ein neues Subnetz mit demselben Namen wie der Skalierungssatz erstellt, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13501-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="13501-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="13501-235">Wenn der Parameter vorhanden ist, wird den VM(s) im Skalierungssatz (sind) eine verwaltete Systemidentität zugewiesen, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="13501-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="13501-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="13501-237">Der Upgraderichtlinienmodus für Instanzen der virtuellen Computer in diesem Scale Set.</span><span class="sxs-lookup"><span data-stu-id="13501-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="13501-238">In der Upgraderichtlinie können automatische, manuelle oder Rollupgrade festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13501-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="13501-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="13501-240">Der Name einer verwalteten Dienstidentität, die den VM(s) im Skalierungssatz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="13501-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="13501-242">Gibt das **VirtualMachineScaleSet-Objekt** an, das die Eigenschaften der VMSS enthält, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="13501-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13501-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="13501-243">-VirtualNetworkName</span></span>
<span data-ttu-id="13501-244">Der Name für das virtuelle Netzwerk, das mit diesem Skalierungssatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="13501-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="13501-245">Wenn kein Wert angegeben wird, wird ein neues virtuelles Netzwerk mit demselben Namen wie die Skalierungssatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="13501-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="13501-246">-VMScaleSetName</span></span>
<span data-ttu-id="13501-247">Gibt den Namen der VMSS an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="13501-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13501-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="13501-248">-VmSize</span></span>
<span data-ttu-id="13501-249">Die Größe der VM-Instanzen in diesem Skalierungssatz.</span><span class="sxs-lookup"><span data-stu-id="13501-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="13501-250">Eine Standardgröße (Standard_DS1_v2) wird verwendet, wenn keine Größe angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="13501-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="13501-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="13501-252">Das Adresspräfix für das virtuelle Netzwerk, das mit diesem Skalierungssatz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="13501-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="13501-253">Standardmäßige Einstellungen für das Präfix für virtuelle Netzwerkadressen (192.168.0.0/16) werden verwendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13501-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13501-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="13501-254">-Zone</span></span>
<span data-ttu-id="13501-255">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="13501-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13501-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13501-256">-Confirm</span></span>
<span data-ttu-id="13501-257">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13501-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13501-258">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="13501-258">-WhatIf</span></span>
<span data-ttu-id="13501-259">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13501-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13501-260">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13501-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13501-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13501-261">CommonParameters</span></span>
<span data-ttu-id="13501-262">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13501-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13501-263">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13501-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13501-264">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13501-264">INPUTS</span></span>

### <span data-ttu-id="13501-265">System.String</span><span class="sxs-lookup"><span data-stu-id="13501-265">System.String</span></span>

### <span data-ttu-id="13501-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="13501-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="13501-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="13501-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="13501-268">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13501-268">OUTPUTS</span></span>

### <span data-ttu-id="13501-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="13501-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="13501-270">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13501-270">NOTES</span></span>

## <span data-ttu-id="13501-271">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13501-271">RELATED LINKS</span></span>

[<span data-ttu-id="13501-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="13501-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="13501-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="13501-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="13501-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="13501-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="13501-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="13501-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


