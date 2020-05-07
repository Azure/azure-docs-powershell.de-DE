---
title: Erste Schritte mit Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 61d6d19336dd0e1885570c3a4e8874a849317fa3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722423"
---
# <a name="get-started-with-azure-powershell"></a>Erste Schritte mit Azure PowerShell

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Azure PowerShell ermöglicht die Verwaltung von Azure-Ressourcen über die Befehlszeile sowie die Erstellung von Automatisierungsskripts für Azure Resource Manager. Azure PowerShell kann mit [Azure Cloud Shell](/azure/cloud-shell/overview) im Browser verwendet oder auf dem lokalen Computer installiert werden. Dieser Artikel unterstützt Sie bei den ersten Schritten mit Azure PowerShell und informiert über die wichtigsten Konzepte.

## <a name="install-azure-powershell"></a>Installieren von Azure Powershell

Vergewissern Sie sich zunächst, dass die neueste Version von Azure PowerShell installiert ist. Informationen zur neuesten Version finden Sie in den [Versionshinweisen](./release-notes-azureps.md).

1. [Installieren Sie Azure PowerShell](install-azurerm-ps.md).

2. Führen Sie `Get-InstalledModule AzureRM -AllVersions` über die Befehlszeile aus, um sich zu vergewissern, dass die Installation erfolgreich war.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Die einfachste Möglichkeit, erste Schritte auszuführen, besteht im [Starten von Cloud Shell](/azure/cloud-shell/quickstart).

1. Starten Sie Cloud Shell über den oberen Navigationsbereich im Azure-Portal.

   ![Shell-Symbol](~/media/get-started-azureps/shell-icon.png)

2. Wählen Sie das zu verwendende Abonnement aus, und erstellen Sie ein Speicherkonto.

   ![Speicherkonto erstellen](~/media/get-started-azureps/storage-prompt.png)

Nach Erstellung des Speichers wird von Cloud Shell eine PowerShell-Sitzung im Browser geöffnet.

