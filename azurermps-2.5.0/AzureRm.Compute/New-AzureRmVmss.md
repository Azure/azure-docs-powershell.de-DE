---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
ms.openlocfilehash: f93e05448278e2aaa70ff226a5d3618fdad0e6b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850119"
---
# <span data-ttu-id="a560e-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="a560e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a560e-102">SYNOPSIS</span></span>
<span data-ttu-id="a560e-103">Erstellt eine VMSS.</span><span class="sxs-lookup"><span data-stu-id="a560e-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a560e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a560e-104">SYNTAX</span></span>

### <span data-ttu-id="a560e-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="a560e-105">DefaultParameter (Default)</span></span>
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a560e-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a560e-106">SimpleParameterSet</span></span>
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a560e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a560e-107">DESCRIPTION</span></span>
<span data-ttu-id="a560e-108">Das Cmdlet **New-AzureRmVmss** erstellt einen virtuellen Computer-Skalierungs Satz (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="a560e-108">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="a560e-109">Dieses Cmdlet akzeptiert ein **VirtualMachineScaleSet** -Objekt als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="a560e-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="a560e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a560e-110">EXAMPLES</span></span>

### <span data-ttu-id="a560e-111">Beispiel 1: Erstellen einer VMSS</span><span class="sxs-lookup"><span data-stu-id="a560e-111">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="a560e-112">Im folgenden komplexen Beispiel wird ein VMSS erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="a560e-113">Der erste Befehl erstellt eine Ressourcengruppe mit dem angegebenen Namen und Speicherort.</span><span class="sxs-lookup"><span data-stu-id="a560e-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="a560e-114">Der zweite Befehl verwendet das Cmdlet **New-AzureRmStorageAccount** , um ein Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a560e-114">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="a560e-115">Der dritte Befehl verwendet dann das Cmdlet " **Get-AzureRmStorageAccount** ", um das im zweiten Befehl erstellte Speicherkonto abzurufen, und speichert das Ergebnis in der $STOAccount Variablen.</span><span class="sxs-lookup"><span data-stu-id="a560e-115">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="a560e-116">Der fünfte Befehl verwendet das Cmdlet **New-AzureRmVirtualNetworkSubnetConfig** , um ein Subnetz zu erstellen und das Ergebnis in der Variablen mit dem Namen $Subnet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-116">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="a560e-117">Der sechste Befehl verwendet das Cmdlet **New-AzureRmVirtualNetwork** , um ein virtuelles Netzwerk zu erstellen und das Ergebnis in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-117">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="a560e-118">Der siebte Befehl verwendet die **Get-AzureRmVirtualNetwork-** Funktion, um Informationen zu dem im sechsten Befehl erstellten virtuellen Netzwerk abzurufen und die Informationen in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-118">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="a560e-119">Der achte und neunte Befehl verwendet die **New-AzureRmPublicIpAddress** und **Get-AzureRmPublicIpAddress** , um Informationen aus dieser öffentlichen IP-Adresse zu erstellen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a560e-119">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="a560e-120">Die Befehle speichern die Informationen in der Variablen mit dem Namen $PubIP.</span><span class="sxs-lookup"><span data-stu-id="a560e-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="a560e-121">Der zehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** , um ein Frontend-Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $Frontend zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="a560e-122">Der elfte Befehl verwendet das **New-AzureRmLoadBalancerBackendAddressPoolConfig-Steuer** System, um eine Konfiguration des Back-End-Adresspools zu erstellen und das Ergebnis in der Variablen mit dem Namen $BackendAddressPool zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-122">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="a560e-123">Der zwölfte Befehl verwendet die **New-AzureRmLoadBalancerProbeConfig-** Funktion, um einen Prüfpunkt zu erstellen und die Prüfpunktinformationen in der Variablen mit dem Namen $Probe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-123">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="a560e-124">Der dreizehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** , um eine eingehende Netzwerkadressübersetzung (Network Address Translation, NAT) für den Lastenausgleich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a560e-124">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="a560e-125">Der vierzehnte Befehl verwendet die **New-AzureRmLoadBalancerRuleConfig-** Funktion, um eine Load Balancer-Regelkonfiguration zu erstellen und das Ergebnis in der Variablen mit dem Namen $LBRule zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-125">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="a560e-126">Der fünfzehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancer** , um ein Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $ActualLb zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-126">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="a560e-127">Der sechzehnte Befehl verwendet die **Get-AzureRmLoadBalancer-** Funktion, um Informationen über das Load Balancer abzurufen, das im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen mit dem Namen $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="a560e-127">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="a560e-128">Der Befehl "siebzehnte" verwendet das Cmdlet " **New-AzureRmVmssIPConfig** ", um eine VMSS-IP-Konfiguration zu erstellen und die Informationen in der Variablen mit dem Namen $IPCfg zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-128">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="a560e-129">Der achtzehnte Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a560e-129">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="a560e-130">Der neunzehnte Befehl verwendet das Cmdlet **New-AzureRmVmss** zum Erstellen des VMSS.</span><span class="sxs-lookup"><span data-stu-id="a560e-130">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="a560e-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="a560e-131">PARAMETERS</span></span>

### <span data-ttu-id="a560e-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="a560e-132">-AllocationMethod</span></span>
<span data-ttu-id="a560e-133">Zuordnungsmethode für die öffentliche IP-Adresse des Skalierungs Satzes (statisch oder dynamisch).</span><span class="sxs-lookup"><span data-stu-id="a560e-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="a560e-134">Wenn kein Wert angegeben wird, ist die Zuweisung statisch.</span><span class="sxs-lookup"><span data-stu-id="a560e-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a560e-135">-AsJob</span></span>
<span data-ttu-id="a560e-136">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="a560e-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a560e-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="a560e-137">-BackendPoolName</span></span>
<span data-ttu-id="a560e-138">Der Name des im Load Balancer für diesen Skalierungs Satz zu verwendenden Back-End-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="a560e-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="a560e-139">Wenn kein Wert angegeben wird, wird ein neuer Back-End-Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a560e-140">-BackendPort</span></span>
<span data-ttu-id="a560e-141">Back-End-Portnummern, die vom Scale-Satz Load Balancer für die Kommunikation mit VMS im Skalierungs Satz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a560e-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="a560e-142">Wenn keine Werte angegeben werden, werden Ports 3389 und 5985 für Windows-VMS verwendet, und Port 22 wird für Linux-VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="a560e-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-143">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a560e-143">-Credential</span></span>
<span data-ttu-id="a560e-144">Die Administratoranmeldeinformationen (Benutzername und Kennwort) für VMs in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a560e-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a560e-145">-DefaultProfile</span></span>
<span data-ttu-id="a560e-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a560e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a560e-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a560e-147">-DomainNameLabel</span></span>
<span data-ttu-id="a560e-148">Die Bezeichnung für den Domänennamen für den öffentlichen Fully-Qualified Domänennamen (Fully Domain Name, FQDN) für diesen Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="a560e-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="a560e-149">Dies ist die erste Komponente des Domänennamens, die dem Skalierungs Satz automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-149">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="a560e-150">Automatisch zugewiesene Domänennamen verwenden das Formular ( <DomainNameLabel> . <Location> . cloudapp.Azure.com).</span><span class="sxs-lookup"><span data-stu-id="a560e-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="a560e-151">Wenn kein Wert angegeben wird, ist die standardmäßige Domänennamen Beschriftung die Verkettung von <ScaleSetName> und <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="a560e-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="a560e-152">-FrontendPoolName</span></span>
<span data-ttu-id="a560e-153">Der Name des zu verwendenden Frontend-Adresspools im Scale-Satz-Lastenausgleichsmodul.</span><span class="sxs-lookup"><span data-stu-id="a560e-153">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="a560e-154">Wenn kein Wert angegeben wird, wird ein neuer Frontend-Adress Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-155">-Bildname</span><span class="sxs-lookup"><span data-stu-id="a560e-155">-ImageName</span></span>
<span data-ttu-id="a560e-156">Der Name des Bilds für VMs in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a560e-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="a560e-157">Wenn kein Wert angegeben wird, wird das Bild "Windows Server 2016 Datacenter" verwendet.</span><span class="sxs-lookup"><span data-stu-id="a560e-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a560e-158">-InstanceCount</span></span>
<span data-ttu-id="a560e-159">Die Anzahl der VM-Bilder im Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="a560e-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="a560e-160">Wenn kein Wert angegeben wird, werden 2 Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a560e-161">-LoadBalancerName</span></span>
<span data-ttu-id="a560e-162">Der Name des Load Balancer, der mit diesem Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a560e-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="a560e-163">Wenn kein Wert angegeben wird, wird ein neues Lastenausgleichsmodul mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-164">-Standort</span><span class="sxs-lookup"><span data-stu-id="a560e-164">-Location</span></span>
<span data-ttu-id="a560e-165">Die Azure-Position, an der dieser Skalierungs Satz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="a560e-166">Wenn kein Wert angegeben wird, wird der Speicherort von dem Speicherort anderer Ressourcen abgeleitet, auf die in den Parametern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="a560e-167">-NatBackendPort</span></span>
<span data-ttu-id="a560e-168">Back-End-Port für eingehende Netzwerkadressübersetzung.</span><span class="sxs-lookup"><span data-stu-id="a560e-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="a560e-169">-PublicIpAddressName</span></span>
<span data-ttu-id="a560e-170">Der Name der öffentlichen IP-Adresse, die mit diesem Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a560e-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="a560e-171">Eine neue öffentliche IPAddress mit dem gleichen Namen wie der Skalierungs Satz wird erstellt, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a560e-172">-ResourceGroupName</span></span>
<span data-ttu-id="a560e-173">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="a560e-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="a560e-174">Wenn kein Wert angegeben wird, wird eine neue ResourceGroup mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="a560e-175">-SecurityGroupName</span></span>
<span data-ttu-id="a560e-176">Der Name der Netzwerksicherheitsgruppe, die auf diesen Skalierungs Satz angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a560e-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="a560e-177">Wenn kein Wert angegeben wird, wird eine standardmäßige Netzwerksicherheitsgruppe mit dem gleichen Namen wie der Skalierungs Satz erstellt und auf den Skalierungs Satz angewendet.</span><span class="sxs-lookup"><span data-stu-id="a560e-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a560e-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="a560e-179">Das Adresspräfix des Subnets, das von diesem scaleset verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="a560e-180">Standardmäßige subneteinstellungen (192.168.1.0/24) werden angewendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a560e-181">-SubnetName</span></span>
<span data-ttu-id="a560e-182">Der Name des für diesen Skalierungs Satz zu verwendenden Subnets.</span><span class="sxs-lookup"><span data-stu-id="a560e-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="a560e-183">Ein neues Subnetz wird mit dem gleichen Namen wie der Skalierungs Satz erstellt, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a560e-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="a560e-185">Der Aktualisierungsrichtlinien Modus für VM-Instanzen in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a560e-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="a560e-186">Die Upgrade-Richtlinie kann automatische, manuelle oder parallele Upgrades angeben.</span><span class="sxs-lookup"><span data-stu-id="a560e-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a560e-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a560e-188">Gibt das **VirtualMachineScaleSet** -Objekt an, das die Eigenschaften des VMSS enthält, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a560e-189">-VirtualNetworkName</span></span>
<span data-ttu-id="a560e-190">Der Name für das virtuelle Netzwerk, der für diesen Skalierungs Satz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a560e-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="a560e-191">Wenn kein Wert angegeben wird, wird ein neues virtuelles Netzwerk mit dem gleichen Namen wie der Skalierungs Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="a560e-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a560e-192">-VMScaleSetName</span></span>
<span data-ttu-id="a560e-193">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="a560e-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a560e-194">-VmSize</span></span>
<span data-ttu-id="a560e-195">Die Größe der VM-Instanzen in dieser Skalierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a560e-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="a560e-196">Wenn keine Größe angegeben ist, wird eine Standardgröße (Standard_DS1_v2) verwendet.</span><span class="sxs-lookup"><span data-stu-id="a560e-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a560e-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="a560e-198">Das Adresspräfix für das virtuelle Netzwerk, das mit diesem Skalierungs Satz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="a560e-199">Standardeinstellungen für das virtuelle Netzwerk Adresspräfix (192.168.0.0/16) werden verwendet, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="a560e-200">-Zone</span></span>
<span data-ttu-id="a560e-201">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="a560e-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="a560e-202">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a560e-202">-Confirm</span></span>
<span data-ttu-id="a560e-203">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a560e-203">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a560e-204">-WhatIf</span></span>
<span data-ttu-id="a560e-205">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a560e-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a560e-206">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a560e-206">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a560e-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a560e-207">CommonParameters</span></span>
<span data-ttu-id="a560e-208">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a560e-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a560e-209">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a560e-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a560e-210">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a560e-210">INPUTS</span></span>

### <span data-ttu-id="a560e-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a560e-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="a560e-212">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a560e-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="a560e-213">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a560e-213">OUTPUTS</span></span>

### <span data-ttu-id="a560e-214">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a560e-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a560e-215">Notizen</span><span class="sxs-lookup"><span data-stu-id="a560e-215">NOTES</span></span>

## <span data-ttu-id="a560e-216">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a560e-216">RELATED LINKS</span></span>

[<span data-ttu-id="a560e-217">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-217">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a560e-218">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-218">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a560e-219">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-219">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a560e-220">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-220">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a560e-221">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-221">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="a560e-222">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-222">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a560e-223">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a560e-223">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


