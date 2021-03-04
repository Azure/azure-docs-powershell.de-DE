---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: f80441cb3555d78974c5a838e829cb2ab350183f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937128"
---
# New-AzVmss

## SYNOPSIS
Erstellt einen VMSS.

## SYNTAX

### Standardparameter (Standard)
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
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet New-AzVmss** erstellt einen VmSS (Virtual Machine Scale Set) in Azure.
Verwenden Sie den einfachen Parametersatz ( ), um schnell einen `SimpleParameterSet` vordefinierten VMSS und zugeordnete Ressourcen zu erstellen. Verwenden Sie den Standardparametersatz ( ) für erweiterte Szenarien, wenn Sie jede Komponente des VMSS und jede zugeordnete Ressource vor der Erstellung `DefaultParameter` genau konfigurieren müssen.

## BEISPIELE

### Beispiel 1: Erstellen eines VMSS mithilfe der **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

Mit dem obigen Befehl wird Folgendes mit dem Namen `$vmssName` erstellt:
* Eine Ressourcengruppe
* Ein virtuelles Netzwerk
* Ein Lastenausgleich
* Eine öffentliche IP
* der VMSS mit 2 Instanzen

Das Standardbild, das für die VMs im VMSS ausgewählt wurde, ist `2016-Datacenter Windows Server` und die SKU `Standard_DS1_v2`

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

Das oben beschriebene komplexe Beispiel erstellt einen VMSS. Im Folgenden wird erläutert, was geschieht:
* Mit dem ersten Befehl wird eine Ressourcengruppe mit dem angegebenen Namen und Speicherort erstellt.
* Der zweite Befehl verwendet das **Cmdlet New-AzStorageAccount,** um ein Speicherkonto zu erstellen.
* Der dritte Befehl verwendet dann das **Get-AzStorageAccount-Cmdlet,** um das speicherkonto zu erhalten, das im zweiten Befehl erstellt wurde, und speichert das Ergebnis in der $STOAccount-Variable.
* Der fünfte Befehl verwendet das **Cmdlet New-AzVirtualNetworkSubnetConfig** zum Erstellen eines Subnetzes und speichert das Ergebnis in der Variablen namens $SubNet.
* Der sechste Befehl verwendet das **Cmdlet New-AzVirtualNetwork** zum Erstellen eines virtuellen Netzwerks und speichert das Ergebnis in der Variablen namens $VNet.
* Der siebte Befehl verwendet **das Get-AzVirtualNetwork,** um Informationen über das virtuelle Netzwerk zu erhalten, das im sechsten Befehl erstellt wurde, und speichert die Informationen in der Variablen namens $VNet.
* Der achte und neunte Befehl verwendet **die New-AzPublicIpAddress-** und **Get- AzureRmPublicIpAddress,** um Informationen aus dieser öffentlichen IP-Adresse zu erstellen und zu erhalten.
* Die Befehle speichern die Informationen in der Variablen namens $PubIP.
* Der zehnte Befehl verwendet das **Cmdlet New- AzureRmLoadBalancerFrontendIpConfig,** um einen frontend load balancer zu erstellen, und speichert das Ergebnis in der Variablen $Frontend.
* Der elfte Befehl verwendet **den New-AzLoadBalancerBackendAddressPoolConfig zum Erstellen einer Back-End-Adresspoolkonfiguration** und speichert das Ergebnis in der Variablen namens $BackendAddressPool.
* Der zwölfte Befehl verwendet die **New-AzLoadBalancerProbeConfig** zum Erstellen eines Prüfpunkts und speichert die Sondeninformationen in der Variablen namens $Probe.
* Der 13. Befehl verwendet das **Cmdlet New-AzLoadBalancerInboundNatPoolConfig,** um eine Nat-Poolkonfiguration (Load Balancer Inbound Network Address Translation) zu erstellen.
* Der vierzehnte Befehl verwendet **die New-AzLoadBalancerRuleConfig,** um eine Load Balancerregelkonfiguration zu erstellen, und speichert das Ergebnis in der Variablen namens $LBRule.
* Der fünfzehnte Befehl verwendet das **Cmdlet New-AzLoadBalancer** zum Erstellen eines Lastenausgleichs und speichert das Ergebnis in der Variablen namens $ActualLb.
* Der 16. Befehl verwendet **get-AzLoadBalancer,** um Informationen zum Lastenausgleich zu erhalten, der im fünfzehnten Befehl erstellt wurde, und speichert die Informationen in der Variablen namens $ExpectedLb.
* Der siebzehnte Befehl verwendet das **Cmdlet New-AzVmssIPConfig** zum Erstellen einer VMSS-IP-Konfiguration und speichert die Informationen in der Variablen namens $IPCfg.
* Der 18. Befehl verwendet das **Cmdlet New-AzVmssConfig** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.
* Der neunzehnte Befehl verwendet das **Cmdlet "New-AzVmss",** um das VMSS zu erstellen.

