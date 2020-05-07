---
title: Erste Schritte mit Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.openlocfilehash: fde36bd3b4e2d5780f74f7bc74267ff611116400
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722474"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="089ce-102">Erste Schritte mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="089ce-102">Get started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="089ce-103">Azure PowerShell ermöglicht die Verwaltung von Azure-Ressourcen über die Befehlszeile sowie die Erstellung von Automatisierungsskripts für Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="089ce-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="089ce-104">Azure PowerShell kann mit [Azure Cloud Shell](/azure/cloud-shell/overview) im Browser verwendet oder auf dem lokalen Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="089ce-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="089ce-105">Dieser Artikel unterstützt Sie bei den ersten Schritten mit Azure PowerShell und informiert über die wichtigsten Konzepte.</span><span class="sxs-lookup"><span data-stu-id="089ce-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="089ce-106">Installieren von Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="089ce-106">Install Azure PowerShell</span></span>

<span data-ttu-id="089ce-107">Vergewissern Sie sich zunächst, dass die neueste Version von Azure PowerShell installiert ist.</span><span class="sxs-lookup"><span data-stu-id="089ce-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="089ce-108">Informationen zur neuesten Version finden Sie in den [Versionshinweisen](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="089ce-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="089ce-109">[Installieren Sie Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="089ce-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="089ce-110">Führen Sie `Get-InstalledModule AzureRM -AllVersions` über die Befehlszeile aus, um sich zu vergewissern, dass die Installation erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="089ce-110">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="089ce-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="089ce-111">Azure Cloud Shell</span></span>

<span data-ttu-id="089ce-112">Die einfachste Möglichkeit, erste Schritte auszuführen, besteht im [Starten von Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="089ce-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="089ce-113">Starten Sie Cloud Shell über den oberen Navigationsbereich im Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="089ce-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell-Symbol](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="089ce-115">Wählen Sie das zu verwendende Abonnement aus, und erstellen Sie ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="089ce-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Speicherkonto erstellen](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="089ce-117">Nach Erstellung des Speichers wird von Cloud Shell eine PowerShell-Sitzung im Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="089ce-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell für PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="089ce-119">Sie können Azure PowerShell auch installieren und lokal in einer PowerShell-Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="089ce-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="089ce-120">Anmelden bei Azure</span><span class="sxs-lookup"><span data-stu-id="089ce-120">Sign in to Azure</span></span>

<span data-ttu-id="089ce-121">Melden Sie sich interaktiv an:</span><span class="sxs-lookup"><span data-stu-id="089ce-121">Sign on interactively:</span></span>

1. <span data-ttu-id="089ce-122">Geben Sie `Connect-AzureRmAccount`ein.</span><span class="sxs-lookup"><span data-stu-id="089ce-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="089ce-123">Im daraufhin erscheinenden Dialogfeld werden Sie zur Eingabe Ihrer Azure-Anmeldeinformationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="089ce-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="089ce-124">Die Option „-Environment“ ermöglicht eine Anmeldung in Azure China oder Azure Deutschland.</span><span class="sxs-lookup"><span data-stu-id="089ce-124">Option '-Environment' can let you login in Azure China or Azure Germany.</span></span>

   <span data-ttu-id="089ce-125">Beispiel: Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="089ce-125">e.g. Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="089ce-126">Geben Sie die dem Konto zugeordnete E-Mail-Adresse und das zugehörige Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="089ce-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="089ce-127">Die Anmeldeinformationen werden von Azure authentifiziert und gespeichert, dann wird das Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="089ce-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="089ce-128">Nach der Anmeldung bei einem Azure-Konto können Sie mithilfe der Azure PowerShell-Cmdlets auf die Ressourcen in Ihrem Abonnement zugreifen und sie verwalten.</span><span class="sxs-lookup"><span data-stu-id="089ce-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="089ce-129">Erstellen eines virtuellen Windows-Computers mithilfe einfacher Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="089ce-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="089ce-130">Das Cmdlet `New-AzureRmVM` stellt eine vereinfachte Syntax bereit und erleichtert dadurch die Erstellung eines neuen virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="089ce-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="089ce-131">Sie müssen nur zwei Parameterwerte angeben: den Namen des virtuellen Computers und eine Reihe von Anmeldeinformationen für das lokale Administratorkonto auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="089ce-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="089ce-132">Erstellen Sie zunächst das Objekt für die Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="089ce-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="089ce-133">Erstellen Sie anschließend den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="089ce-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="089ce-134">Das war einfach.</span><span class="sxs-lookup"><span data-stu-id="089ce-134">That was easy.</span></span> <span data-ttu-id="089ce-135">Sie fragen sich jedoch vielleicht, welche anderen Elemente erstellt werden und wie der virtuelle Computer konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="089ce-135">But, you may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="089ce-136">Zunächst sehen wir uns unsere Ressourcengruppen an.</span><span class="sxs-lookup"><span data-stu-id="089ce-136">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="089ce-137">Die Ressourcengruppe **cloud-shell-storage-westus** wird bei der ersten Verwendung von Cloud Shell erstellt.</span><span class="sxs-lookup"><span data-stu-id="089ce-137">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="089ce-138">Die Ressourcengruppe **SampleVM** wurde vom Cmdlet `New-AzureRmVM` erstellt.</span><span class="sxs-lookup"><span data-stu-id="089ce-138">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="089ce-139">Welche anderen Ressourcen wurden in dieser neuen Ressourcengruppe erstellt?</span><span class="sxs-lookup"><span data-stu-id="089ce-139">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="089ce-140">Wir rufen nun weitere Details zum virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="089ce-140">Let's get some more details about the VM.</span></span> <span data-ttu-id="089ce-141">Dieses Beispiel zeigt, wie Sie Informationen zum Betriebssystemimage abrufen, das zum Erstellen des virtuellen Computers verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="089ce-141">This examples shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="089ce-142">Erstellen eines vollständig konfigurierten virtuellen Linux-Computers</span><span class="sxs-lookup"><span data-stu-id="089ce-142">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="089ce-143">Im vorherigen Beispiel wurden die vereinfachte Syntax und die Standardparameterwerte verwenden, um einen virtuellen Windows-Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-143">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="089ce-144">In diesem Beispiel geben wir Werte für alle Optionen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="089ce-144">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="089ce-145">Erstellen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="089ce-145">Create a resource group</span></span>

<span data-ttu-id="089ce-146">In diesem Beispiel möchten wir eine Ressourcengruppe erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-146">For this example we want to create a Resource Group.</span></span> <span data-ttu-id="089ce-147">Ressourcengruppen ermöglichen in Azure die Verwaltung mehrerer Ressourcen, die Sie zu einer logischen Gruppe zusammenfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="089ce-147">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="089ce-148">So können Sie etwa eine Ressourcengruppe für eine Anwendung oder für ein Projekt erstellen und darin einen virtuellen Computer, eine Datenbank und einen CDN-Dienst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="089ce-148">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="089ce-149">Erstellen wir doch einmal eine Ressourcengruppe namens „MyResourceGroup“ in der Azure-Region „USA, Westen“.</span><span class="sxs-lookup"><span data-stu-id="089ce-149">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="089ce-150">Geben Sie dazu den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="089ce-150">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="089ce-151">Diese neue Ressourcengruppe wird alle Ressourcen enthalten, die für den neuen von uns erstellten virtuellen Computer erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="089ce-151">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="089ce-152">Um einen neuen virtuellen Linux-Computer zu erstellen, müssen wir zunächst die anderen erforderlichen Ressourcen erstellen und sie einer Konfiguration zuweisen.</span><span class="sxs-lookup"><span data-stu-id="089ce-152">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="089ce-153">Diese Konfiguration können wir dann zum Erstellen des virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="089ce-153">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="089ce-154">Darüber hinaus benötigen Sie einen öffentlichen SSH-Schlüssel mit dem Namen `id_rsa.pub` im Verzeichnis „.ssh“ Ihres Benutzerprofils.</span><span class="sxs-lookup"><span data-stu-id="089ce-154">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="089ce-155">Erstellen der erforderlichen Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="089ce-155">Create the required network resources</span></span>

<span data-ttu-id="089ce-156">Als erstes müssen wir eine Subnetzkonfiguration erstellen, die wir bei der Erstellung des virtuellen Netzwerks verwenden können.</span><span class="sxs-lookup"><span data-stu-id="089ce-156">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="089ce-157">Außerdem erstellen wir eine öffentliche IP-Adresse, damit wir eine Verbindung mit dem virtuellen Computer herstellen können.</span><span class="sxs-lookup"><span data-stu-id="089ce-157">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="089ce-158">Zum Schutz des Zugriffs auf die öffentliche Adresse erstellen wir eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="089ce-158">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="089ce-159">Und schließlich erstellen wir unter Verwendung aller vorherigen Ressourcen die virtuelle NIC.</span><span class="sxs-lookup"><span data-stu-id="089ce-159">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="089ce-160">Erstellen der VM-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="089ce-160">Create the VM configuration</span></span>

<span data-ttu-id="089ce-161">Nachdem wir nun über die erforderlichen Ressourcen verfügen, können wir das VM-Konfigurationsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-161">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="089ce-162">Erstellen des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="089ce-162">Create the virtual machine</span></span>

<span data-ttu-id="089ce-163">Jetzt können wir den virtuellen Computer mit dem VM-Konfigurationsobjekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-163">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="089ce-164">Nach Erstellung des virtuellen Computers können Sie sich bei Ihrem neuen virtuellen Linux-Computer anmelden. Verwenden Sie dazu SSH und die öffentliche IP-Adresse des virtuellen Computers, die Sie erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="089ce-164">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="089ce-165">Erstellen anderer Ressourcen in Azure</span><span class="sxs-lookup"><span data-stu-id="089ce-165">Creating other resources in Azure</span></span>

<span data-ttu-id="089ce-166">Sie wissen nun, wie Sie eine Ressourcengruppe, einen virtuellen Linux-Computer und einen virtuellen Windows Server-Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-166">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="089ce-167">Sie können aber auch noch viele andere Arten von Azure-Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-167">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="089ce-168">Mithilfe des folgenden create-Befehls können Sie beispielsweise einen Azure-Netzwerklastenausgleich erstellen, den wir dann unseren neu erstellten virtuellen Computern zuordnen können:</span><span class="sxs-lookup"><span data-stu-id="089ce-168">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="089ce-169">Wir könnten für unsere Infrastruktur auch ein neues privates virtuelles Netzwerk (in Azure für gewöhnlich als VNET bezeichnet) erstellen. Hierzu wird folgender Befehl verwendet:</span><span class="sxs-lookup"><span data-stu-id="089ce-169">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="089ce-170">Das Praktische an Azure und Azure PowerShell ist, dass wir damit nicht nur eine cloudbasierte Infrastruktur erhalten, sondern auch verwaltete Plattformdienste erstellen können.</span><span class="sxs-lookup"><span data-stu-id="089ce-170">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="089ce-171">Die verwalteten Plattformdienste lassen sich zudem mit Infrastruktur zu noch leistungsfähigeren Lösungen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="089ce-171">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="089ce-172">So können Sie beispielsweise mithilfe von Azure PowerShell eine Azure AppService-Instanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="089ce-172">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="089ce-173">Azure AppService ist ein verwalteter Plattformdienst, der sich bestens zum Hosten von Web-Apps eignet, ohne dass Sie sich dabei Gedanken um die Infrastruktur machen müssen.</span><span class="sxs-lookup"><span data-stu-id="089ce-173">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="089ce-174">Nach Erstellung der Azure AppService-Instanz können Sie darin mithilfe folgender Befehle zwei neue Azure-Web-Apps erstellen:</span><span class="sxs-lookup"><span data-stu-id="089ce-174">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="089ce-175">Auflisten der bereitgestellten Ressourcen</span><span class="sxs-lookup"><span data-stu-id="089ce-175">Listing deployed resources</span></span>

<span data-ttu-id="089ce-176">Mit dem Cmdlet `Get-AzureRmResource` können Sie die in Azure ausgeführten Ressourcen auflisten.</span><span class="sxs-lookup"><span data-stu-id="089ce-176">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="089ce-177">Das folgende Beispiel zeigt die Ressourcen, die wir gerade eben in der neuen Ressourcengruppe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="089ce-177">The following example shows the resources we just created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="089ce-178">Löschen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="089ce-178">Deleting resources</span></span>

<span data-ttu-id="089ce-179">Zur Bereinigung Ihres Azure-Kontos können Sie die Ressourcen entfernen, die wir in diesem Beispiel erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="089ce-179">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="089ce-180">Nicht mehr benötigte Ressourcen können mithilfe der Cmdlets vom Typ `Remove-AzureRm*` gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="089ce-180">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="089ce-181">Verwenden Sie den folgenden Befehl, um den virtuellen Windows-Computer zu entfernen, den wir zuvor erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="089ce-181">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="089ce-182">Sie werden gefragt, ob Sie die Ressource wirklich entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="089ce-182">You will be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="089ce-183">Sie können auch mehrere Ressourcen gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="089ce-183">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="089ce-184">Der folgende Befehl löscht beispielsweise die gesamte Ressourcengruppe „MyResourceGroup“, die wir in den Beispielen dieses Tutorials verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="089ce-184">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="089ce-185">Dadurch werden die Ressourcengruppe und sämtliche darin enthaltene Ressourcen entfernt.</span><span class="sxs-lookup"><span data-stu-id="089ce-185">This removes the resource group and all of the resources in it.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="089ce-186">Das kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="089ce-186">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="089ce-187">Herunterladen von Beispielen</span><span class="sxs-lookup"><span data-stu-id="089ce-187">Get samples</span></span>

<span data-ttu-id="089ce-188">Weitere Informationen zu den Verwendungsmöglichkeiten von Azure PowerShell finden Sie in unseren allgemeinen Skripts für [virtuelle Linux-Computer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuelle Windows-Computer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web-Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) und [SQL-Datenbanken](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="089ce-188">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="089ce-189">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="089ce-189">Next steps</span></span>

* [<span data-ttu-id="089ce-190">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="089ce-190">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="089ce-191">Verwalten von Azure-Abonnements mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="089ce-191">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="089ce-192">Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="089ce-192">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="089ce-193">Lesen Sie die Versionshinweise zur Migration von einer älteren Version: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="089ce-193">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="089ce-194">Hilfe aus der Community:</span><span class="sxs-lookup"><span data-stu-id="089ce-194">Get help from the community:</span></span>
  * [<span data-ttu-id="089ce-195">Azure-Forum auf MSDN</span><span class="sxs-lookup"><span data-stu-id="089ce-195">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="089ce-196">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="089ce-196">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
