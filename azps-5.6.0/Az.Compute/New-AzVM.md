---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: a7fbf991357e63dbe2436350892f9e601eb586db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920832"
---
# <span data-ttu-id="4a624-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-101">New-AzVM</span></span>

## <span data-ttu-id="4a624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a624-102">SYNOPSIS</span></span>
<span data-ttu-id="4a624-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4a624-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="4a624-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a624-104">SYNTAX</span></span>

### <span data-ttu-id="4a624-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a624-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a624-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a624-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a624-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a624-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a624-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a624-108">DESCRIPTION</span></span>
<span data-ttu-id="4a624-109">Das **Cmdlet New-AzVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="4a624-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="4a624-110">Dieses Cmdlet übernimmt ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="4a624-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="4a624-111">Verwenden Sie New-AzVMConfig-Cmdlet, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a624-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="4a624-112">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, z. B. Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface und Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="4a624-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="4a624-113">Bietet `SimpleParameterSet` eine praktische Methode zum Erstellen einer VM, indem allgemeine Argumente für die Vm-Erstellung optional werden.</span><span class="sxs-lookup"><span data-stu-id="4a624-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="4a624-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a624-114">EXAMPLES</span></span>

### <span data-ttu-id="4a624-115">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="4a624-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="4a624-116">Dieses Beispielskript zeigt, wie sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a624-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="4a624-117">Das Skript fragt einen Benutzernamen und ein Kennwort für die VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="4a624-118">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4a624-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="4a624-119">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="4a624-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="4a624-120">In diesem Beispiel wird ein vorhandenes systemspezifisches, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet, an das ein Datenträger anfügen, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="4a624-121">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers inline verwendet, anstatt **Get-Credential** aufrief, was eine Benutzerinteraktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="4a624-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="4a624-122">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="4a624-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="4a624-123">Sie können Ihren Anmeldestatus mithilfe des **Get-AzSubscription-Cmdlets** bestätigen.</span><span class="sxs-lookup"><span data-stu-id="4a624-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="4a624-124">Beispiel 3: Erstellen einer VM aus einem Marketplace-Bild ohne öffentliche IP</span><span class="sxs-lookup"><span data-stu-id="4a624-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="4a624-125">In diesem Beispiel wird ein neues Netzwerk bereitgestellt und eine Windows-VM aus dem Marketplace bereitgestellt, ohne eine öffentliche IP-Adresse oder Netzwerksicherheitsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a624-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="4a624-126">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers inline verwendet, anstatt **Get-Credential** aufrief, was eine Benutzerinteraktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="4a624-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="4a624-127">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a624-127">PARAMETERS</span></span>

