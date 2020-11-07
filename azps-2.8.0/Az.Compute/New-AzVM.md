---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 4350a1bca25d94f2d3fab27c202eda4392180027
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652062"
---
# <span data-ttu-id="68ecb-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-101">New-AzVM</span></span>

## <span data-ttu-id="68ecb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="68ecb-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="68ecb-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="68ecb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ecb-104">SYNTAX</span></span>

### <span data-ttu-id="68ecb-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68ecb-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ecb-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ecb-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68ecb-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ecb-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ecb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="68ecb-109">Das Cmdlet **New-AzVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="68ecb-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="68ecb-110">Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="68ecb-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="68ecb-111">Verwenden Sie das New-AzVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="68ecb-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="68ecb-112">Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Satz-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="68ecb-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="68ecb-113">Das `SimpleParameterSet` bietet eine bequeme Methode zum Erstellen eines virtuellen Computers, indem häufige Argumente für die VM-Erstellung optional sind.</span><span class="sxs-lookup"><span data-stu-id="68ecb-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="68ecb-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68ecb-114">EXAMPLES</span></span>

### <span data-ttu-id="68ecb-115">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="68ecb-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="68ecb-116">Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="68ecb-117">Das Skript fragt einen Benutzernamen und ein Kennwort für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="68ecb-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="68ecb-118">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="68ecb-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="68ecb-119">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="68ecb-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="68ecb-120">In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68ecb-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="68ecb-121">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="68ecb-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="68ecb-122">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="68ecb-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="68ecb-123">Mit dem Cmdlet **Get-AzSubscription** können Sie Ihren Anmeldestatus bestätigen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="68ecb-124">Beispiel 3: Erstellen eines virtuellen Computers aus einem Marketplace-Abbild ohne öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="68ecb-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="68ecb-125">In diesem Beispiel wird ein neues Netzwerk bereitgestellt und eine Windows-VM vom Marketplace bereitgestellt, ohne dass eine öffentliche IP-Adresse oder Netzwerksicherheitsgruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="68ecb-126">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="68ecb-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="68ecb-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ecb-127">PARAMETERS</span></span>

### <span data-ttu-id="68ecb-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="68ecb-128">-AddressPrefix</span></span>
<span data-ttu-id="68ecb-129">Das Adresspräfix für das virtuelle Netzwerk, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="68ecb-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="68ecb-130">-AllocationMethod</span></span>
<span data-ttu-id="68ecb-131">Die IP-Zuordnungsmethode für die öffentliche IP-Adresse, die für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="68ecb-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68ecb-132">-AsJob</span></span>
<span data-ttu-id="68ecb-133">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="68ecb-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="68ecb-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="68ecb-134">-AvailabilitySetName</span></span>
<span data-ttu-id="68ecb-135">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="68ecb-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="68ecb-136">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="68ecb-136">-Credential</span></span>
<span data-ttu-id="68ecb-137">Die Administratoranmeldeinformationen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="68ecb-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="68ecb-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="68ecb-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="68ecb-139">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="68ecb-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="68ecb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ecb-140">-DefaultProfile</span></span>
<span data-ttu-id="68ecb-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68ecb-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68ecb-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="68ecb-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="68ecb-143">Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="68ecb-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="68ecb-144">-Diskdatei</span><span class="sxs-lookup"><span data-stu-id="68ecb-144">-DiskFile</span></span>
<span data-ttu-id="68ecb-145">Der lokale Pfad zur virtuellen Festplatten-Datei, die in die Cloud hochgeladen werden soll, und zum Erstellen des virtuellen Computers, und er muss ". VHD" als Suffix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="68ecb-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="68ecb-146">-DomainNameLabel</span></span>
<span data-ttu-id="68ecb-147">Die Subdomain-Bezeichnung für den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des VM.</span><span class="sxs-lookup"><span data-stu-id="68ecb-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="68ecb-148">Dies nimmt die Form an `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="68ecb-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="68ecb-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="68ecb-149">-EnableUltraSSD</span></span>
<span data-ttu-id="68ecb-150">Verwenden Sie UltraSSD-Datenträger für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="68ecb-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="68ecb-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="68ecb-151">-EvictionPolicy</span></span>
<span data-ttu-id="68ecb-152">Die Räumungs Richtlinie für den virtuellen Computer mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="68ecb-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="68ecb-153">Nur unterstützter Wert ist "freigeben".</span><span class="sxs-lookup"><span data-stu-id="68ecb-153">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="68ecb-154">-Host-Nr</span><span class="sxs-lookup"><span data-stu-id="68ecb-154">-HostId</span></span>
<span data-ttu-id="68ecb-155">Die ID des Hosts</span><span class="sxs-lookup"><span data-stu-id="68ecb-155">The Id of Host</span></span>

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

