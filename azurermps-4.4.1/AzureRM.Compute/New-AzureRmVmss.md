---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 54ddf9527abcb1f94a4d8c262f9c0f22e18ea1ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505158"
---
# <span data-ttu-id="47863-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="47863-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47863-102">SYNOPSIS</span></span>
<span data-ttu-id="47863-103">Erstellt eine VMSS.</span><span class="sxs-lookup"><span data-stu-id="47863-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47863-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47863-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47863-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47863-105">DESCRIPTION</span></span>
<span data-ttu-id="47863-106">Das Cmdlet **New-AzureRmVmss** erstellt einen virtuellen Computer-Skalierungs Satz (VMSS) in Azure.</span><span class="sxs-lookup"><span data-stu-id="47863-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="47863-107">Dieses Cmdlet akzeptiert ein **VirtualMachineScaleSet** -Objekt als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="47863-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="47863-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47863-108">EXAMPLES</span></span>

### <span data-ttu-id="47863-109">Beispiel 1: Erstellen einer VMSS</span><span class="sxs-lookup"><span data-stu-id="47863-109">Example 1: Create a VMSS</span></span>
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

<span data-ttu-id="47863-110">Im folgenden komplexen Beispiel wird ein VMSS erstellt.</span><span class="sxs-lookup"><span data-stu-id="47863-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="47863-111">Der erste Befehl erstellt eine Ressourcengruppe mit dem angegebenen Namen und Speicherort.</span><span class="sxs-lookup"><span data-stu-id="47863-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="47863-112">Der zweite Befehl verwendet das Cmdlet **New-AzureRmStorageAccount** , um ein Speicherkonto zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47863-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="47863-113">Der dritte Befehl verwendet dann das Cmdlet " **Get-AzureRmStorageAccount** ", um das im zweiten Befehl erstellte Speicherkonto abzurufen, und speichert das Ergebnis in der $STOAccount Variablen.</span><span class="sxs-lookup"><span data-stu-id="47863-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="47863-114">Der fünfte Befehl verwendet das Cmdlet **New-AzureRmVirtualNetworkSubnetConfig** , um ein Subnetz zu erstellen und das Ergebnis in der Variablen mit dem Namen $Subnet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="47863-115">Der sechste Befehl verwendet das Cmdlet **New-AzureRmVirtualNetwork** , um ein virtuelles Netzwerk zu erstellen und das Ergebnis in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="47863-116">Der siebte Befehl verwendet die **Get-AzureRmVirtualNetwork-** Funktion, um Informationen zu dem im sechsten Befehl erstellten virtuellen Netzwerk abzurufen und die Informationen in der Variablen mit dem Namen $VNet zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="47863-117">Der achte und neunte Befehl verwendet die **New-AzureRmPublicIpAddress** und **Get-AzureRmPublicIpAddress** , um Informationen aus dieser öffentlichen IP-Adresse zu erstellen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="47863-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="47863-118">Die Befehle speichern die Informationen in der Variablen mit dem Namen $PubIP.</span><span class="sxs-lookup"><span data-stu-id="47863-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="47863-119">Der zehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** , um ein Frontend-Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $Frontend zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="47863-120">Der elfte Befehl verwendet das **New-AzureRmLoadBalancerBackendAddressPoolConfig-Steuer** System, um eine Konfiguration des Back-End-Adresspools zu erstellen und das Ergebnis in der Variablen mit dem Namen $BackendAddressPool zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="47863-121">Der zwölfte Befehl verwendet die **New-AzureRmLoadBalancerProbeConfig-** Funktion, um einen Prüfpunkt zu erstellen und die Prüfpunktinformationen in der Variablen mit dem Namen $Probe zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="47863-122">Der dreizehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerInboundNatPoolConfig** , um eine eingehende Netzwerkadressübersetzung (Network Address Translation, NAT) für den Lastenausgleich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47863-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="47863-123">Der vierzehnte Befehl verwendet die **New-AzureRmLoadBalancerRuleConfig-** Funktion, um eine Load Balancer-Regelkonfiguration zu erstellen und das Ergebnis in der Variablen mit dem Namen $LBRule zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="47863-124">Der fünfzehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancer** , um ein Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $ActualLb zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="47863-125">Der sechzehnte Befehl verwendet die **Get-AzureRmLoadBalancer-** Funktion, um Informationen über das Load Balancer abzurufen, das im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen mit dem Namen $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="47863-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="47863-126">Der Befehl "siebzehnte" verwendet das Cmdlet " **New-AzureRmVmssIPConfig** ", um eine VMSS-IP-Konfiguration zu erstellen und die Informationen in der Variablen mit dem Namen $IPCfg zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="47863-127">Der achtzehnte Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47863-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="47863-128">Der neunzehnte Befehl verwendet das Cmdlet **New-AzureRmVmss** zum Erstellen des VMSS.</span><span class="sxs-lookup"><span data-stu-id="47863-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="47863-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="47863-129">PARAMETERS</span></span>

### <span data-ttu-id="47863-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47863-130">-DefaultProfile</span></span>
<span data-ttu-id="47863-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47863-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47863-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47863-132">-ResourceGroupName</span></span>
<span data-ttu-id="47863-133">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="47863-133">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47863-134">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="47863-134">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="47863-135">Gibt das **VirtualMachineScaleSet** -Objekt an, das die Eigenschaften des VMSS enthält, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="47863-135">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47863-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="47863-136">-VMScaleSetName</span></span>
<span data-ttu-id="47863-137">Gibt den Namen des von diesem Cmdlet erstellten VMSS an.</span><span class="sxs-lookup"><span data-stu-id="47863-137">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47863-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47863-138">-Confirm</span></span>
<span data-ttu-id="47863-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47863-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47863-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47863-140">-WhatIf</span></span>
<span data-ttu-id="47863-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47863-141">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="47863-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47863-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47863-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47863-143">CommonParameters</span></span>
<span data-ttu-id="47863-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47863-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47863-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47863-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47863-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47863-146">INPUTS</span></span>

## <span data-ttu-id="47863-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47863-147">OUTPUTS</span></span>

### <span data-ttu-id="47863-148">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="47863-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="47863-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="47863-149">NOTES</span></span>

## <span data-ttu-id="47863-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47863-150">RELATED LINKS</span></span>

[<span data-ttu-id="47863-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="47863-152">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="47863-153">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="47863-154">Satz-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="47863-155">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="47863-156">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="47863-157">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="47863-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