### <span data-ttu-id="4a624-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4a624-128">-AddressPrefix</span></span>
<span data-ttu-id="4a624-129">Das Adresspräfix für das virtuelle Netzwerk, das für die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="4a624-130">-AllocationMethod</span></span>
<span data-ttu-id="4a624-131">Die IP-Zuweisungsmethode für die öffentliche IP, die für die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a624-132">-AsJob</span></span>
<span data-ttu-id="4a624-133">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4a624-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4a624-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="4a624-134">-AvailabilitySetName</span></span>
<span data-ttu-id="4a624-135">Gibt einen Namen für den Verfügbarkeitssatz an.</span><span class="sxs-lookup"><span data-stu-id="4a624-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-136">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4a624-136">-Credential</span></span>
<span data-ttu-id="4a624-137">Die Administratoranmeldeinformationen für die VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="4a624-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="4a624-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="4a624-139">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="4a624-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a624-140">-DefaultProfile</span></span>
<span data-ttu-id="4a624-141">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a624-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a624-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="4a624-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="4a624-143">Gibt an, dass dieses Cmdlet die **BG Info-Erweiterung** nicht auf dem virtuellen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="4a624-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="4a624-144">-DiskFile</span></span>
<span data-ttu-id="4a624-145">Der lokale Pfad zur virtuellen Festplattendatei, die in die Cloud hochgeladen werden soll, und zum Erstellen der VM, und er muss ".vhd" als Suffix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4a624-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="4a624-146">-DomainNameLabel</span></span>
<span data-ttu-id="4a624-147">Die Unterdomänenbeschriftung für den vollqualifizierten Domänennamen (Fully-Qualified Domain Name, FQDN) der VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="4a624-148">Dies nimmt das Formular `{domainNameLabel}.{location}.cloudapp.azure.com` auf.</span><span class="sxs-lookup"><span data-stu-id="4a624-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="4a624-149">-EnableUltraSSD</span></span>
<span data-ttu-id="4a624-150">Verwenden Sie UltraSSD-Datenträger für die vm.</span><span class="sxs-lookup"><span data-stu-id="4a624-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="4a624-151">-EvictionPolicy</span></span>
<span data-ttu-id="4a624-152">Die Räumungsrichtlinie für den virtuellen Azure Spot-Computer.</span><span class="sxs-lookup"><span data-stu-id="4a624-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="4a624-153">Unterstützte Werte sind "Deallocate" und "Delete".</span><span class="sxs-lookup"><span data-stu-id="4a624-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="4a624-154">-HostGroupId</span></span>
<span data-ttu-id="4a624-155">Gibt die dedizierte Hostgruppe an, in der sich der virtuelle Computer befindet.</span><span class="sxs-lookup"><span data-stu-id="4a624-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="4a624-156">-HostId</span></span>
<span data-ttu-id="4a624-157">Die Id des Hosts</span><span class="sxs-lookup"><span data-stu-id="4a624-157">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-158">-Image</span><span class="sxs-lookup"><span data-stu-id="4a624-158">-Image</span></span>
<span data-ttu-id="4a624-159">Der Name des anzeigefreundlichen Bilds, auf dem die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="4a624-160">Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="4a624-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4a624-161">-LicenseType</span></span>
<span data-ttu-id="4a624-162">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal lizenziert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a624-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="4a624-163">Mögliche Werte für Windows Server sind:</span><span class="sxs-lookup"><span data-stu-id="4a624-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="4a624-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="4a624-164">Windows_Client</span></span>
- <span data-ttu-id="4a624-165">Windows_Server Mögliche Werte für Das Betriebssystem Linux Server sind:</span><span class="sxs-lookup"><span data-stu-id="4a624-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="4a624-166">RHEL_BYOS (für RREL)</span><span class="sxs-lookup"><span data-stu-id="4a624-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="4a624-167">SLES_BYOS (für SUSE)</span><span class="sxs-lookup"><span data-stu-id="4a624-167">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="4a624-168">-Linux</span></span>
<span data-ttu-id="4a624-169">Gibt an, ob die Datenträgerdatei für die Linux-VM verwendet wird( sofern angegeben). oder Windows, sofern nicht standardmäßig angegeben.</span><span class="sxs-lookup"><span data-stu-id="4a624-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-170">-Location</span><span class="sxs-lookup"><span data-stu-id="4a624-170">-Location</span></span>
<span data-ttu-id="4a624-171">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="4a624-171">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-172">-MaxPreis</span><span class="sxs-lookup"><span data-stu-id="4a624-172">-MaxPrice</span></span>
<span data-ttu-id="4a624-173">Der max. Preis für die Abrechnung eines virtuellen Computers mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="4a624-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="4a624-174">-EncryptionAtHost</span></span>
<span data-ttu-id="4a624-175">Die EncryptionAtHost-Eigenschaft kann vom Benutzer in der Anforderung verwendet werden, um die Hostverschlüsselung für den Skalierungssatz des virtuellen Computers oder virtuellen Computers zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4a624-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="4a624-176">Dadurch wird die Verschlüsselung für alle Datenträger aktiviert, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst.</span><span class="sxs-lookup"><span data-stu-id="4a624-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="4a624-177">Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a624-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="4a624-178">-Name</span><span class="sxs-lookup"><span data-stu-id="4a624-178">-Name</span></span>
<span data-ttu-id="4a624-179">Der Name der VM-Ressource.</span><span class="sxs-lookup"><span data-stu-id="4a624-179">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="4a624-180">-OpenPorts</span></span>
<span data-ttu-id="4a624-181">Eine Liste der Ports, die in der Netzwerksicherheitsgruppe (Network Security Group, NSG) für die erstellte VM geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4a624-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="4a624-182">Der Standardwert hängt vom typ des ausgewählten Bilds ab (d. h. Windows: 3389, 5985 und Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="4a624-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-183">-Priorität</span><span class="sxs-lookup"><span data-stu-id="4a624-183">-Priority</span></span>
<span data-ttu-id="4a624-184">Die Priorität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4a624-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="4a624-185">Nur unterstützte Werte sind "Normal", "Spot" und "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="4a624-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="4a624-186">"Regular" ist für einen normalen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4a624-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="4a624-187">"Spot" ist für virtuelle Spotcomputer.</span><span class="sxs-lookup"><span data-stu-id="4a624-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="4a624-188">"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="4a624-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="4a624-189">Verwenden Sie "Spot" statt "Niedrig".</span><span class="sxs-lookup"><span data-stu-id="4a624-189">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4a624-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="4a624-191">Die Ressourcen-ID der Näherungsgruppe, die für diesen virtuellen Computer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a624-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="4a624-192">-PublicIpAddressName</span></span>
<span data-ttu-id="4a624-193">Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse für die erstellte VM, die verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a624-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="4a624-194">Wenn nicht angegeben, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="4a624-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a624-195">-ResourceGroupName</span></span>
<span data-ttu-id="4a624-196">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4a624-196">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="4a624-197">-SecurityGroupName</span></span>
<span data-ttu-id="4a624-198">Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG) für die erstellte VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="4a624-199">Wenn nicht angegeben, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="4a624-199">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-200">-Size</span><span class="sxs-lookup"><span data-stu-id="4a624-200">-Size</span></span>
<span data-ttu-id="4a624-201">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="4a624-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="4a624-202">Der Standardwert ist: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="4a624-202">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4a624-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="4a624-204">Das Adresspräfix für das Subnetz, das für die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-204">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-205">-Subnetzname</span><span class="sxs-lookup"><span data-stu-id="4a624-205">-SubnetName</span></span>
<span data-ttu-id="4a624-206">Der Name eines neuen (oder vorhandenen) Subnetzes für die erstellte VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="4a624-207">Wenn nicht angegeben, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="4a624-207">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4a624-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="4a624-209">Wenn der Parameter vorhanden ist, wird der VM eine verwaltete Systemidentität zugewiesen, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-210">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a624-210">-Tag</span></span>
<span data-ttu-id="4a624-211">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Namen-Wert-Paaren markiert werden können.</span><span class="sxs-lookup"><span data-stu-id="4a624-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="4a624-212">Durch das Hinzufügen von Tags zu Ressourcen können Sie Ressourcen über Ressourcengruppen hinweg gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a624-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="4a624-213">Jede Ressource oder Ressourcengruppe kann maximal 15 Tags haben.</span><span class="sxs-lookup"><span data-stu-id="4a624-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4a624-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="4a624-215">Der Name einer verwalteten Dienstidentität, die der VM zugewiesen werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4a624-215">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4a624-216">-VirtualNetworkName</span></span>
<span data-ttu-id="4a624-217">Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks für die erstellte VM.</span><span class="sxs-lookup"><span data-stu-id="4a624-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="4a624-218">Wenn nicht angegeben, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="4a624-218">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-219">-VM</span><span class="sxs-lookup"><span data-stu-id="4a624-219">-VM</span></span>
<span data-ttu-id="4a624-220">Gibt einen lokalen virtuellen Computer an, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a624-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="4a624-221">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das New-AzVMConfig Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a624-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="4a624-222">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, z. B. Set-AzVMOperatingSystem, Set-AzVMSourceImage und Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="4a624-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="4a624-223">-VmssId</span></span>
<span data-ttu-id="4a624-224">Die ID des Skalierungssets für virtuelle Computer, dem diese VM zugeordnet wird</span><span class="sxs-lookup"><span data-stu-id="4a624-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="4a624-225">-Zone</span></span>
<span data-ttu-id="4a624-226">Gibt die Zonenliste des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4a624-226">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a624-227">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a624-227">-Confirm</span></span>
<span data-ttu-id="4a624-228">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a624-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a624-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a624-229">-WhatIf</span></span>
<span data-ttu-id="4a624-230">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a624-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a624-231">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a624-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a624-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a624-232">CommonParameters</span></span>
<span data-ttu-id="4a624-233">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a624-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a624-234">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a624-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a624-235">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a624-235">INPUTS</span></span>

### <span data-ttu-id="4a624-236">System.String</span><span class="sxs-lookup"><span data-stu-id="4a624-236">System.String</span></span>

### <span data-ttu-id="4a624-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a624-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4a624-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4a624-238">System.String[]</span></span>

### <span data-ttu-id="4a624-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a624-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a624-240">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a624-240">OUTPUTS</span></span>

### <span data-ttu-id="4a624-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4a624-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="4a624-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a624-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4a624-243">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a624-243">NOTES</span></span>

## <span data-ttu-id="4a624-244">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a624-244">RELATED LINKS</span></span>

[<span data-ttu-id="4a624-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4a624-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="4a624-247">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="4a624-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="4a624-249">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="4a624-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4a624-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="4a624-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4a624-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="4a624-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4a624-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="4a624-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4a624-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="4a624-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4a624-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="4a624-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="4a624-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="4a624-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="4a624-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


