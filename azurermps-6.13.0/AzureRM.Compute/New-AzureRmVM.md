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
# New-AzureRmVM

## Synopsis
Erstellt einen virtuellen Computer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SimpleParameterSet (Standard)
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DefaultParameterSet
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DiskFileParameterSet
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmVM** erstellt einen virtuellen Computer in Azure.
Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.
Verwenden Sie das New-AzureRmVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.
Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Satz-AzureRmVMOSDisk" zu konfigurieren.
Das `SimpleParameterSet` bietet eine bequeme Methode zum Erstellen eines virtuellen Computers, indem häufige Argumente für die VM-Erstellung optional sind.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Computers
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

Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.
Das Skript fragt einen Benutzernamen und ein Kennwort für den virtuellen Computer ab.
Dieses Skript verwendet mehrere andere Cmdlets.

### Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild
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

In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.
Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.
Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.
Mit dem Cmdlet **Get-AzureSubscription** können Sie Ihren Anmeldestatus bestätigen.

### Beispiel 3: Erstellen eines virtuellen Computers aus einem Marketplace-Abbild ohne öffentliche IP-Adresse
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

In diesem Beispiel wird ein neues Netzwerk bereitgestellt und eine Windows-VM vom Marketplace bereitgestellt, ohne dass eine öffentliche IP-Adresse oder Netzwerksicherheitsgruppe erstellt wird.
Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.

## Parameter

### -AddressPrefix
Das Adresspräfix für das virtuelle Netzwerk, das für den virtuellen Computer erstellt wird.

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

### -AllocationMethod
Die IP-Zuordnungsmethode für die öffentliche IP-Adresse, die für den virtuellen Computer erstellt wird.

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

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.

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

### -AvailabilitySetName
Gibt einen Namen für den Verfügbarkeits Satz an.

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

### – Anmeldeinformationen
Die Administratoranmeldeinformationen für den virtuellen Computer.

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

### -DataDiskSizeInGb
Gibt die Größe von Datenträgern in GB an.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -DisableBginfoExtension
Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.

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

### -Diskdatei
Der lokale Pfad zur virtuellen Festplatten-Datei, die in die Cloud hochgeladen werden soll, und zum Erstellen des virtuellen Computers, und er muss ". VHD" als Suffix aufweisen.

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

### -DomainNameLabel
Die Subdomain-Bezeichnung für den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des VM.  Dies nimmt die Form an `{domainNameLabel}.{location}.cloudapp.azure.com` .

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

### -Bild
Der Name des angezeigten Bilds, auf dem die VM erstellt wird.  Dazu gehören: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Cores, Debian, openSUSE-Leap, RHEL, SLES.

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

### -LicenseType
Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.
Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Windows_Client
- Windows_Server dieser Wert kann nicht aktualisiert werden.
Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.

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

### -Linux
Gibt an, ob die Datenträgerdatei für Linux VM ist, falls angegeben; oder Windows, wenn nicht standardmäßig angegeben.

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

### -Standort
Gibt einen Speicherort für den virtuellen Computer an.

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

### -Name
Der Name der VM-Ressource.

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

### -OpenPorts
Eine Liste der Ports, die für die erstellte VM in der Network Security Group (NSG) geöffnet werden sollen.  Der Standardwert hängt von der Art des ausgewählten Bilds ab (also Windows: 3389, 5985 und Linux: 22).

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

### -PublicIpAddressName
Der Name einer neuen (oder vorhandenen) öffentlichen IP-Adresse, die von der erstellten VM verwendet werden soll.  Wenn keine Angabe erfolgt, wird ein Name generiert.

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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.

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

### -SecurityGroupName
Der Name einer neuen (oder vorhandenen) Netzwerksicherheitsgruppe (NSG), die von der erstellten VM verwendet werden soll.  Wenn keine Angabe erfolgt, wird ein Name generiert.

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

### -Size
Die Größe des virtuellen Computers.  Der Standardwert lautet: Standard_DS1_v2.

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

### -SubnetAddressPrefix
Das Adresspräfix für das Subnetz, das für den virtuellen Computer erstellt wird.

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

### -SubnetName
Der Name eines neuen (oder vorhandenen) Subnets, das von der erstellten VM verwendet werden soll.  Wenn keine Angabe erfolgt, wird ein Name generiert.

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

### -SystemAssignedIdentity
Wenn der Parameter vorhanden ist, wird dem virtuellen Computer eine verwaltete System Identität zugewiesen, die automatisch generiert wird.

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

### -Tag
Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.
Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.
Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.

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

### -UserAssignedIdentity
Der Name einer verwalteten Dienstidentität, die dem virtuellen Computer zugewiesen werden soll.

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

### -VirtualNetworkName
Der Name eines neuen (oder vorhandenen) virtuellen Netzwerks, das von der erstellten VM verwendet werden soll.  Wenn keine Angabe erfolgt, wird ein Name generiert.

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

### -VM
Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.
Verwenden Sie das New-AzureRmVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.
Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzureRmVMOperatingSystem", "AzureRmVMSourceImage" und "Add-AzureRmVMNetworkInterface".

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

### -Zone
Gibt die Zonenliste der virtuellen Maschine an.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

### System. String []

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Notizen

## Verwandte Links

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Neustart-AzureRmVM](./Restart-AzureRmVM.md)

[Anfang-AzureRmVM](./Start-AzureRmVM.md)

[Stopp-AzureRmVM](./Stop-AzureRmVM.md)

[Update-AzureRmVM](./Update-AzureRmVM.md)

[Add-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[Add-AzureRmVMNetworkInterface](./Add-AzureRmVMNetworkInterface.md)

[Neu – AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Satz-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Satz-AzureRmVMSourceImage](./Set-AzureRmVMSourceImage.md)

[Satz-AzureRmVMOSDisk](./Set-AzureRmVMOSDisk.md)


