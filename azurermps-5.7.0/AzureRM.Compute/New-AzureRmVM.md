---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478602"
---
# <span data-ttu-id="db2e8-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-101">New-AzureRmVM</span></span>

## <span data-ttu-id="db2e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db2e8-102">SYNOPSIS</span></span>
<span data-ttu-id="db2e8-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="db2e8-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db2e8-104">SYNTAX</span></span>

### <span data-ttu-id="db2e8-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="db2e8-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2e8-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2e8-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db2e8-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="db2e8-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2e8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db2e8-108">DESCRIPTION</span></span>
<span data-ttu-id="db2e8-109">Das Cmdlet **New-AzureRmVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="db2e8-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="db2e8-110">Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="db2e8-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="db2e8-111">Verwenden Sie das New-AzureRmVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="db2e8-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="db2e8-112">Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Satz-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="db2e8-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="db2e8-113">Das `SimpleParameterSet` bietet eine bequeme Methode zum Erstellen eines virtuellen Computers, indem häufige Argumente für die VM-Erstellung optional sind.</span><span class="sxs-lookup"><span data-stu-id="db2e8-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="db2e8-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db2e8-114">EXAMPLES</span></span>

### <span data-ttu-id="db2e8-115">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="db2e8-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="db2e8-116">Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="db2e8-117">Das Skript fragt einen Benutzernamen und ein Kennwort für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="db2e8-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="db2e8-118">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="db2e8-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="db2e8-119">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="db2e8-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="db2e8-120">In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db2e8-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="db2e8-121">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="db2e8-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="db2e8-122">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="db2e8-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="db2e8-123">Mit dem Cmdlet **Get-AzureSubscription** können Sie Ihren Anmeldestatus bestätigen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="db2e8-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="db2e8-124">PARAMETERS</span></span>

### <span data-ttu-id="db2e8-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="db2e8-125">-AddressPrefix</span></span>
<span data-ttu-id="db2e8-126">Das Adresspräfix für das virtuelle Netzwerk, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db2e8-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="db2e8-127">-AllocationMethod</span></span>
<span data-ttu-id="db2e8-128">Die IP-Zuordnungsmethode für die öffentliche IP-Adresse, die für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db2e8-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db2e8-129">-AsJob</span></span>
<span data-ttu-id="db2e8-130">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="db2e8-130">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="db2e8-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="db2e8-131">-AvailabilitySetName</span></span>
<span data-ttu-id="db2e8-132">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="db2e8-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-133">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="db2e8-133">-Credential</span></span>
<span data-ttu-id="db2e8-134">Die Administratoranmeldeinformationen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="db2e8-134">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="db2e8-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="db2e8-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="db2e8-136">Gibt die Größe von Datenträgern in GB an.</span><span class="sxs-lookup"><span data-stu-id="db2e8-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2e8-137">-DefaultProfile</span></span>
<span data-ttu-id="db2e8-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db2e8-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db2e8-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="db2e8-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="db2e8-140">Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="db2e8-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-141">-Diskdatei</span><span class="sxs-lookup"><span data-stu-id="db2e8-141">-DiskFile</span></span>
<span data-ttu-id="db2e8-142">Der lokale Pfad zur virtuellen Festplatten-Datei, die in die Cloud hochgeladen werden soll, und zum Erstellen des virtuellen Computers, und er muss ". VHD" als Suffix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="db2e8-143">-DomainNameLabel</span></span>
<span data-ttu-id="db2e8-144">Die Subdomain-Bezeichnung für den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des VM.</span><span class="sxs-lookup"><span data-stu-id="db2e8-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="db2e8-145">Dies nimmt die Form an `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="db2e8-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-146">-Bildname</span><span class="sxs-lookup"><span data-stu-id="db2e8-146">-ImageName</span></span>
<span data-ttu-id="db2e8-147">Der Name des angezeigten Bilds, auf dem die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db2e8-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="db2e8-148">Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Cores, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="db2e8-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="db2e8-149">-LicenseType</span></span>
<span data-ttu-id="db2e8-150">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="db2e8-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="db2e8-151">Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="db2e8-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="db2e8-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="db2e8-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db2e8-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="db2e8-153">Windows_Client</span></span>
- <span data-ttu-id="db2e8-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="db2e8-154">Windows_Server</span></span>

