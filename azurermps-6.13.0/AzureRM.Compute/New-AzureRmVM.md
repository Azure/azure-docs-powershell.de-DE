---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663206"
---
# <span data-ttu-id="95bb4-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-101">New-AzureRmVM</span></span>

## <span data-ttu-id="95bb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="95bb4-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="95bb4-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95bb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95bb4-104">SYNTAX</span></span>

### <span data-ttu-id="95bb4-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95bb4-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="95bb4-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="95bb4-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bb4-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="95bb4-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95bb4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95bb4-108">DESCRIPTION</span></span>
<span data-ttu-id="95bb4-109">Das Cmdlet **New-AzureRmVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="95bb4-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="95bb4-110">Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="95bb4-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="95bb4-111">Verwenden Sie das New-AzureRmVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="95bb4-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="95bb4-112">Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Satz-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="95bb4-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="95bb4-113">Das `SimpleParameterSet` bietet eine bequeme Methode zum Erstellen eines virtuellen Computers, indem häufige Argumente für die VM-Erstellung optional sind.</span><span class="sxs-lookup"><span data-stu-id="95bb4-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="95bb4-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95bb4-114">EXAMPLES</span></span>

### <span data-ttu-id="95bb4-115">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="95bb4-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="95bb4-116">Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="95bb4-117">Das Skript fragt einen Benutzernamen und ein Kennwort für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="95bb4-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="95bb4-118">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="95bb4-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="95bb4-119">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="95bb4-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="95bb4-120">In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95bb4-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="95bb4-121">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95bb4-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="95bb4-122">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="95bb4-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="95bb4-123">Mit dem Cmdlet **Get-AzureSubscription** können Sie Ihren Anmeldestatus bestätigen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="95bb4-124">Beispiel 3: Erstellen eines virtuellen Computers aus einem Marketplace-Abbild ohne öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="95bb4-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="95bb4-125">In diesem Beispiel wird ein neues Netzwerk bereitgestellt und eine Windows-VM vom Marketplace bereitgestellt, ohne dass eine öffentliche IP-Adresse oder Netzwerksicherheitsgruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="95bb4-126">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95bb4-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="95bb4-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bb4-127">PARAMETERS</span></span>

