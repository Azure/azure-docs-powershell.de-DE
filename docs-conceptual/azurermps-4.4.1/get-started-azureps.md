---
title: Erste Schritte mit Azure PowerShell | Microsoft-Dokumentation
description: 'Weitere Informationen: Erste Schritte mit Azure PowerShell'
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 78f8217bf9fefba37dc1f9d11d9331ac3a7170d9
ms.sourcegitcommit: 3715500acad08bcc482b0465edddaafb7b95cb9e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "98566076"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="b71ce-103">Erste Schritte mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b71ce-103">Getting started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="b71ce-104">Azure PowerShell ermöglicht die Verwaltung von Azure-Ressourcen über die Befehlszeile sowie die Erstellung von Automatisierungsskripts für Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b71ce-104">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="b71ce-105">Azure PowerShell kann mit [Azure Cloud Shell](/azure/cloud-shell/overview) im Browser verwendet oder auf dem lokalen Computer installiert und in einer beliebigen PowerShell-Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b71ce-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="b71ce-106">Dieser Artikel hilft Ihnen beim Einstieg und informiert über die wichtigsten Konzepte.</span><span class="sxs-lookup"><span data-stu-id="b71ce-106">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="b71ce-107">Verbinden</span><span class="sxs-lookup"><span data-stu-id="b71ce-107">Connect</span></span>

