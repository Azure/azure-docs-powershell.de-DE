---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: deb33c8e26dcedd96a6cdb3073b9c71f26750abf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010019"
---
# New-AzVmss

## Synopsis
Erstellt eine VMSS.

## Syntax

### Defaultparameter (Standard)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>] 
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>]
 [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzVmss** erstellt einen virtuellen Computer-Skalierungs Satz (VMSS) in Azure.
Verwenden Sie den einfachen Parametersatz ( `SimpleParameterSet` ), um schnell eine vordefinierte VMSS und zugeordnete Ressourcen zu erstellen. Verwenden Sie den standardmäßigen Parametersatz ( `DefaultParameter` ) für erweiterte Szenarien, wenn Sie jede Komponente des VMSS und jede zugeordnete Ressource vor der Erstellung genau konfigurieren müssen.

## Beispiele

### Beispiel 1: Erstellen einer VMSS mit der **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Der obige Befehl erstellt Folgendes mit dem Namen `$vmssName` :
* Eine Ressourcengruppe
* Ein virtuelles Netzwerk
* Ein Lastenausgleichsmodul
* Eine öffentliche IP-Adresse
* VMSS mit zwei Instanzen

Das für die VMs in der VMSS ausgewählte Standardbild ist `2016-Datacenter Windows Server` und die SKU `Standard_DS1_v2`

### Beispiel 2: Erstellen eines VMSS mithilfe der **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

Im obigen komplexen Beispiel wird eine VMSS erstellt, und im folgenden wird erläutert, was passiert:
* Der erste Befehl erstellt eine Ressourcengruppe mit dem angegebenen Namen und Speicherort.
* Der zweite Befehl verwendet das Cmdlet **New-AzStorageAccount** , um ein Speicherkonto zu erstellen.
* Der dritte Befehl verwendet dann das Cmdlet " **Get-AzStorageAccount** ", um das im zweiten Befehl erstellte Speicherkonto abzurufen, und speichert das Ergebnis in der $STOAccount Variablen.
* Der fünfte Befehl verwendet das Cmdlet **New-AzVirtualNetworkSubnetConfig** , um ein Subnetz zu erstellen und das Ergebnis in der Variablen mit dem Namen $Subnet zu speichern.
* Der sechste Befehl verwendet das Cmdlet **New-AzVirtualNetwork** , um ein virtuelles Netzwerk zu erstellen und das Ergebnis in der Variablen mit dem Namen $VNet zu speichern.
* Der siebte Befehl verwendet die **Get-AzVirtualNetwork-** Funktion, um Informationen zu dem im sechsten Befehl erstellten virtuellen Netzwerk abzurufen und die Informationen in der Variablen mit dem Namen $VNet zu speichern.
* Der achte und neunte Befehl verwendet die **New-AzPublicIpAddress** und **Get-AzureRmPublicIpAddress** , um Informationen aus dieser öffentlichen IP-Adresse zu erstellen und abzurufen.
* Die Befehle speichern die Informationen in der Variablen mit dem Namen $PubIP.
* Der zehnte Befehl verwendet das Cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** , um ein Frontend-Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $Frontend zu speichern.
* Der elfte Befehl verwendet das **New-AzLoadBalancerBackendAddressPoolConfig-Steuer** System, um eine Konfiguration des Back-End-Adresspools zu erstellen und das Ergebnis in der Variablen mit dem Namen $BackendAddressPool zu speichern.
* Der zwölfte Befehl verwendet die **New-AzLoadBalancerProbeConfig-** Funktion, um einen Prüfpunkt zu erstellen und die Prüfpunktinformationen in der Variablen mit dem Namen $Probe zu speichern.
* Der dreizehnte Befehl verwendet das Cmdlet **New-AzLoadBalancerInboundNatPoolConfig** , um eine eingehende Netzwerkadressübersetzung (Network Address Translation, NAT) für den Lastenausgleich zu erstellen.
* Der vierzehnte Befehl verwendet die **New-AzLoadBalancerRuleConfig-** Funktion, um eine Load Balancer-Regelkonfiguration zu erstellen und das Ergebnis in der Variablen mit dem Namen $LBRule zu speichern.
* Der fünfzehnte Befehl verwendet das Cmdlet **New-AzLoadBalancer** , um ein Lastenausgleichsmodul zu erstellen und das Ergebnis in der Variablen mit dem Namen $ActualLb zu speichern.
* Der sechzehnte Befehl verwendet die **Get-AzLoadBalancer-** Funktion, um Informationen über das Load Balancer abzurufen, das im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen mit dem Namen $ExpectedLb.
* Der Befehl "siebzehnte" verwendet das Cmdlet " **New-AzVmssIPConfig** ", um eine VMSS-IP-Konfiguration zu erstellen und die Informationen in der Variablen mit dem Namen $IPCfg zu speichern.
* Der achtzehnte Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.
* Der neunzehnte Befehl verwendet das Cmdlet **New-AzVmss** zum Erstellen des VMSS.

## Parameter

### -AllocationMethod
Zuordnungsmethode für die öffentliche IP-Adresse des Skalierungs Satzes (statisch oder dynamisch).  Wenn kein Wert angegeben wird, ist die Zuweisung statisch.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
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

### -BackendPoolName
Der Name des im Load Balancer für diesen Skalierungs Satz zu verwendenden Back-End-Adresspools.  Wenn kein Wert angegeben wird, wird ein neuer Back-End-Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Back-End-Portnummern, die vom Scale-Satz Load Balancer für die Kommunikation mit VMS im Skalierungs Satz verwendet werden.  Wenn keine Werte angegeben werden, werden Ports 3389 und 5985 für Windows-VMS verwendet, und Port 22 wird für Linux-VMs verwendet.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Anmeldeinformationen
Die Administratoranmeldeinformationen (Benutzername und Kennwort) für VMs in dieser Skalierungs Gruppe.

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
Parameter Sets: SimpleParameterSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
Die Bezeichnung für den Domänennamen für den öffentlichen Fully-Qualified Domänennamen (Fully Domain Name, FQDN) für diesen Skalierungs Satz. Dies ist die erste Komponente des Domänennamens, die dem Skalierungs Satz automatisch zugewiesen wird. Automatisch zugewiesene Domänennamen verwenden das Formular ( <DomainNameLabel> . <Location> . cloudapp.Azure.com). Wenn kein Wert angegeben wird, ist die standardmäßige Domänennamen Beschriftung die Verkettung von <ScaleSetName> und <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltraSSD
Verwenden Sie UltraSSD-Datenträger für die VMs im Skalierungs Satz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Mit diesem Parameter wird die Verschlüsselung für alle Datenträger einschließlich des Ressourcen/Temp-Datenträgers am Host selbst aktiviert. Standard: die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf "true" festgelegt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EvictionPolicy
Die Räumungs Richtlinie für den Skalierungs Satz der virtuellen Maschine mit niedriger Priorität.  Nur Unterstützte Werte sind "freigeben" und "Löschen".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Der Name des zu verwendenden Frontend-Adresspools im Scale-Satz-Lastenausgleichsmodul.  Wenn kein Wert angegeben wird, wird ein neuer Frontend-Adress Pool mit dem gleichen Namen wie der Skalierungs Satz erstellt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostGroupId
Gibt die dedizierte Hostgruppe an, in der sich der Skalierungs Satz des virtuellen Computers befindet.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Bildname
Der Name des Bilds für VMs in dieser Skalierungs Gruppe. Wenn kein Wert angegeben wird, wird das Bild "Windows Server 2016 Datacenter" verwendet.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Die Anzahl der VM-Bilder im Skalierungs Satz.  Wenn kein Wert angegeben wird, werden 2 Instanzen erstellt.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Der Name des Load Balancer, der mit diesem Skalierungs Satz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neues Lastenausgleichsmodul mit dem gleichen Namen wie der Skalierungs Satz erstellt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Die Azure-Position, an der dieser Skalierungs Satz erstellt wird.  Wenn kein Wert angegeben wird, wird der Speicherort von dem Speicherort anderer Ressourcen abgeleitet, auf die in den Parametern verwiesen wird.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Der Höchstbetrag für die Abrechnung einer Skalierungs Gruppe für virtuelle Maschinen mit niedriger Priorität.

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Back-End-Port für eingehende Netzwerkadressübersetzung.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorität
Die Priorität für den virtuellen Computer im Skalierungs Satz.  Nur Unterstützte Werte sind "Normal", "Spot" und "Low".
"Normal" ist für normalen virtuellen Computer.
"Spot" ist für Spot Virtual Machine.
"Low" ist auch für Spot Virtual Machine, wird aber durch "Spot" ersetzt. Bitte verwenden Sie "Spot" anstelle von "Low".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
Die Ressourcen-ID der für diesen Skalierungs Satz zu verwendenden Näherungs Platzierungs Gruppe.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Der Name der öffentlichen IP-Adresse, die mit diesem Skalierungs Satz verwendet werden soll.  Eine neue öffentliche IPAddress mit dem gleichen Namen wie der Skalierungs Satz wird erstellt, wenn kein Wert angegeben wird.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des VMSS an.  Wenn kein Wert angegeben wird, wird eine neue ResourceGroup mit dem gleichen Namen wie der Skalierungs Satz erstellt.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Die Regeln, die beim Skalieren in einem Skalierungs Satz einer virtuellen Maschine befolgt werden müssen.  Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".  "Standard" Wenn der Skalierungs Satz einer virtuellen Maschine skaliert wird, wird der Skalierungs Satz zunächst zonenübergreifend ausbalanciert, wenn es sich um einen Zonal-Skalierungs Satz handelt.  In diesem Fall werden die fehlerdomänen so weit wie möglich ausgeglichen.  Innerhalb jeder fehlerdomäne sind die für die Entfernung ausgewählten virtuellen Computer die neuesten, die nicht vor dem Skalieren geschützt sind.  "OldestVM" Wenn ein Skalierungs Satz für einen virtuellen Computer skaliert wird, werden die ältesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.  Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.  Innerhalb jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.  "NewestVM" Wenn ein Skalierungs Satz für virtuelle Maschinen skaliert wird, werden die neuesten virtuellen Computer, die nicht vor dem Skalieren geschützt sind, zum Entfernen ausgewählt.  Bei Skalen Sätzen für virtuelle Maschinen in Zonal wird der Skalierungs Satz zunächst zonenübergreifend ausgeglichen.  In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Der Name der Netzwerksicherheitsgruppe, die auf diesen Skalierungs Satz angewendet werden soll.  Wenn kein Wert angegeben wird, wird eine standardmäßige Netzwerksicherheitsgruppe mit dem gleichen Namen wie der Skalierungs Satz erstellt und auf den Skalierungs Satz angewendet.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Verwenden Sie diese Einstellung, um den Skalierungs Satz in einer einzelnen Placement-Gruppe zu erstellen, Standard ist mehrere Gruppen

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überlegten VMS ausgeführt werden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Das Adresspräfix des Subnets, das von diesem scaleset verwendet wird. Standardmäßige subneteinstellungen (192.168.1.0/24) werden angewendet, wenn kein Wert angegeben wird.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Der Name des für diesen Skalierungs Satz zu verwendenden Subnets.  Ein neues Subnetz wird mit dem gleichen Namen wie der Skalierungs Satz erstellt, wenn kein Wert angegeben wird.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Wenn der Parameter vorhanden ist, wird den virtuellen Computern im Skalierungs Satz eine verwaltete System Identität zugewiesen, die automatisch generiert wird.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Der Aktualisierungsrichtlinien Modus für VM-Instanzen in dieser Skalierungs Gruppe.  Die Upgrade-Richtlinie kann automatische, manuelle oder parallele Upgrades angeben.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Der Name einer verwalteten Dienstidentität, die den VM (n) im Skalierungs Satz zugewiesen werden soll.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Gibt das **VirtualMachineScaleSet** -Objekt an, das die Eigenschaften des VMSS enthält, das von diesem Cmdlet erstellt wird.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Der Name für das virtuelle Netzwerk, der für diesen Skalierungs Satz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neues virtuelles Netzwerk mit dem gleichen Namen wie der Skalierungs Satz erstellt.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Gibt den Namen des von diesem Cmdlet erstellten VMSS an.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Die Größe der VM-Instanzen in dieser Skalierungs Gruppe.  Wenn keine Größe angegeben ist, wird eine Standardgröße (Standard_DS1_v2) verwendet.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Das Adresspräfix für das virtuelle Netzwerk, das mit diesem Skalierungs Satz verwendet wird.  Standardeinstellungen für das virtuelle Netzwerk Adresspräfix (192.168.0.0/16) werden verwendet, wenn kein Wert angegeben wird.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Notizen

## Verwandte Links

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Neustart-AzVmss](./Restart-AzVmss.md)

[Satz-AzVmss](./Set-AzVmss.md)

[Anfang-AzVmss](./Start-AzVmss.md)

[Stopp-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


