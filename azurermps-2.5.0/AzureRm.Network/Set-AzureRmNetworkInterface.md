---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 978db7296b9789f738f5b277a4bf3731803fdcd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850304"
---
# Set-AzureRmNetworkInterface

## Synopsis
Legt den Zielstatus für eine Netzwerkschnittstelle fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das **Set-AzureRmNetworkInterface** legt den Zielstatus für eine Azure-Netzwerkschnittstelle fest.

## Beispiele

### Beispiel 1: Konfigurieren einer Netzwerkschnittstelle
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.
Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 in der Ressourcengruppe ResourceGroup1.
Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.
Der dritte Befehl legt die private IP-Zuordnungsmethode auf static fest.
Der vierte Befehl legt ein Tag auf der Netzwerkschnittstelle fest.
Der fünfte Befehl verwendet die in der $NIC-Variablen gespeicherten Informationen, um die Netzwerkschnittstelle einzurichten.

### Beispiel 2: Ändern der DNS-Einstellungen auf einer Netzwerkschnittstelle
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen NetworkInterface1 ab, die innerhalb der Ressourcengruppen-ResourceGroup1 vorhanden ist. Mit dem zweiten Befehl wird dieser Schnittstelle der DNS-Server 192.168.1.100 hinzugefügt. Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an. Wenn Sie einen DNS-Server entfernen möchten, folgen Sie den oben aufgeführten Befehlen, ersetzen Sie aber ". "Mit" hinzufügen. Remove "im zweiten Befehl.

### Beispiel 3: Aktivieren von IP-Forwading auf einer Netzwerkschnittstelle
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen. Mit dem zweiten Befehl wird der Wert für die IP-Weiterleitung in true geändert. Schließlich wendet der dritte Befehl die Änderungen auf die Netzwerkschnittstelle an. Wenn Sie die IP-Weiterleitung auf einer Netzwerkschnittstelle deaktivieren möchten, folgen Sie dem Beispiel Beispiel, aber stellen Sie sicher, dass Sie den zweiten Befehl in "$Nic" ändern. EnableIPForwarding = 0 ".

### Beispiel 4: Ändern des Subnets einer Netzwerkschnittstelle
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

Der erste Befehl ruft die Netzwerkschnittstellen-NetworkInterface1 ab und speichert Sie in der $NIC-Variablen. Der zweite Befehl ruft das virtuelle Netzwerk ab, dem das Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll. Der zweite Befehl ruft das Subnetz ab und speichert es in der Variablen $Subnet 2. Der dritte Befehl verknüpfte die primäre private IP-Adresse der Netzwerkschnittstelle mit dem neuen Subnetz. Schließlich hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle übernommen.

>[!NOTE] 
>Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können. Wenn Sie über statische IP-Konfigurationen verfügen, wechseln Sie dann zu Dynamic, bevor Sie fortfahren. 

>[!NOTE]
>Wenn die Netzwerkschnittstelle über mehrere IP-Konfigurationen verfügt, muss der Befehl Forth für alle diese IP-Konfigurationen ausgeführt werden, bevor der endgültige Set-AzureRmNetworkInterface Befehl ausgeführt wird. Dies kann wie im Befehl Forth erfolgen, aber durch Ersetzen von "0" durch die entsprechende Zahl. Wenn eine Netzwerkschnittstelle über n IP-Konfigurationen verfügt, muss n-1 dieser Befehle vorhanden sein.

### Beispiel 5: zuordnen/distanzieren einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens NetworkInterface1 ab und speichert Sie in der $NIC-Variablen. Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens MyNSG ab und speichert Sie in der $NSG-Variablen. Mit dem Befehl Forth wird die $NSG dem $NIC zugewiesen. Schließlich wendet der fünfte Befehl die Änderungen auf die Netzwerkschnittstelle an. Um Netzwerk Sicherheitsgruppen von einer Netzwerkschnittstelle zu trennen, ersetzen Sie einfach $NSG im Befehl Forth durch $Null.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Network Interface
Gibt ein **Network Interface** -Objekt an, das den Zielstatus für eine Netzwerkschnittstelle darstellt.

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSNetworkInterface
Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## Notizen

## Verwandte Links

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Get-AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[Neu – AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[Remove-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)
