---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetwork.md
ms.openlocfilehash: d131b4aa22f46fed151486ed2d87f32684b6035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174563"
---
# New-AzVirtualNetwork

## Synopsis
Erstellt ein virtuelles Netzwerk.

## Syntax

```
New-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String> -AddressPrefix <String[]>
 [-DnsServer <String[]>] [-Subnet <PSSubnet[]>] [-BgpCommunity <String>] [-Tag <Hashtable>]
 [-EnableDdosProtection] [-DdosProtectionPlanId <String>] [-IpAllocation <PSIpAllocation[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzVirtualNetwork** wird ein Azure-virtuelles Netzwerk erstellt.

## Beispiele

### Beispiel 1: Erstellen eines virtuellen Netzwerks mit zwei Subnetzen
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen erstellt. Zunächst wird eine neue Ressourcengruppe in der Region centralus erstellt. Anschließend werden im Beispiel in-Memory-Darstellungen von zwei Subnetzen erstellt. Das New-AzVirtualNetworkSubnetConfig-Cmdlet erstellt kein Subnetz auf der Serverseite. Es gibt ein Subnetz namens frontendSubnet und ein Subnetz mit dem Namen backendSubnet. Das New-AzVirtualNetwork-Cmdlet erstellt dann ein virtuelles Netzwerk mit dem CIDR-10.0.0.0/16 als Adresspräfix und zwei Subnetzen.

### Beispiel 2: Erstellen eines virtuellen Netzwerks mit DNS-Einstellungen
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

In diesem Beispiel wird ein virtuelles Netzwerk mit zwei Subnetzen und zwei DNS-Servern erstellt. Die Angabe der DNS-Server im virtuellen Netzwerk bewirkt, dass die NICs/VMS, die in diesem virtuellen Netzwerk bereitgestellt werden, diese DNS-Server als Standardwerte erben. Diese Standardeinstellungen können pro NIC über eine NIC-Level-Einstellung überschrieben werden. Wenn auf einem VNET keine DNS-Server und keine DNS-Server auf den NICs angegeben sind, werden die standardmäßigen Azure-DNS-Server für die DNS-Auflösung verwendet.

### Beispiel 3: Erstellen eines virtuellen Netzwerks mit einem Subnetz, das auf eine Netzwerksicherheitsgruppe verweist
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule              = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet       = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet        = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

In diesem Beispiel wird ein virtuelles Netzwerk mit Subnetzen erstellt, die auf eine Netzwerksicherheitsgruppe verweisen. Im Beispiel wird zunächst eine Ressourcengruppe als Container für die zu erstellden Ressourcen erstellt. Anschließend wird eine Netzwerksicherheitsgruppe erstellt, die den eingehenden RDP-Zugriff zulässt, aber ansonsten die standardmäßigen Netzwerk Sicherheitsgruppen Regeln erzwingt. Das New-AzVirtualNetworkSubnetConfig-Cmdlet erstellt dann in-Memory-Darstellungen von zwei Subnetzen, die beide auf die erstellte Netzwerksicherheitsgruppe verweisen. Mit dem Befehl New-AzVirtualNetwork wird dann das virtuelle Netzwerk erstellt.

## Parameter

### -AddressPrefix
Gibt einen Bereich von IP-Adressen für ein virtuelles Netzwerk an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -BgpCommunity
Die BGP-Community, die über Express Route angekündigt wurde.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DdosProtectionPlanId
Verweis auf die dem virtuellen Netzwerk zugeordnete Ressource für DDoS-Schutzplan.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DnsServer
Gibt den DNS-Server für ein Subnetz an.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableDdosProtection
Ein Switch-Parameter, der darstellt, ob DDoS-Schutz aktiviert ist oder nicht.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -IpAllocation
Gibt IpAllocations für ein virtuelles Netzwerk an.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Bereich für das virtuelle Netzwerk an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen des virtuellen Netzwerks an, das von diesem Cmdlet erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, die das virtuelle Netzwerk enthalten soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subnetz
Gibt eine Liste der Subnetze an, die dem virtuellen Netzwerk zugeordnet werden sollen.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
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

### System. String []

### Microsoft. Azure. Commands. Network. Models. PSSubnet []

### System. Collections. Hashtable

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork

## Notizen

## Verwandte Links

[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)

[Remove-AzVirtualNetwork](./Remove-AzVirtualNetwork.md)

[Satz-AzVirtualNetwork](./Set-AzVirtualNetwork.md)

[Neu – AzDdosProtectionPlan](./New-AzDdosProtectionPlan.md)