## PARAMETER

### -AllocationMethod
Zuordnungsmethode für die öffentliche IP-Adresse des Skalierungssets (Statisch oder Dynamisch).  Wenn kein Wert angegeben wird, ist die Zuordnung statisch.

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
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.

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

### -Back-EndPoolName
Der Name des Back-End-Adresspools, der im Load Balancer für diesen Skalierungssatz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neuer Back-End-Pool mit demselben Namen wie der Skalierungssatz erstellt.

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

### -Back-EndPort
Back-End-Portnummern, die vom Lastenausgleich für Skalierungssatz verwendet werden, um mit VMs im Skalierungssatz zu kommunizieren.  Wenn keine Werte angegeben werden, werden die Ports 3389 und 5985 für Windows VMS und Port 22 für Linux-VMs verwendet.

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

### -Anmeldeinformationen
Die Administratoranmeldeinformationen (Benutzername und Kennwort) für VMs in diesem Skalierungssatz.

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
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Die Domänennamenbeschriftung für den öffentlichen Fully-Qualified (FQDN) für diesen Skalierungssatz. Dies ist die erste Komponente des Domänennamens, die dem Skalierungssatz automatisch zugewiesen wird. Automatisch zugewiesene Domänennamen verwenden das Formular ( <DomainNameLabel> <Location> . . cloudapp.azure.com). Wenn kein Wert angegeben wird, ist die Standardmäßige Domänennamenbeschriftung die Verkettung von <ScaleSetName> <ResourceGroupName> und.

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
Verwenden Sie UltraSSD-Datenträger für die VMs im Skalierungssatz.

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
Dieser Parameter aktiviert die Verschlüsselung für alle Datenträger, einschließlich des Ressourcen-/Temp-Datenträgers beim Host selbst. Standard: Die Verschlüsselung beim Host wird deaktiviert, es sei denn, diese Eigenschaft ist für die Ressource auf true festgelegt.

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
Die Räumungsrichtlinie für den Skalierungssatz für virtuelle Computer mit niedriger Priorität.  Nur unterstützte Werte sind "Deallocate" und "Delete".

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
Der Name des Frontend-Adresspools, der im Lastenausgleichsmaßstab verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neuer Frontend-Adresspool mit demselben Namen wie der Skalierungssatz erstellt.

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
Gibt die dedizierte Hostgruppe an, in der sich der Skalierungssatz des virtuellen Computers befindet.

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

### -ImageName
Der Name des Bilds für VMs in diesem Skalierungssatz. Wenn kein Wert angegeben wird, wird das Bild "Windows Server 2016 DataCenter" verwendet.

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
Die Anzahl der VM-Bilder im Skalierungssatz.  Wenn kein Wert angegeben wird, werden zwei Instanzen erstellt.

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
Der Name des Lastenausgleichs, der mit diesem Skalierungssatz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neuer Lastenausgleich mit demselben Namen wie der Skalierungssatz erstellt.

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

### -Location
Der Azure-Speicherort, an dem dieser Skalierungssatz erstellt wird.  Wenn kein Wert angegeben wird, wird der Speicherort vom Speicherort anderer Ressourcen abgeleitet, auf die in den Parametern verwiesen wird.

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

### -MaxPreis
Der maximale Preis für die Abrechnung eines Skalierungssets für virtuelle Computer mit geringer Priorität.

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
Back-End-Port für die Übersetzung eingehender Netzwerkadressen.

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