<span data-ttu-id="db2e8-155">Dieser Wert kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="db2e8-155">This value cannot be updated.</span></span>
<span data-ttu-id="db2e8-156">Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="db2e8-157">-Linux</span></span>
<span data-ttu-id="db2e8-158">Gibt an, ob die Datenträgerdatei für Linux VM ist, falls angegeben; oder Windows, wenn nicht standardmäßig angegeben.</span><span class="sxs-lookup"><span data-stu-id="db2e8-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-159">-Standort</span><span class="sxs-lookup"><span data-stu-id="db2e8-159">-Location</span></span>
<span data-ttu-id="db2e8-160">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="db2e8-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-161">-Name</span><span class="sxs-lookup"><span data-stu-id="db2e8-161">-Name</span></span>
<span data-ttu-id="db2e8-162">Der Name der VM-Ressource.</span><span class="sxs-lookup"><span data-stu-id="db2e8-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="db2e8-163">-OpenPorts</span></span>
<span data-ttu-id="db2e8-164">Eine Liste der Ports, die für die erstellte VM in der Network Security Group (NSG) geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="db2e8-165">Der Standardwert hängt von der Art des ausgewählten Bilds ab (also Windows: 3389, 5985 und Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="db2e8-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="db2e8-166">-PublicIpAddressName</span></span>
<span data-ttu-id="db2e8-167">Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse, die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db2e8-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="db2e8-168">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="db2e8-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2e8-169">-ResourceGroupName</span></span>
<span data-ttu-id="db2e8-170">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="db2e8-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="db2e8-171">-SecurityGroupName</span></span>
<span data-ttu-id="db2e8-172">Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG), die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db2e8-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="db2e8-173">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="db2e8-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-174">-Size</span><span class="sxs-lookup"><span data-stu-id="db2e8-174">-Size</span></span>
<span data-ttu-id="db2e8-175">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="db2e8-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="db2e8-176">Der Standardwert lautet: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="db2e8-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="db2e8-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="db2e8-178">Das Adresspräfix für das Subnetz, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="db2e8-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="db2e8-179">-SubnetName</span></span>
<span data-ttu-id="db2e8-180">Der Name eines neuen (oder vorhandenen) Subnets, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db2e8-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="db2e8-181">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="db2e8-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="db2e8-182">-Tag</span></span>
<span data-ttu-id="db2e8-183">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="db2e8-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="db2e8-184">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="db2e8-185">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="db2e8-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="db2e8-186">-VirtualNetworkName</span></span>
<span data-ttu-id="db2e8-187">Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="db2e8-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="db2e8-188">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="db2e8-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-189">-VM</span><span class="sxs-lookup"><span data-stu-id="db2e8-189">-VM</span></span>
<span data-ttu-id="db2e8-190">Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="db2e8-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="db2e8-191">Verwenden Sie das New-AzureRmVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="db2e8-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="db2e8-192">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzureRmVMOperatingSystem", "AzureRmVMSourceImage" und "Add-AzureRmVMNetworkInterface".</span><span class="sxs-lookup"><span data-stu-id="db2e8-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="db2e8-193">-Zone</span></span>
<span data-ttu-id="db2e8-194">Gibt die Zonenliste der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="db2e8-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2e8-195">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db2e8-195">-Confirm</span></span>
<span data-ttu-id="db2e8-196">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db2e8-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2e8-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2e8-197">-WhatIf</span></span>
<span data-ttu-id="db2e8-198">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db2e8-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="db2e8-199">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db2e8-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2e8-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2e8-200">CommonParameters</span></span>
<span data-ttu-id="db2e8-201">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2e8-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2e8-202">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2e8-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2e8-203">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db2e8-203">INPUTS</span></span>

### <span data-ttu-id="db2e8-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="db2e8-204">PSVirtualMachine</span></span>
<span data-ttu-id="db2e8-205">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="db2e8-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="db2e8-206">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db2e8-206">OUTPUTS</span></span>

### <span data-ttu-id="db2e8-207">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="db2e8-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="db2e8-208">Notizen</span><span class="sxs-lookup"><span data-stu-id="db2e8-208">NOTES</span></span>

## <span data-ttu-id="db2e8-209">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db2e8-209">RELATED LINKS</span></span>

[<span data-ttu-id="db2e8-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="db2e8-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="db2e8-212">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="db2e8-213">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="db2e8-214">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="db2e8-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="db2e8-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="db2e8-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="db2e8-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="db2e8-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db2e8-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="db2e8-218">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="db2e8-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="db2e8-219">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="db2e8-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="db2e8-220">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="db2e8-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="db2e8-221">Satz-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="db2e8-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