### <span data-ttu-id="95bb4-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="95bb4-128">-AddressPrefix</span></span>
<span data-ttu-id="95bb4-129">Das Adresspräfix für das virtuelle Netzwerk, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="95bb4-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="95bb4-130">-AllocationMethod</span></span>
<span data-ttu-id="95bb4-131">Die IP-Zuordnungsmethode für die öffentliche IP-Adresse, die für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="95bb4-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95bb4-132">-AsJob</span></span>
<span data-ttu-id="95bb4-133">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="95bb4-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95bb4-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="95bb4-134">-AvailabilitySetName</span></span>
<span data-ttu-id="95bb4-135">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="95bb4-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="95bb4-136">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="95bb4-136">-Credential</span></span>
<span data-ttu-id="95bb4-137">Die Administratoranmeldeinformationen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="95bb4-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="95bb4-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="95bb4-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="95bb4-139">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="95bb4-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="95bb4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bb4-140">-DefaultProfile</span></span>
<span data-ttu-id="95bb4-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95bb4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95bb4-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="95bb4-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="95bb4-143">Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="95bb4-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="95bb4-144">-Diskdatei</span><span class="sxs-lookup"><span data-stu-id="95bb4-144">-DiskFile</span></span>
<span data-ttu-id="95bb4-145">Der lokale Pfad zur virtuellen Festplatten-Datei, die in die Cloud hochgeladen werden soll, und zum Erstellen des virtuellen Computers, und er muss ". VHD" als Suffix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="95bb4-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="95bb4-146">-DomainNameLabel</span></span>
<span data-ttu-id="95bb4-147">Die Subdomain-Bezeichnung für den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des VM.</span><span class="sxs-lookup"><span data-stu-id="95bb4-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="95bb4-148">Dies nimmt die Form an `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="95bb4-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="95bb4-149">-Bild</span><span class="sxs-lookup"><span data-stu-id="95bb4-149">-Image</span></span>
<span data-ttu-id="95bb4-150">Der Name des angezeigten Bilds, auf dem die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="95bb4-151">Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Cores, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="95bb4-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="95bb4-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="95bb4-152">-LicenseType</span></span>
<span data-ttu-id="95bb4-153">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="95bb4-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="95bb4-154">Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="95bb4-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="95bb4-155">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="95bb4-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95bb4-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="95bb4-156">Windows_Client</span></span>
- <span data-ttu-id="95bb4-157">Windows_Server dieser Wert kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="95bb4-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="95bb4-158">Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="95bb4-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="95bb4-159">-Linux</span></span>
<span data-ttu-id="95bb4-160">Gibt an, ob die Datenträgerdatei für Linux VM ist, falls angegeben; oder Windows, wenn nicht standardmäßig angegeben.</span><span class="sxs-lookup"><span data-stu-id="95bb4-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="95bb4-161">-Standort</span><span class="sxs-lookup"><span data-stu-id="95bb4-161">-Location</span></span>
<span data-ttu-id="95bb4-162">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="95bb4-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="95bb4-163">-Name</span><span class="sxs-lookup"><span data-stu-id="95bb4-163">-Name</span></span>
<span data-ttu-id="95bb4-164">Der Name der VM-Ressource.</span><span class="sxs-lookup"><span data-stu-id="95bb4-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="95bb4-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="95bb4-165">-OpenPorts</span></span>
<span data-ttu-id="95bb4-166">Eine Liste der Ports, die für die erstellte VM in der Network Security Group (NSG) geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="95bb4-167">Der Standardwert hängt von der Art des ausgewählten Bilds ab (also Windows: 3389, 5985 und Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="95bb4-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="95bb4-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="95bb4-168">-PublicIpAddressName</span></span>
<span data-ttu-id="95bb4-169">Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse, die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bb4-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="95bb4-170">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="95bb4-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="95bb4-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bb4-171">-ResourceGroupName</span></span>
<span data-ttu-id="95bb4-172">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="95bb4-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="95bb4-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="95bb4-173">-SecurityGroupName</span></span>
<span data-ttu-id="95bb4-174">Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG), die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bb4-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="95bb4-175">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="95bb4-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="95bb4-176">-Size</span><span class="sxs-lookup"><span data-stu-id="95bb4-176">-Size</span></span>
<span data-ttu-id="95bb4-177">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="95bb4-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="95bb4-178">Der Standardwert lautet: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="95bb4-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="95bb4-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="95bb4-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="95bb4-180">Das Adresspräfix für das Subnetz, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="95bb4-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="95bb4-181">-SubnetName</span></span>
<span data-ttu-id="95bb4-182">Der Name eines neuen (oder vorhandenen) Subnets, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bb4-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="95bb4-183">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="95bb4-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="95bb4-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95bb4-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="95bb4-185">Wenn der Parameter vorhanden ist, wird dem virtuellen Computer eine verwaltete System Identität zugewiesen, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="95bb4-186">-Tag</span><span class="sxs-lookup"><span data-stu-id="95bb4-186">-Tag</span></span>
<span data-ttu-id="95bb4-187">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="95bb4-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="95bb4-188">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="95bb4-189">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="95bb4-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="95bb4-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="95bb4-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="95bb4-191">Der Name einer verwalteten Dienstidentität, die dem virtuellen Computer zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bb4-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="95bb4-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="95bb4-192">-VirtualNetworkName</span></span>
<span data-ttu-id="95bb4-193">Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95bb4-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="95bb4-194">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="95bb4-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="95bb4-195">-VM</span><span class="sxs-lookup"><span data-stu-id="95bb4-195">-VM</span></span>
<span data-ttu-id="95bb4-196">Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="95bb4-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="95bb4-197">Verwenden Sie das New-AzureRmVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95bb4-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="95bb4-198">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzureRmVMOperatingSystem", "AzureRmVMSourceImage" und "Add-AzureRmVMNetworkInterface".</span><span class="sxs-lookup"><span data-stu-id="95bb4-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="95bb4-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="95bb4-199">-Zone</span></span>
<span data-ttu-id="95bb4-200">Gibt die Zonenliste der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="95bb4-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="95bb4-201">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95bb4-201">-Confirm</span></span>
<span data-ttu-id="95bb4-202">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95bb4-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bb4-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bb4-203">-WhatIf</span></span>
<span data-ttu-id="95bb4-204">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95bb4-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bb4-205">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95bb4-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bb4-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bb4-206">CommonParameters</span></span>
<span data-ttu-id="95bb4-207">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bb4-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bb4-208">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bb4-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bb4-209">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95bb4-209">INPUTS</span></span>

### <span data-ttu-id="95bb4-210">System. String</span><span class="sxs-lookup"><span data-stu-id="95bb4-210">System.String</span></span>

### <span data-ttu-id="95bb4-211">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95bb4-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="95bb4-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="95bb4-212">System.String[]</span></span>

### <span data-ttu-id="95bb4-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="95bb4-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="95bb4-214">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95bb4-214">OUTPUTS</span></span>

### <span data-ttu-id="95bb4-215">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="95bb4-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="95bb4-216">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="95bb4-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="95bb4-217">Notizen</span><span class="sxs-lookup"><span data-stu-id="95bb4-217">NOTES</span></span>

## <span data-ttu-id="95bb4-218">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95bb4-218">RELATED LINKS</span></span>

[<span data-ttu-id="95bb4-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="95bb4-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="95bb4-221">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="95bb4-222">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="95bb4-223">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="95bb4-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95bb4-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="95bb4-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="95bb4-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="95bb4-226">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="95bb4-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="95bb4-227">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="95bb4-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="95bb4-228">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="95bb4-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="95bb4-229">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="95bb4-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="95bb4-230">Satz-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="95bb4-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