<span data-ttu-id="b71ce-108">Die einfachste Möglichkeit, erste Schritte auszuführen, besteht im [Starten von Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="b71ce-108">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="b71ce-109">Starten Sie Cloud Shell über den oberen Navigationsbereich im Azure-Portal.</span><span class="sxs-lookup"><span data-stu-id="b71ce-109">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell-Symbol](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="b71ce-111">Wählen Sie das zu verwendende Abonnement aus, und erstellen Sie ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b71ce-111">Choose the subscription you want to use and create a storage account.</span></span>

   ![Speicherkonto erstellen](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="b71ce-113">Nach Erstellung des Speichers wird von Cloud Shell eine PowerShell-Sitzung im Browser geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b71ce-113">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell für PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="b71ce-115">Sie können Azure PowerShell auch installieren und lokal in einer PowerShell-Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="b71ce-115">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="b71ce-116">Installieren von Azure Powershell</span><span class="sxs-lookup"><span data-stu-id="b71ce-116">Install Azure PowerShell</span></span>

<span data-ttu-id="b71ce-117">Vergewissern Sie sich zunächst, dass die neueste Version von Azure PowerShell installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b71ce-117">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="b71ce-118">Informationen zur neuesten Version finden Sie in den [Versionshinweisen](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b71ce-118">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="b71ce-119">[Installieren Sie Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="b71ce-119">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="b71ce-120">Führen Sie `Get-InstalledModule AzureRM -AllVersions` über die Befehlszeile aus, um sich zu vergewissern, dass die Installation erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b71ce-120">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="b71ce-121">Anmelden bei Azure</span><span class="sxs-lookup"><span data-stu-id="b71ce-121">Sign in to Azure</span></span>

<span data-ttu-id="b71ce-122">Melden Sie sich interaktiv an:</span><span class="sxs-lookup"><span data-stu-id="b71ce-122">Sign on interactively:</span></span>

1. <span data-ttu-id="b71ce-123">Geben Sie `Login-AzureRmAccount`ein.</span><span class="sxs-lookup"><span data-stu-id="b71ce-123">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="b71ce-124">Im daraufhin erscheinenden Dialogfeld werden Sie zur Eingabe Ihrer Azure-Anmeldeinformationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b71ce-124">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="b71ce-125">Die Option „-EnvironmentName“ ermöglicht eine Authentifizierung für Azure China oder Azure Deutschland.</span><span class="sxs-lookup"><span data-stu-id="b71ce-125">Option '-EnvironmentName' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="b71ce-126">Beispiel: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="b71ce-126">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="b71ce-127">Geben Sie die dem Konto zugeordnete E-Mail-Adresse und das zugehörige Kennwort ein.</span><span class="sxs-lookup"><span data-stu-id="b71ce-127">Type the email address and password associated with your account.</span></span> <span data-ttu-id="b71ce-128">Die Anmeldeinformationen werden von Azure authentifiziert und gespeichert, dann wird das Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-128">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="b71ce-129">Nach der Anmeldung bei einem Azure-Konto können Sie mithilfe der Azure PowerShell-Cmdlets auf die Ressourcen in Ihrem Abonnement zugreifen und sie verwalten.</span><span class="sxs-lookup"><span data-stu-id="b71ce-129">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="b71ce-130">Erstellen einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b71ce-130">Create a resource group</span></span>

<span data-ttu-id="b71ce-131">Nachdem nun alles eingerichtet ist, können wir mit Azure PowerShell Ressourcen in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-131">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="b71ce-132">Erstellen Sie zunächst eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b71ce-132">First, create a Resource Group.</span></span> <span data-ttu-id="b71ce-133">Ressourcengruppen ermöglichen in Azure die Verwaltung mehrerer Ressourcen, die Sie zu einer logischen Gruppe zusammenfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="b71ce-133">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="b71ce-134">So können Sie etwa eine Ressourcengruppe für eine Anwendung oder für ein Projekt erstellen und darin einen virtuellen Computer, eine Datenbank und einen CDN-Dienst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-134">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="b71ce-135">Erstellen wir doch einmal eine Ressourcengruppe namens „MyResourceGroup“ in der Azure-Region „USA, Westen“.</span><span class="sxs-lookup"><span data-stu-id="b71ce-135">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="b71ce-136">Geben Sie dazu den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="b71ce-136">To do so type the following command:</span></span>

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="b71ce-137">Erstellen eines virtuellen Windows-Computers</span><span class="sxs-lookup"><span data-stu-id="b71ce-137">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="b71ce-138">Nachdem wir nun über eine Ressourcengruppe verfügen, erstellen wir darin einen virtuellen Windows-Computer.</span><span class="sxs-lookup"><span data-stu-id="b71ce-138">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="b71ce-139">Um einen neuen virtuellen Computer zu erstellen, müssen wir zunächst die anderen erforderlichen Ressourcen erstellen und sie einer Konfiguration zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-139">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="b71ce-140">Diese Konfiguration können wir dann zum Erstellen des virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="b71ce-140">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="b71ce-141">Erstellen der erforderlichen Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="b71ce-141">Create the required network resources</span></span>

<span data-ttu-id="b71ce-142">Als erstes müssen wir eine Subnetzkonfiguration erstellen, die wir bei der Erstellung des virtuellen Netzwerks verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b71ce-142">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="b71ce-143">Außerdem erstellen wir eine öffentliche IP-Adresse, damit wir eine Verbindung mit dem virtuellen Computer herstellen können.</span><span class="sxs-lookup"><span data-stu-id="b71ce-143">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="b71ce-144">Zum Schutz des Zugriffs auf die öffentliche Adresse erstellen wir eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b71ce-144">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="b71ce-145">Und schließlich erstellen wir unter Verwendung aller vorherigen Ressourcen die virtuelle NIC.</span><span class="sxs-lookup"><span data-stu-id="b71ce-145">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="b71ce-146">Erstellen des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b71ce-146">Create the virtual machine</span></span>

<span data-ttu-id="b71ce-147">Zunächst einmal benötigen wir Anmeldeinformationen für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="b71ce-147">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="b71ce-148">Nachdem wir nun über die erforderlichen Ressourcen verfügen, können wir den virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-148">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="b71ce-149">Für diesen Schritt erstellen wir ein VM-Konfigurationsobjekt und verwenden die Konfiguration dann zur Erstellung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b71ce-149">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="b71ce-150">Der Befehl `New-AzureRmVM` gibt Ergebnisse aus, wenn der virtuelle Computer vollständig erstellt wurde und einsatzbereit ist.</span><span class="sxs-lookup"><span data-stu-id="b71ce-150">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="b71ce-151">Melden Sie sich nun unter Verwendung von Remotedesktop und der öffentlichen IP-Adresse des virtuellen Computers bei Ihrem neu erstellten virtuellen Windows Server-Computer an.</span><span class="sxs-lookup"><span data-stu-id="b71ce-151">Now sign in to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="b71ce-152">Der folgende Befehl zeigt die öffentliche IP-Adresse an, die im vorherigen Skript erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b71ce-152">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="b71ce-153">Bei einem Windows-basierten System können Sie hierzu über die Befehlszeile den Befehl „mstsc“ ausführen:</span><span class="sxs-lookup"><span data-stu-id="b71ce-153">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="b71ce-154">Geben Sie bei der Anmeldung die gleiche Kombination aus Benutzername und Kennwort an, die Sie auch beim Erstellen des virtuellen Computers verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b71ce-154">Supply the same username/password combination you used when creating the VM to sign in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="b71ce-155">Erstellen eines virtuellen Linux-Computers</span><span class="sxs-lookup"><span data-stu-id="b71ce-155">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="b71ce-156">Um einen neuen virtuellen Linux-Computer zu erstellen, müssen wir zunächst die anderen erforderlichen Ressourcen erstellen und sie einer Konfiguration zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-156">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="b71ce-157">Diese Konfiguration können wir dann zum Erstellen des virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="b71ce-157">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="b71ce-158">Hierbei wird davon ausgegangen, dass Sie bereits die Ressourcengruppe erstellt haben, wie weiter oben gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b71ce-158">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="b71ce-159">Darüber hinaus benötigen Sie einen öffentlichen SSH-Schlüssel mit dem Namen `id_rsa.pub` im Verzeichnis „.ssh“ Ihres Benutzerprofils.</span><span class="sxs-lookup"><span data-stu-id="b71ce-159">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="b71ce-160">Erstellen der erforderlichen Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="b71ce-160">Create the required network resources</span></span>

<span data-ttu-id="b71ce-161">Als erstes müssen wir eine Subnetzkonfiguration erstellen, die wir bei der Erstellung des virtuellen Netzwerks verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b71ce-161">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="b71ce-162">Außerdem erstellen wir eine öffentliche IP-Adresse, damit wir eine Verbindung mit dem virtuellen Computer herstellen können.</span><span class="sxs-lookup"><span data-stu-id="b71ce-162">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="b71ce-163">Zum Schutz des Zugriffs auf die öffentliche Adresse erstellen wir eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b71ce-163">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="b71ce-164">Und schließlich erstellen wir unter Verwendung aller vorherigen Ressourcen die virtuelle NIC.</span><span class="sxs-lookup"><span data-stu-id="b71ce-164">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="b71ce-165">Erstellen des virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="b71ce-165">Create the virtual machine</span></span>

<span data-ttu-id="b71ce-166">Nachdem wir nun über die erforderlichen Ressourcen verfügen, können wir den virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-166">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="b71ce-167">Für diesen Schritt erstellen wir ein VM-Konfigurationsobjekt und verwenden die Konfiguration dann zur Erstellung des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b71ce-167">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="b71ce-168">Nach Erstellung des virtuellen Computers können Sie sich bei Ihrem neuen virtuellen Linux-Computer anmelden. Verwenden Sie dazu SSH und die öffentliche IP-Adresse des virtuellen Computers, die Sie erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="b71ce-168">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="b71ce-169">Erstellen anderer Ressourcen in Azure</span><span class="sxs-lookup"><span data-stu-id="b71ce-169">Creating other resources in Azure</span></span>

<span data-ttu-id="b71ce-170">Sie wissen nun, wie Sie eine Ressourcengruppe, einen virtuellen Linux-Computer und einen virtuellen Windows Server-Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-170">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="b71ce-171">Sie können aber auch noch viele andere Arten von Azure-Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-171">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="b71ce-172">Mithilfe des folgenden create-Befehls können Sie beispielsweise einen Azure-Netzwerklastenausgleich erstellen, den wir dann unseren neu erstellten virtuellen Computern zuordnen können:</span><span class="sxs-lookup"><span data-stu-id="b71ce-172">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="b71ce-173">Wir könnten für unsere Infrastruktur auch ein neues privates virtuelles Netzwerk (in Azure für gewöhnlich als VNET bezeichnet) erstellen. Hierzu wird folgender Befehl verwendet:</span><span class="sxs-lookup"><span data-stu-id="b71ce-173">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="b71ce-174">Das Praktische an Azure und Azure PowerShell ist, dass wir damit nicht nur eine cloudbasierte Infrastruktur erhalten, sondern auch verwaltete Plattformdienste erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b71ce-174">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="b71ce-175">Die verwalteten Plattformdienste lassen sich zudem mit Infrastruktur zu noch leistungsfähigeren Lösungen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="b71ce-175">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="b71ce-176">So können Sie beispielsweise mithilfe von Azure PowerShell eine Azure AppService-Instanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-176">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="b71ce-177">Azure AppService ist ein verwalteter Plattformdienst, der sich bestens zum Hosten von Web-Apps eignet, ohne dass Sie sich dabei Gedanken um die Infrastruktur machen müssen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-177">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="b71ce-178">Nach Erstellung der Azure AppService-Instanz können Sie darin mithilfe folgender Befehle zwei neue Azure-Web-Apps erstellen:</span><span class="sxs-lookup"><span data-stu-id="b71ce-178">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="b71ce-179">Auflisten der bereitgestellten Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b71ce-179">Listing deployed resources</span></span>

<span data-ttu-id="b71ce-180">Mit dem Cmdlet `Get-AzureRmResource` können Sie die in Azure ausgeführten Ressourcen auflisten.</span><span class="sxs-lookup"><span data-stu-id="b71ce-180">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="b71ce-181">Das folgende Beispiel zeigt die Ressourcen, die wir gerade eben in der neuen Ressourcengruppe erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b71ce-181">The following example shows the resources we just created in the new resource group.</span></span>

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
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

## <a name="deleting-resources"></a><span data-ttu-id="b71ce-182">Löschen von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b71ce-182">Deleting resources</span></span>

<span data-ttu-id="b71ce-183">Zur Bereinigung Ihres Azure-Kontos können Sie die Ressourcen entfernen, die wir in diesem Beispiel erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b71ce-183">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="b71ce-184">Nicht mehr benötigte Ressourcen können mithilfe der Cmdlets vom Typ `Remove-AzureRm*` gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b71ce-184">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="b71ce-185">Verwenden Sie den folgenden Befehl, um den virtuellen Windows-Computer zu entfernen, den wir zuvor erstellt haben:</span><span class="sxs-lookup"><span data-stu-id="b71ce-185">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="b71ce-186">Sie werden gefragt, ob Sie die Ressource wirklich entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="b71ce-186">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b71ce-187">Sie können auch mehrere Ressourcen gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="b71ce-187">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="b71ce-188">Der folgende Befehl löscht beispielsweise die gesamte Ressourcengruppe „MyResourceGroup“, die wir in den Beispielen dieses Tutorials verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b71ce-188">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="b71ce-189">Dadurch werden die Ressourcengruppe und sämtliche darin enthaltene Ressourcen entfernt.</span><span class="sxs-lookup"><span data-stu-id="b71ce-189">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="b71ce-190">Das kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="b71ce-190">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="b71ce-191">Herunterladen von Beispielen</span><span class="sxs-lookup"><span data-stu-id="b71ce-191">Get samples</span></span>

<span data-ttu-id="b71ce-192">Weitere Informationen zu den Verwendungsmöglichkeiten von Azure PowerShell finden Sie in unseren allgemeinen Skripts für [virtuelle Linux-Computer](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuelle Windows-Computer](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web-Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) und [SQL-Datenbanken](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="b71ce-192">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="b71ce-193">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="b71ce-193">Next steps</span></span>

* [<span data-ttu-id="b71ce-194">Anmelden mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b71ce-194">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="b71ce-195">Verwalten von Azure-Abonnements mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b71ce-195">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="b71ce-196">Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b71ce-196">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="b71ce-197">Lesen Sie die [Versionshinweise](./release-notes-azureps.md) zur Migration von einer älteren Version.</span><span class="sxs-lookup"><span data-stu-id="b71ce-197">Read the [Release notes](./release-notes-azureps.md) about migrating from an older release.</span></span>
* <span data-ttu-id="b71ce-198">Hilfe aus der Community:</span><span class="sxs-lookup"><span data-stu-id="b71ce-198">Get help from the community:</span></span>
  * [<span data-ttu-id="b71ce-199">Azure-Forum auf MSDN</span><span class="sxs-lookup"><span data-stu-id="b71ce-199">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="b71ce-200">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="b71ce-200">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
