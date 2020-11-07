---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844472"
---
# <span data-ttu-id="d2ae9-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-101">New-AzVM</span></span>

## <span data-ttu-id="d2ae9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ae9-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="d2ae9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ae9-104">SYNTAX</span></span>

### <span data-ttu-id="d2ae9-105">SimpleParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2ae9-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ae9-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2ae9-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ae9-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2ae9-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ae9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2ae9-108">DESCRIPTION</span></span>
<span data-ttu-id="d2ae9-109">Das Cmdlet **New-AzVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="d2ae9-110">Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="d2ae9-111">Verwenden Sie das New-AzVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="d2ae9-112">Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzVMOperatingSystem", "AzVMSourceImage", "Add-AzVMNetworkInterface" und "Satz-AzVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="d2ae9-113">Das `SimpleParameterSet` bietet eine bequeme Methode zum Erstellen eines virtuellen Computers, indem häufige Argumente für die VM-Erstellung optional sind.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="d2ae9-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2ae9-114">EXAMPLES</span></span>

### <span data-ttu-id="d2ae9-115">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d2ae9-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="d2ae9-116">Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="d2ae9-117">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="d2ae9-118">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="d2ae9-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="d2ae9-119">In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="d2ae9-120">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="d2ae9-121">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="d2ae9-122">Mit dem Cmdlet **Get-AzureSubscription** können Sie Ihren Anmeldestatus bestätigen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="d2ae9-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2ae9-123">PARAMETERS</span></span>