![Cloud Shell für PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Sie können Azure PowerShell auch installieren und lokal in einer PowerShell-Sitzung verwenden.

## <a name="sign-in-to-azure"></a>Anmelden bei Azure

Melden Sie sich interaktiv an:

1. Geben Sie `Connect-AzureRmAccount`ein. Im daraufhin angezeigten Dialogfeld werden Sie zum Eingeben Ihrer Azure-Anmeldeinformationen aufgefordert. Die Option „-Environment“ ermöglicht eine Authentifizierung für Azure China oder Azure Deutschland.

   Beispiel: Connect-AzureRmAccount -Environment AzureChinaCloud

2. Geben Sie die dem Konto zugeordnete E-Mail-Adresse und das zugehörige Kennwort ein. Die Anmeldeinformationen werden von Azure authentifiziert und gespeichert, dann wird das Fenster geschlossen.

Nach der Anmeldung an einem Azure-Konto können Sie mithilfe der Azure PowerShell-Cmdlets auf die Ressourcen in Ihrem Abonnement zugreifen und sie verwalten.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Erstellen eines virtuellen Windows-Computers mithilfe einfacher Standardeinstellungen

Das Cmdlet `New-AzureRmVM` stellt eine vereinfachte Syntax bereit und erleichtert dadurch die Erstellung eines neuen virtuellen Computers. Sie müssen nur zwei Parameterwerte angeben: den Namen des virtuellen Computers und eine Reihe von Anmeldeinformationen für das lokale Administratorkonto auf dem virtuellen Computer.

Erstellen Sie zunächst das Objekt für die Anmeldeinformationen.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Erstellen Sie anschließend den virtuellen Computer.

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

Sie werden sich vielleicht fragen, welche anderen Elemente erstellt werden und wie der virtuelle Computer konfiguriert wird. Zunächst sehen wir uns unsere Ressourcengruppen an.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Die Ressourcengruppe **cloud-shell-storage-westus** wird bei der ersten Verwendung von Cloud Shell erstellt. Die Ressourcengruppe **SampleVM** wurde vom Cmdlet `New-AzureRmVM` erstellt.

Welche anderen Ressourcen wurden in dieser neuen Ressourcengruppe erstellt?

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

Wir rufen nun weitere Details zum virtuellen Computer ab. Dieses Beispiel zeigt, wie Sie Informationen zum Betriebssystemimage abrufen, das zum Erstellen des virtuellen Computers verwendet wurde.

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Erstellen eines vollständig konfigurierten virtuellen Linux-Computers

Im vorherigen Beispiel wurden die vereinfachte Syntax und die Standardparameterwerte verwenden, um einen virtuellen Windows-Computer zu erstellen. In diesem Beispiel geben wir Werte für alle Optionen des virtuellen Computers an.

### <a name="create-a-resource-group"></a>Erstellen einer Ressourcengruppe

In diesem Beispiel möchten wir eine Ressourcengruppe erstellen. Ressourcengruppen ermöglichen in Azure die Verwaltung mehrerer Ressourcen, die Sie zu einer logischen Gruppe zusammenfassen möchten. So können Sie etwa eine Ressourcengruppe für eine Anwendung oder für ein Projekt erstellen und darin einen virtuellen Computer, eine Datenbank und einen CDN-Dienst hinzufügen.

Erstellen wir doch einmal eine Ressourcengruppe namens „MyResourceGroup“ in der Azure-Region „USA, Westen“. Geben Sie dazu den folgenden Befehl ein:

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

Diese neue Ressourcengruppe wird alle Ressourcen enthalten, die für den neuen von uns erstellten virtuellen Computer erforderlich sind. Um einen neuen virtuellen Linux-Computer zu erstellen, müssen wir zunächst die anderen erforderlichen Ressourcen erstellen und sie einer Konfiguration zuweisen. Diese Konfiguration können wir dann zum Erstellen des virtuellen Computers verwenden. Darüber hinaus benötigen Sie einen öffentlichen SSH-Schlüssel mit dem Namen `id_rsa.pub` im Verzeichnis „.ssh“ Ihres Benutzerprofils.

#### <a name="create-the-required-network-resources"></a>Erstellen der erforderlichen Netzwerkressourcen

Als erstes müssen wir eine Subnetzkonfiguration erstellen, die wir bei der Erstellung des virtuellen Netzwerks verwenden können. Außerdem erstellen wir eine öffentliche IP-Adresse, damit wir eine Verbindung mit dem virtuellen Computer herstellen können. Zum Schutz des Zugriffs auf die öffentliche Adresse erstellen wir eine Netzwerksicherheitsgruppe. Und schließlich erstellen wir unter Verwendung aller vorherigen Ressourcen die virtuelle NIC.

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

### <a name="create-the-vm-configuration"></a>Erstellen der VM-Konfiguration

Nachdem wir nun über die erforderlichen Ressourcen verfügen, können wir das VM-Konfigurationsobjekt erstellen.

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

### <a name="create-the-virtual-machine"></a>Erstellen des virtuellen Computers

Jetzt können wir den virtuellen Computer mit dem VM-Konfigurationsobjekt erstellen.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Nach der Erstellung des virtuellen Computers können Sie sich an Ihrem neuen virtuellen Linux-Computer anmelden. Verwenden Sie hierfür SSH und die öffentliche IP-Adresse des virtuellen Computers, den Sie erstellt haben:

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

## <a name="creating-other-resources-in-azure"></a>Erstellen anderer Ressourcen in Azure

Sie wissen nun, wie Sie eine Ressourcengruppe, einen virtuellen Linux-Computer und einen virtuellen Windows Server-Computer erstellen. Sie können aber auch noch viele andere Arten von Azure-Ressourcen erstellen.

Mithilfe des folgenden create-Befehls können Sie beispielsweise einen Azure-Netzwerklastenausgleich erstellen, den wir dann unseren neu erstellten virtuellen Computern zuordnen können:

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Wir könnten für unsere Infrastruktur auch ein neues privates virtuelles Netzwerk (in Azure für gewöhnlich als VNET bezeichnet) erstellen. Hierzu wird folgender Befehl verwendet:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Das Praktische an Azure und Azure PowerShell ist, dass wir damit nicht nur eine cloudbasierte Infrastruktur erhalten, sondern auch verwaltete Plattformdienste erstellen können. Die verwalteten Plattformdienste lassen sich zudem mit Infrastruktur zu noch leistungsfähigeren Lösungen kombinieren.

So können Sie beispielsweise mithilfe von Azure PowerShell eine Azure AppService-Instanz erstellen. Azure AppService ist ein verwalteter Plattformdienst, der sich bestens zum Hosten von Web-Apps eignet, ohne dass Sie sich dabei Gedanken um die Infrastruktur machen müssen. Nach Erstellung der Azure AppService-Instanz können Sie darin mithilfe folgender Befehle zwei neue Azure-Web-Apps erstellen:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Auflisten der bereitgestellten Ressourcen

Mit dem Cmdlet `Get-AzureRmResource` können Sie die in Azure ausgeführten Ressourcen auflisten. Das folgende Beispiel zeigt die Ressourcen, die wir in der neuen Ressourcengruppe erstellt haben.

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

## <a name="deleting-resources"></a>Löschen von Ressourcen

Zur Bereinigung Ihres Azure-Kontos können Sie die Ressourcen entfernen, die wir in diesem Beispiel erstellt haben. Nicht mehr benötigte Ressourcen können mithilfe der Cmdlets vom Typ `Remove-AzureRm*` gelöscht werden. Verwenden Sie den folgenden Befehl, um den virtuellen Windows-Computer zu entfernen, den wir zuvor erstellt haben:

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Sie werden gefragt, ob Sie die Ressource wirklich entfernen möchten.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Sie können auch eine größere Zahl von Ressourcen gleichzeitig löschen. Mit dem folgenden Befehl wird beispielsweise die Ressourcengruppe „MyResourceGroup“ gelöscht, die wir bisher für alle Beispiele dieses Tutorials verwendet haben.
Es werden auch alle Ressourcen der Gruppe gelöscht.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Der Vorgang kann je nach Anzahl und Typ der Ressourcen mehrere Minuten dauern.

## <a name="get-samples"></a>Herunterladen von Beispielen

Weitere Informationen zu den Verwendungsmöglichkeiten von Azure PowerShell finden Sie in unseren allgemeinen Skripts für [virtuelle Linux-Computer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuelle Windows-Computer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web-Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) und [SQL-Datenbanken](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Nächste Schritte

* [Anmelden mit Azure PowerShell](authenticate-azureps.md)
* [Verwalten von Azure-Abonnements mit Azure PowerShell](manage-subscriptions-azureps.md)
* [Erstellen eines Azure-Dienstprinzipals mit Azure PowerShell](create-azure-service-principal-azureps.md)
* Lesen Sie die Versionshinweise zur Migration von einer älteren Version: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Hilfe aus der Community:
  * [Azure-Forum auf MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](https://go.microsoft.com/fwlink/?LinkId=320213)