### <span data-ttu-id="68ecb-156">-Bild</span><span class="sxs-lookup"><span data-stu-id="68ecb-156">-Image</span></span>
<span data-ttu-id="68ecb-157">Der Name des angezeigten Bilds, auf dem die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="68ecb-158">Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Cores, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="68ecb-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="68ecb-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="68ecb-159">-LicenseType</span></span>
<span data-ttu-id="68ecb-160">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="68ecb-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="68ecb-161">Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="68ecb-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="68ecb-162">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="68ecb-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68ecb-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="68ecb-163">Windows_Client</span></span>
- <span data-ttu-id="68ecb-164">Windows_Server dieser Wert kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="68ecb-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="68ecb-165">Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="68ecb-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="68ecb-166">-Linux</span></span>
<span data-ttu-id="68ecb-167">Gibt an, ob die Datenträgerdatei für Linux VM ist, falls angegeben; oder Windows, wenn nicht standardmäßig angegeben.</span><span class="sxs-lookup"><span data-stu-id="68ecb-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="68ecb-168">-Standort</span><span class="sxs-lookup"><span data-stu-id="68ecb-168">-Location</span></span>
<span data-ttu-id="68ecb-169">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="68ecb-169">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="68ecb-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="68ecb-170">-MaxPrice</span></span>
<span data-ttu-id="68ecb-171">Der Höchstbetrag für die Abrechnung einer virtuellen Maschine mit niedriger Priorität.</span><span class="sxs-lookup"><span data-stu-id="68ecb-171">The max price of the billing of a low priority virtual machine.</span></span>

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

### <span data-ttu-id="68ecb-172">-Name</span><span class="sxs-lookup"><span data-stu-id="68ecb-172">-Name</span></span>
<span data-ttu-id="68ecb-173">Der Name der VM-Ressource.</span><span class="sxs-lookup"><span data-stu-id="68ecb-173">The name of the VM resource.</span></span>

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