### <span data-ttu-id="d2ae9-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d2ae9-124">-AddressPrefix</span></span>
<span data-ttu-id="d2ae9-125">Das Adresspräfix für das virtuelle Netzwerk, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="d2ae9-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="d2ae9-126">-AllocationMethod</span></span>
<span data-ttu-id="d2ae9-127">Die IP-Zuordnungsmethode für die öffentliche IP-Adresse, die für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="d2ae9-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2ae9-128">-AsJob</span></span>
<span data-ttu-id="d2ae9-129">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d2ae9-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-130">-AvailabilitySetName</span></span>
<span data-ttu-id="d2ae9-131">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="d2ae9-132">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d2ae9-132">-Credential</span></span>
<span data-ttu-id="d2ae9-133">Die Administratoranmeldeinformationen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="d2ae9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ae9-134">-DefaultProfile</span></span>
<span data-ttu-id="d2ae9-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2ae9-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d2ae9-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="d2ae9-137">Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="d2ae9-138">-Diskdatei</span><span class="sxs-lookup"><span data-stu-id="d2ae9-138">-DiskFile</span></span>
<span data-ttu-id="d2ae9-139">Der lokale Pfad zur virtuellen Festplatten-Datei, die in die Cloud hochgeladen werden soll, und zum Erstellen des virtuellen Computers, und er muss ". VHD" als Suffix aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="d2ae9-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d2ae9-140">-DomainNameLabel</span></span>
<span data-ttu-id="d2ae9-141">Die Subdomain-Bezeichnung für den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des VM.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="d2ae9-142">Dies nimmt die Form an `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="d2ae9-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="d2ae9-143">-Bildname</span><span class="sxs-lookup"><span data-stu-id="d2ae9-143">-ImageName</span></span>
<span data-ttu-id="d2ae9-144">Der Name des angezeigten Bilds, auf dem die VM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="d2ae9-145">Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Cores, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="d2ae9-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d2ae9-146">-LicenseType</span></span>
<span data-ttu-id="d2ae9-147">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="d2ae9-148">Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="d2ae9-149">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2ae9-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2ae9-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="d2ae9-150">Windows_Client</span></span> 
- <span data-ttu-id="d2ae9-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="d2ae9-151">Windows_Server</span></span>

<span data-ttu-id="d2ae9-152">Dieser Wert kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-152">This value cannot be updated.</span></span>
<span data-ttu-id="d2ae9-153">Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="d2ae9-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="d2ae9-154">-Linux</span></span>
<span data-ttu-id="d2ae9-155">Gibt an, ob die Datenträgerdatei für Linux VM ist, falls angegeben; oder Windows, wenn nicht standardmäßig angegeben.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="d2ae9-156">-Standort</span><span class="sxs-lookup"><span data-stu-id="d2ae9-156">-Location</span></span>
<span data-ttu-id="d2ae9-157">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="d2ae9-158">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ae9-158">-Name</span></span>
<span data-ttu-id="d2ae9-159">Der Name der VM-Ressource.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="d2ae9-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="d2ae9-160">-OpenPorts</span></span>
<span data-ttu-id="d2ae9-161">Eine Liste der Ports, die für die erstellte VM in der Network Security Group (NSG) geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="d2ae9-162">Der Standardwert hängt von der Art des ausgewählten Bilds ab (also Windows: 3389, 5985 und Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="d2ae9-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="d2ae9-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-163">-PublicIpAddressName</span></span>
<span data-ttu-id="d2ae9-164">Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse, die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="d2ae9-165">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d2ae9-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-166">-ResourceGroupName</span></span>
<span data-ttu-id="d2ae9-167">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d2ae9-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-168">-SecurityGroupName</span></span>
<span data-ttu-id="d2ae9-169">Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG), die von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="d2ae9-170">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d2ae9-171">-Size</span><span class="sxs-lookup"><span data-stu-id="d2ae9-171">-Size</span></span>
<span data-ttu-id="d2ae9-172">Die Größe des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="d2ae9-173">Der Standardwert lautet: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="d2ae9-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d2ae9-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="d2ae9-175">Das Adresspräfix für das Subnetz, das für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="d2ae9-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-176">-SubnetName</span></span>
<span data-ttu-id="d2ae9-177">Der Name eines neuen (oder vorhandenen) Subnets, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="d2ae9-178">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d2ae9-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2ae9-179">-Tag</span></span>
<span data-ttu-id="d2ae9-180">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="d2ae9-181">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="d2ae9-182">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="d2ae9-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d2ae9-183">-VirtualNetworkName</span></span>
<span data-ttu-id="d2ae9-184">Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks, das von der erstellten VM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="d2ae9-185">Wenn keine Angabe erfolgt, wird ein Name generiert.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="d2ae9-186">-VM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-186">-VM</span></span>
<span data-ttu-id="d2ae9-187">Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="d2ae9-188">Verwenden Sie das New-AzVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="d2ae9-189">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzVMOperatingSystem", "AzVMSourceImage" und "Add-AzVMNetworkInterface".</span><span class="sxs-lookup"><span data-stu-id="d2ae9-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="d2ae9-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="d2ae9-190">-Zone</span></span>
<span data-ttu-id="d2ae9-191">Gibt die Zonenliste der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="d2ae9-192">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2ae9-192">-Confirm</span></span>
<span data-ttu-id="d2ae9-193">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ae9-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ae9-194">-WhatIf</span></span>
<span data-ttu-id="d2ae9-195">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d2ae9-196">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ae9-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ae9-197">CommonParameters</span></span>
<span data-ttu-id="d2ae9-198">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ae9-199">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ae9-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ae9-200">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2ae9-200">INPUTS</span></span>

### <span data-ttu-id="d2ae9-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2ae9-201">PSVirtualMachine</span></span>
<span data-ttu-id="d2ae9-202">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d2ae9-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d2ae9-203">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2ae9-203">OUTPUTS</span></span>

### <span data-ttu-id="d2ae9-204">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d2ae9-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d2ae9-205">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2ae9-205">NOTES</span></span>

## <span data-ttu-id="d2ae9-206">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2ae9-206">RELATED LINKS</span></span>

[<span data-ttu-id="d2ae9-207">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d2ae9-208">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="d2ae9-209">Neustart-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="d2ae9-210">Anfang-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="d2ae9-211">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="d2ae9-212">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2ae9-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="d2ae9-213">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d2ae9-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="d2ae9-214">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d2ae9-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="d2ae9-215">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d2ae9-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="d2ae9-216">Satz-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d2ae9-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d2ae9-217">Satz-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="d2ae9-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="d2ae9-218">Satz-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="d2ae9-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


