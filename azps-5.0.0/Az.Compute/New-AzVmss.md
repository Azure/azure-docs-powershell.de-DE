---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300777"
---
# <span data-ttu-id="fd7e3-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-101">New-AzVmss</span></span>

## <span data-ttu-id="fd7e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e3-103">Erstellt eine VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-103">Creates a VMSS.</span></span>

## <span data-ttu-id="fd7e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd7e3-104">SYNTAX</span></span>

### <span data-ttu-id="fd7e3-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd7e3-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7e3-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-106">SimpleParameterSet</span></span>
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

## <span data-ttu-id="fd7e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd7e3-107">DESCRIPTION</span></span>
<span data-ttu-id="fd7e3-108">Das Cmdlet **New-AzVmss** erstellt einen virtuellen Computer-Skalierungs Satz (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="fd7e3-109">Verwenden Sie den einfachen Parametersatz ( `SimpleParameterSet` ), um schnell eine vordefinierte VMSS und zugeordnete Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="fd7e3-110">Verwenden Sie den standardmäßigen Parametersatz ( `DefaultParameter` ) für erweiterte Szenarien, wenn Sie jede Komponente des VMSS und jede zugeordnete Ressource vor der Erstellung genau konfigurieren müssen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="fd7e3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd7e3-111">EXAMPLES</span></span>

### <span data-ttu-id="fd7e3-112">Beispiel 1: Erstellen einer VMSS mit der **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fd7e3-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="fd7e3-113">Der obige Befehl erstellt Folgendes mit dem Namen `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="fd7e3-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="fd7e3-114">Eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fd7e3-114">A Resource Group</span></span>
* <span data-ttu-id="fd7e3-115">Ein virtuelles Netzwerk</span><span class="sxs-lookup"><span data-stu-id="fd7e3-115">A virtual network</span></span>
* <span data-ttu-id="fd7e3-116">Ein Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="fd7e3-116">A load balancer</span></span>
* <span data-ttu-id="fd7e3-117">Eine öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="fd7e3-117">A public IP</span></span>
* <span data-ttu-id="fd7e3-118">VMSS mit zwei Instanzen</span><span class="sxs-lookup"><span data-stu-id="fd7e3-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="fd7e3-119">Das für die VMs in der VMSS ausgewählte Standardbild ist `2016-Datacenter Windows Server` und die SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="fd7e3-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="fd7e3-120">Beispiel 2: Erstellen eines VMSS mithilfe der **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fd7e3-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="fd7e3-121">Im obigen komplexen Beispiel wird eine VMSS erstellt, und im folgenden wird erläutert, was passiert:</span><span class="sxs-lookup"><span data-stu-id="fd7e3-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="fd7e3-122">Der erste Befehl erstellt eine Ressourcengruppe mit dem angegebenen Namen und Speicherort.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="fd7e3-123">Der zweite Befehl verwendet das Cmdlet **New-AzStorageAccount** , um ein Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="fd7e3-124">Der dritte Befehl verwendet dann das Cmdlet " **Get-AzStorageAccount** ", um das im zweiten Befehl erstellte Speicherkonto abzurufen, und speichert das Ergebnis in der $STOAccount Variablen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="fd7e3-125">Der fünfte Befehl verwendet das Cmdlet **New-AzVirtualNetworkSubnetConfig** , um ein Subnetz zu erstellen und das Ergebnis in der Variablen mit dem Namen $Subnet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="fd7e3-126">Der sechste Befehl verwendet das Cmdlet **New-AzVirtualNetwork** , um ein virtuelles Netzwerk zu erstellen und das Ergebnis in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="fd7e3-127">Der siebte Befehl verwendet die **Get-AzVirtualNetwork-** Funktion, um Informationen zu dem im sechsten Befehl erstellten virtuellen Netzwerk abzurufen und die Informationen in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="fd7e3-128">Der achte und neunte Befehl verwendet die **New-AzPublicIpAddress** und **Get-AzureRmPublicIpAddress** , um Informationen aus dieser öffentlichen IP-Adresse zu erstellen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="fd7e3-129">Die Befehle speichern die Informationen in der Variablen mit dem Namen $PubIP.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="fd7e3-130">Der zehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** , um ein Frontend-Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $Frontend zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="fd7e3-131">Der elfte Befehl verwendet das **New-AzLoadBalancerBackendAddressPoolConfig-Steuer** System, um eine Konfiguration des Back-End-Adresspools zu erstellen und das Ergebnis in der Variablen mit dem Namen $BackendAddressPool zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="fd7e3-132">Der zwölfte Befehl verwendet die **New-AzLoadBalancerProbeConfig-** Funktion, um einen Prüfpunkt zu erstellen und die Prüfpunktinformationen in der Variablen mit dem Namen $Probe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="fd7e3-133">Der dreizehnte Befehl verwendet das Cmdlet **New-AzLoadBalancerInboundNatPoolConfig** , um eine eingehende Netzwerkadressübersetzung (Network Address Translation, NAT) für den Lastenausgleich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="fd7e3-134">Der vierzehnte Befehl verwendet die **New-AzLoadBalancerRuleConfig-** Funktion, um eine Load Balancer-Regelkonfiguration zu erstellen und das Ergebnis in der Variablen mit dem Namen $LBRule zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="fd7e3-135">Der fünfzehnte Befehl verwendet das Cmdlet **New-AzLoadBalancer** , um ein Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $ActualLb zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="fd7e3-136">Der sechzehnte Befehl verwendet die **Get-AzLoadBalancer-** Funktion, um Informationen über das Load Balancer abzurufen, das im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen mit dem Namen $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="fd7e3-137">Der Befehl "siebzehnte" verwendet das Cmdlet " **New-AzVmssIPConfig** ", um eine VMSS-IP-Konfiguration zu erstellen und die Informationen in der Variablen mit dem Namen $IPCfg zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="fd7e3-138">Der achtzehnte Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="fd7e3-139">Der neunzehnte Befehl verwendet das Cmdlet **New-AzVmss** zum Erstellen des VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="fd7e3-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd7e3-140">PARAMETERS</span></span>

### <span data-ttu-id="fd7e3-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fd7e3-141">-AllocationMethod</span></span>
<span data-ttu-id="fd7e3-142">Zuordnungsmethode für die öffentliche IP-Adresse des Skalierungs Satzes (statisch oder dynamisch).</span><span class="sxs-lookup"><span data-stu-id="fd7e3-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="fd7e3-143">Wenn kein Wert angegeben wird, ist die Zuweisung statisch.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="fd7e3-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7e3-144">-AsJob</span></span>
<span data-ttu-id="fd7e3-145">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fd7e3-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-146">-BackendPoolName</span></span>
<span data-ttu-id="fd7e3-147">Der Name des im Load Balancer für diesen Skalierungs Satz zu verwendenden Back-End-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="fd7e3-148">Wenn kein Wert angegeben wird, wird ein neuer Back-End-Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fd7e3-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fd7e3-149">-BackendPort</span></span>
<span data-ttu-id="fd7e3-150">Back-End-Portnummern, die vom Scale-Satz Load Balancer für die Kommunikation mit VMS im Skalierungs Satz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="fd7e3-151">Wenn keine Werte angegeben werden, werden Ports 3389 und 5985 für Windows-VMS verwendet, und Port 22 wird für Linux-VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="fd7e3-152">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="fd7e3-152">-Credential</span></span>
<span data-ttu-id="fd7e3-153">Die Administratoranmeldeinformationen (Benutzername und Kennwort) für VMs in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="fd7e3-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="fd7e3-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="fd7e3-155">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="fd7e3-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e3-156">-DefaultProfile</span></span>
<span data-ttu-id="fd7e3-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7e3-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fd7e3-158">-DomainNameLabel</span></span>
<span data-ttu-id="fd7e3-159">Die Bezeichnung für den Domänennamen für den öffentlichen Fully-Qualified Domänennamen (Fully Domain Name, FQDN) für diesen Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="fd7e3-160">Dies ist die erste Komponente des Domänennamens, die dem Skalierungs Satz automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="fd7e3-161">Automatisch zugewiesene Domänennamen verwenden das Formular ( <DomainNameLabel> . <Location> . cloudapp.Azure.com).</span><span class="sxs-lookup"><span data-stu-id="fd7e3-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="fd7e3-162">Wenn kein Wert angegeben wird, ist die standardmäßige Domänennamen Beschriftung die Verkettung von <ScaleSetName> und <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="fd7e3-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="fd7e3-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fd7e3-163">-EnableUltraSSD</span></span>
<span data-ttu-id="fd7e3-164">Verwenden Sie UltraSSD-Datenträger für die VMs im Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="fd7e3-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="fd7e3-165">-EncryptionAtHost</span></span>
<span data-ttu-id="fd7e3-166">Mit diesem Parameter wird die Verschlüsselung für alle Datenträger einschließlich des Ressourcen/Temp-Datenträgers am Host selbst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="fd7e3-167">Standard: die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="fd7e3-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd7e3-168">-EvictionPolicy</span></span>
<span data-ttu-id="fd7e3-169">Die Räumungs Richtlinie für den Skalierungs Satz der virtuellen Maschine mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="fd7e3-170">Nur Unterstützte Werte sind "freigeben" und "Löschen".</span><span class="sxs-lookup"><span data-stu-id="fd7e3-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="fd7e3-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-171">-FrontendPoolName</span></span>
<span data-ttu-id="fd7e3-172">Der Name des zu verwendenden Frontend-Adresspools im Scale-Satz-Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="fd7e3-173">Wenn kein Wert angegeben wird, wird ein neuer Frontend-Adress Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="fd7e3-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="fd7e3-174">-HostGroupId</span></span>
<span data-ttu-id="fd7e3-175">Gibt die dedizierte Hostgruppe an, in der sich der Skalierungs Satz des virtuellen Computers befindet.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="fd7e3-176">-Bildname</span><span class="sxs-lookup"><span data-stu-id="fd7e3-176">-ImageName</span></span>
<span data-ttu-id="fd7e3-177">Der Name des Bilds für VMs in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="fd7e3-178">Wenn kein Wert angegeben wird, wird das Bild "Windows Server 2016 Datacenter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="fd7e3-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fd7e3-179">-InstanceCount</span></span>
<span data-ttu-id="fd7e3-180">Die Anzahl der VM-Bilder im Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="fd7e3-181">Wenn kein Wert angegeben wird, werden 2 Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="fd7e3-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-182">-LoadBalancerName</span></span>
<span data-ttu-id="fd7e3-183">Der Name des Load Balancer, der mit diesem Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="fd7e3-184">Wenn kein Wert angegeben wird, wird ein neues Lastenausgleichsmodul mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="fd7e3-185">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd7e3-185">-Location</span></span>
<span data-ttu-id="fd7e3-186">Die Azure-Position, an der dieser Skalierungs Satz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="fd7e3-187">Wenn kein Wert angegeben wird, wird der Speicherort von dem Speicherort anderer Ressourcen abgeleitet, auf die in den Parametern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="fd7e3-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fd7e3-188">-MaxPrice</span></span>
<span data-ttu-id="fd7e3-189">Der Höchstbetrag für die Abrechnung einer Skalierungs Gruppe für virtuelle Maschinen mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="fd7e3-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="fd7e3-190">-NatBackendPort</span></span>
<span data-ttu-id="fd7e3-191">Back-End-Port für eingehende Netzwerkadressübersetzung.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="fd7e3-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fd7e3-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fd7e3-193">Anzahl der fehlerdomänen für jede Placement-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-193">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="fd7e3-194">-Priorität</span><span class="sxs-lookup"><span data-stu-id="fd7e3-194">-Priority</span></span>
<span data-ttu-id="fd7e3-195">Die Priorität für den virtuellen Computer im Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="fd7e3-196">Nur Unterstützte Werte sind "Normal", "Spot" und "Low".</span><span class="sxs-lookup"><span data-stu-id="fd7e3-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="fd7e3-197">"Normal" ist für normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="fd7e3-198">"Spot" ist für Spot Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="fd7e3-199">"Low" ist auch für Spot Virtual Machine, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="fd7e3-200">Bitte verwenden Sie "Spot" anstelle von "Low".</span><span class="sxs-lookup"><span data-stu-id="fd7e3-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="fd7e3-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fd7e3-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fd7e3-202">Die Ressourcen-ID der für diesen Skalierungs Satz zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="fd7e3-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-203">-PublicIpAddressName</span></span>
<span data-ttu-id="fd7e3-204">Der Name der öffentlichen IP-Adresse, die mit diesem Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="fd7e3-205">Eine neue öffentliche IPAddress mit dem gleichen Namen wie der Skalierungs Satz wird erstellt, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="fd7e3-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-206">-ResourceGroupName</span></span>
<span data-ttu-id="fd7e3-207">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="fd7e3-208">Wenn kein Wert angegeben wird, wird eine neue ResourceGroup mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fd7e3-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fd7e3-209">-ScaleInPolicy</span></span>
<span data-ttu-id="fd7e3-210">Die Regeln, die beim Skalieren in einem Skalierungs Satz einer virtuellen Maschine befolgt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fd7e3-211">Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="fd7e3-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fd7e3-212">"Standard" Wenn der Skalierungs Satz einer virtuellen Maschine skaliert wird, wird der Skalierungs Satz zunächst zonenübergreifend ausbalanciert, wenn es sich um einen Zonal-Skalierungs Satz handelt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fd7e3-213">In diesem Fall werden die fehlerdomänen so weit wie möglich ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fd7e3-214">Innerhalb jeder fehlerdomäne sind die für die Entfernung ausgewählten virtuellen Computer die neuesten, die nicht vor dem Skalieren geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fd7e3-215">"OldestVM" Wenn ein Skalierungs Satz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fd7e3-216">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fd7e3-217">Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fd7e3-218">"NewestVM" Wenn ein Skalierungs Satz für virtuelle Maschinen skaliert wird, werden die neuesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fd7e3-219">Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fd7e3-220">In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="fd7e3-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-221">-SecurityGroupName</span></span>
<span data-ttu-id="fd7e3-222">Der Name der Netzwerksicherheitsgruppe, die auf diesen Skalierungs Satz angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="fd7e3-223">Wenn kein Wert angegeben wird, wird eine standardmäßige Netzwerksicherheitsgruppe mit dem gleichen Namen wie der Skalierungs Satz erstellt und auf den Skalierungs Satz angewendet.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="fd7e3-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fd7e3-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="fd7e3-225">Verwenden Sie diese Einstellung, um den Skalierungs Satz in einer einzelnen Placement-Gruppe zu erstellen, Standard ist mehrere Gruppen</span><span class="sxs-lookup"><span data-stu-id="fd7e3-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="fd7e3-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="fd7e3-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fd7e3-227">Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überlegten VMS ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fd7e3-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd7e3-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="fd7e3-229">Das Adresspräfix des Subnets, das von diesem scaleset verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="fd7e3-230">Standardmäßige subneteinstellungen (192.168.1.0/24) werden angewendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="fd7e3-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-231">-SubnetName</span></span>
<span data-ttu-id="fd7e3-232">Der Name des für diesen Skalierungs Satz zu verwendenden Subnets.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="fd7e3-233">Ein neues Subnetz wird mit dem gleichen Namen wie der Skalierungs Satz erstellt, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="fd7e3-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd7e3-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fd7e3-235">Wenn der Parameter vorhanden ist, wird den virtuellen Computern im Skalierungs Satz eine verwaltete System Identität zugewiesen, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="fd7e3-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fd7e3-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="fd7e3-237">Der Aktualisierungsrichtlinien Modus für VM-Instanzen in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="fd7e3-238">Die Upgrade-Richtlinie kann automatische, manuelle oder parallele Upgrades angeben.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="fd7e3-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd7e3-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="fd7e3-240">Der Name einer verwalteten Dienstidentität, die den VM (n) im Skalierungs Satz zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="fd7e3-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd7e3-242">Gibt das **VirtualMachineScaleSet** -Objekt an, das die Eigenschaften des VMSS enthält, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fd7e3-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-243">-VirtualNetworkName</span></span>
<span data-ttu-id="fd7e3-244">Der Name für das virtuelle Netzwerk, der für diesen Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="fd7e3-245">Wenn kein Wert angegeben wird, wird ein neues virtuelles Netzwerk mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="fd7e3-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fd7e3-246">-VMScaleSetName</span></span>
<span data-ttu-id="fd7e3-247">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fd7e3-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fd7e3-248">-VmSize</span></span>
<span data-ttu-id="fd7e3-249">Die Größe der VM-Instanzen in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="fd7e3-250">Wenn keine Größe angegeben ist, wird eine Standardgröße (Standard_DS1_v2) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="fd7e3-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd7e3-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="fd7e3-252">Das Adresspräfix für das virtuelle Netzwerk, das mit diesem Skalierungs Satz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="fd7e3-253">Standardeinstellungen für das virtuelle Netzwerk Adresspräfix (192.168.0.0/16) werden verwendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="fd7e3-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="fd7e3-254">-Zone</span></span>
<span data-ttu-id="fd7e3-255">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fd7e3-256">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd7e3-256">-Confirm</span></span>
<span data-ttu-id="fd7e3-257">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7e3-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7e3-258">-WhatIf</span></span>
<span data-ttu-id="fd7e3-259">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7e3-260">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7e3-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e3-261">CommonParameters</span></span>
<span data-ttu-id="fd7e3-262">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7e3-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e3-263">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd7e3-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e3-264">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd7e3-264">INPUTS</span></span>

### <span data-ttu-id="fd7e3-265">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7e3-265">System.String</span></span>

### <span data-ttu-id="fd7e3-266">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fd7e3-267">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd7e3-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fd7e3-268">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd7e3-268">OUTPUTS</span></span>

### <span data-ttu-id="fd7e3-269">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd7e3-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fd7e3-270">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd7e3-270">NOTES</span></span>

## <span data-ttu-id="fd7e3-271">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd7e3-271">RELATED LINKS</span></span>

[<span data-ttu-id="fd7e3-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fd7e3-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fd7e3-274">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fd7e3-275">Satz-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fd7e3-276">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fd7e3-277">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fd7e3-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd7e3-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