### -PlatformFaultDomainCount
Fehlerdomänenanzahl für jede Platzierungsgruppe.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priorität
Die Priorität für den virtuellen Computer im Skalierungssatz.  Nur unterstützte Werte sind "Normal", "Spot" und "Niedrig".
"Regular" ist für einen normalen virtuellen Computer.
"Spot" ist für virtuelle Spotcomputer.
"Low" ist auch für virtuelle Spotcomputer, wird aber durch "Spot" ersetzt. Verwenden Sie "Spot" statt "Niedrig".

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
Die Ressourcen-ID der Näherungsgruppe, die mit diesem Skalierungssatz verwendet werden soll.

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
Der Name der öffentlichen IP-Adresse, die mit diesem Skalierungssatz verwendet werden soll.  Wenn kein Wert angegeben wird, wird eine neue öffentliche IPAddress mit demselben Namen wie der Skalierungssatz erstellt.

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
Gibt den Namen der Ressourcengruppe des VMSS an.  Wenn kein Wert angegeben wird, wird unter demselben Namen wie der Skalierungssatz eine neue Ressourcengruppe erstellt.

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
Die Regeln, die beim Skalieren in einem Skalierungssatz für virtuelle Computer befolgt werden müssen.  Mögliche Werte sind: "Standard", "OldestVM" und "NewestVM".  "Standard", wenn ein Skalierungssatz für virtuelle Computer skaliert wird, wird der Skalierungssatz zuerst über Zonen verteilt, wenn es sich um einen zonalen Skalierungssatz handelt.  Anschließend wird er so weit wie möglich über Fehlerdomänen hinweg ausgeglichen.  Innerhalb jeder Fehlerdomäne sind die virtuellen Computer, die zum Entfernen ausgewählt wurden, die neuesten, die nicht vor Scale-In geschützt sind.  "OldestVM", wenn ein Skalierungssatz für virtuelle Computer skaliert wird, werden die ältesten virtuellen Computer ausgewählt, die nicht vor Skalierung geschützt sind.  Bei Skalierungssätzen virtueller Virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  In jeder Zone werden die ältesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.  Wenn ein Skalierungssatz für virtuelle Computer skaliert wird, werden die neuesten virtuellen Computer, die nicht vor Scale-In geschützt sind, zum Entfernen ausgewählt.  Bei Skalierungssätzen virtueller Virtueller Computer wird der Skalierungssatz zuerst zonenübergreifend ausgeglichen.  In jeder Zone werden die neuesten virtuellen Computer, die nicht geschützt sind, zum Entfernen ausgewählt.

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
Der Name der Netzwerksicherheitsgruppe, die auf diesen Skalierungssatz angewendet werden soll.  Wenn kein Wert angegeben wird, wird eine Standardmäßige Netzwerksicherheitsgruppe mit demselben Namen wie der Skalierungssatz erstellt und auf den Skalierungssatz angewendet.

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
Verwenden Sie dies, um den Skalierungssatz in einer einzelnen Platzierungsgruppe zu erstellen, standardmäßig sind mehrere Gruppen.

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
Gibt an, dass die Erweiterungen nicht auf den zusätzlichen überprovisionierten VMs ausgeführt werden.

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
Das Adresspräfix des Subnetzes, das von dieser ScaleSet verwendet wird. Standardmäßige Subnetzeinstellungen (192.168.1.0/24) werden angewendet, wenn kein Wert angegeben wird.

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

### -Subnetzname
Der Name des Subnetzes, das mit diesem Skalierungssatz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neues Subnetz mit demselben Namen wie der Skalierungssatz erstellt.

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
Wenn der Parameter vorhanden ist, wird den VM(n) im Skalierungssatz eine verwaltete Systemidentität zugewiesen,die automatisch generiert wird.

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
Der Upgraderichtlinienmodus für VM-Instanzen in diesem Skalierungssatz.  Die Upgraderichtlinie kann automatische, manuelle oder rollende Upgrades angeben.

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
Der Name einer verwalteten Dienstidentität, die den VM(n) im Skalierungssatz zugewiesen werden sollte.

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
Gibt das **VirtualMachineScaleSet-Objekt** an, das die Eigenschaften des von diesem Cmdlet erstellten VMSS enthält.

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
Der Name für das virtuelle Netzwerk, das mit diesem Skalierungssatz verwendet werden soll.  Wenn kein Wert angegeben wird, wird ein neues virtuelles Netzwerk mit demselben Namen wie das Skalierungsset erstellt.

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
Die Größe der VM-Instanzen in diesem Skalierungssatz.  Wenn keine Größe angegeben ist, wird eine Standardgröße (Standard_DS1_v2) verwendet.

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
Das Adresspräfix für das virtuelle Netzwerk, das mit diesem Skalierungssatz verwendet wird.  Standardmäßige Präfixeinstellungen für virtuelle Netzwerkadressen (192.168.0.0/16) werden verwendet, wenn kein Wert angegeben wird.

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
Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugewiesene IP bezeichnet wird, muss von stammen.

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
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTIZEN

## VERWANDTE LINKS

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stopp-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