### <span data-ttu-id="68ecb-174">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="68ecb-174">-OpenPorts</span></span>
<span data-ttu-id="68ecb-175">Eine Liste der Ports, die für die erstellte VM in der Network Security Group (NSG) geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="68ecb-176">Der Standardwert hängt von der Art des ausgewählten Bilds ab (also Windows: 3389, 5985 und Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="68ecb-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="68ecb-177">-Priorität</span><span class="sxs-lookup"><span data-stu-id="68ecb-177">-Priority</span></span>
<span data-ttu-id="68ecb-178">Die Priorität für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="68ecb-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="68ecb-179">Nur Unterstützte Werte sind "Regular" und "Low".</span><span class="sxs-lookup"><span data-stu-id="68ecb-179">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="68ecb-180">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="68ecb-180">-ProximityPlacementGroup</span></span>
<span data-ttu-id="68ecb-181">Der Name oder die Ressourcen-ID der für diesen virtuellen Computer zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="68ecb-181">The name or resource id of the Proximity Placement Group to use with this VM.</span></span>

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

### <span data-ttu-id="68ecb-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="68ecb-182">-PublicIpAddressName</span></span>
<span data-ttu-id="68ecb-183">Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse, die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ecb-183">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="68ecb-184">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="68ecb-184">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="68ecb-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ecb-185">-ResourceGroupName</span></span>
<span data-ttu-id="68ecb-186">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="68ecb-186">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="68ecb-187">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="68ecb-187">-SecurityGroupName</span></span>
<span data-ttu-id="68ecb-188">Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG), die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ecb-188">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="68ecb-189">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="68ecb-189">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="68ecb-190">-Size</span><span class="sxs-lookup"><span data-stu-id="68ecb-190">-Size</span></span>
<span data-ttu-id="68ecb-191">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="68ecb-191">The Virtual Machine Size.</span></span>  <span data-ttu-id="68ecb-192">Der Standardwert lautet: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="68ecb-192">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="68ecb-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="68ecb-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="68ecb-194">Das Adresspräfix für das Subnetz, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-194">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="68ecb-195">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="68ecb-195">-SubnetName</span></span>
<span data-ttu-id="68ecb-196">Der Name eines neuen (oder vorhandenen) Subnets, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ecb-196">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="68ecb-197">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="68ecb-197">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="68ecb-198">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="68ecb-198">-SystemAssignedIdentity</span></span>
<span data-ttu-id="68ecb-199">Wenn der Parameter vorhanden ist, wird dem virtuellen Computer eine verwaltete System Identität zugewiesen, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-199">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="68ecb-200">-Tag</span><span class="sxs-lookup"><span data-stu-id="68ecb-200">-Tag</span></span>
<span data-ttu-id="68ecb-201">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="68ecb-201">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="68ecb-202">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-202">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="68ecb-203">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="68ecb-203">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="68ecb-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="68ecb-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="68ecb-205">Der Name einer verwalteten Dienstidentität, die dem virtuellen Computer zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ecb-205">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="68ecb-206">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="68ecb-206">-VirtualNetworkName</span></span>
<span data-ttu-id="68ecb-207">Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68ecb-207">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="68ecb-208">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="68ecb-208">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="68ecb-209">-VM</span><span class="sxs-lookup"><span data-stu-id="68ecb-209">-VM</span></span>
<span data-ttu-id="68ecb-210">Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="68ecb-210">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="68ecb-211">Verwenden Sie das New-AzVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68ecb-211">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="68ecb-212">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzVMOperatingSystem", "AzVMSourceImage" und "Add-AzVMNetworkInterface".</span><span class="sxs-lookup"><span data-stu-id="68ecb-212">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="68ecb-213">-Zone</span><span class="sxs-lookup"><span data-stu-id="68ecb-213">-Zone</span></span>
<span data-ttu-id="68ecb-214">Gibt die Zonenliste der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="68ecb-214">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="68ecb-215">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68ecb-215">-Confirm</span></span>
<span data-ttu-id="68ecb-216">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68ecb-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ecb-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ecb-217">-WhatIf</span></span>
<span data-ttu-id="68ecb-218">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68ecb-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ecb-219">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68ecb-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ecb-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ecb-220">CommonParameters</span></span>
<span data-ttu-id="68ecb-221">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68ecb-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ecb-222">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68ecb-222">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ecb-223">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68ecb-223">INPUTS</span></span>

### <span data-ttu-id="68ecb-224">System. String</span><span class="sxs-lookup"><span data-stu-id="68ecb-224">System.String</span></span>

### <span data-ttu-id="68ecb-225">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="68ecb-225">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="68ecb-226">System. String []</span><span class="sxs-lookup"><span data-stu-id="68ecb-226">System.String[]</span></span>

### <span data-ttu-id="68ecb-227">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="68ecb-227">System.Collections.Hashtable</span></span>

## <span data-ttu-id="68ecb-228">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68ecb-228">OUTPUTS</span></span>

### <span data-ttu-id="68ecb-229">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="68ecb-229">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="68ecb-230">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="68ecb-230">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="68ecb-231">Notizen</span><span class="sxs-lookup"><span data-stu-id="68ecb-231">NOTES</span></span>

## <span data-ttu-id="68ecb-232">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68ecb-232">RELATED LINKS</span></span>

[<span data-ttu-id="68ecb-233">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-233">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="68ecb-234">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-234">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="68ecb-235">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-235">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="68ecb-236">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-236">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="68ecb-237">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-237">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="68ecb-238">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="68ecb-238">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="68ecb-239">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="68ecb-239">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="68ecb-240">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="68ecb-240">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="68ecb-241">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="68ecb-241">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="68ecb-242">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="68ecb-242">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="68ecb-243">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="68ecb-243">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="68ecb-244">Satz-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="68ecb-244">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


