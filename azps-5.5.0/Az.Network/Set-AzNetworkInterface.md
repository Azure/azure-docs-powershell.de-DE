---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154084"
---
# Set-AzNetworkInterface

## SYNOPSIS
Aktualisiert eine Netzwerkschnittstelle.

## SYNTAX

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
**Set-AzNetworkInterface aktualisiert** eine Netzwerkschnittstelle.

## BEISPIELE

### Beispiel 1: Konfigurieren einer Netzwerkschnittstelle
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

In diesem Beispiel wird eine Netzwerkschnittstelle konfiguriert.
Der erste Befehl ruft eine Netzwerkschnittstelle namens "NetworkInterface1" in der Ressourcengruppe "ResourceGroup1" ab.
Der zweite Befehl legt die private IP-Adresse der IP-Konfiguration fest.
Der dritte Befehl legt die Private -IP-Zuweisungsmethode auf "Static" fest.
Der vierte Befehl legt ein Tag für die Netzwerkschnittstelle fest.
Der fünfte Befehl verwendet die in der Variablen $Nic gespeicherten Informationen zum Festlegen der Netzwerkschnittstelle.

### Beispiel 2: Ändern von DNS-Einstellungen auf einer Netzwerkschnittstelle
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Der erste Befehl ruft eine Netzwerkschnittstelle namens "NetworkInterface1" ab, die in der Ressourcengruppe "ResourceGroup1" vorhanden ist. Mit dem zweiten Befehl wird dieser Schnittstelle der DNS-Server 192.168.1.100 hinzufügt. Der dritte Befehl wendet diese Änderungen auf die Netzwerkschnittstelle an. Zum Entfernen eines DNS-Servers folgen Sie den oben aufgeführten Befehlen, ersetzen aber ". Hinzufügen" mit ". Remove" im zweiten Befehl aus.

### Beispiel 3: Aktivieren der IP-Weiterleitung auf einer Netzwerkschnittstelle
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens "NetworkInterface1" ab und speichert sie in der $nic Variable. Mit dem zweiten Befehl wird der Wert für die IP-Weiterleitung auf "true" geändert. Schließlich wendet der dritte Befehl die Änderungen an der Netzwerkschnittstelle an. Um die IP-Weiterleitung auf einer Netzwerkschnittstelle zu deaktivieren, folgen Sie dem Beispielbeispiel. Achten Sie jedoch darauf, den zweiten Befehl in "$nic. EnableIPForwarding = 0".

### Beispiel 4: Ändern des Subnetzes einer Netzwerkschnittstelle
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Der erste Befehl ruft die Netzwerkschnittstelle "NetworkInterface1" ab und speichert sie in der $nic Variable. Der zweite Befehl ruft das virtuelle Netzwerk ab, das dem Subnetz zugeordnet ist, dem die Netzwerkschnittstelle zugeordnet werden soll. Der zweite Befehl ruft das Subnetz ab und speichert es in der $subnet 2-Variable. Der dritte Befehl hat dem neuen Subnetz die primäre private IP-Adresse der Netzwerkschnittstelle zugeordnet. Zuletzt hat der letzte Befehl diese Änderungen auf der Netzwerkschnittstelle angewendet.
>[!NOTE] 
>Die IP-Konfigurationen müssen dynamisch sein, bevor Sie das Subnetz ändern können. Wenn Sie über statische IP-Konfigurationen verfügen, ändern Sie diese in "Dynamisch", bevor Sie fortfahren. 
>[!NOTE]
>Verfügt die Netzwerkschnittstelle über mehrere IP-Konfigurationen, muss der vierte Befehl für alle diese IP-Konfigurationen ausgeführt werden, bevor der Set-AzNetworkInterface ausgeführt wird. Dies kann wie im vierten Befehl geschehen, aber durch Ersetzen von "0" durch die entsprechende Zahl. Wenn eine Netzwerkschnittstelle über N-IP-Konfigurationen verfügt, müssen N-1 dieser Befehle vorhanden sein.

### Beispiel 5: Zuordnen/Trennen einer Netzwerksicherheitsgruppe zu einer Netzwerkschnittstelle
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens "NetworkInterface1" ab und speichert sie in der $nic Variable. Der zweite Befehl ruft eine vorhandene Netzwerksicherheitsgruppe namens "MyNSG" ab und speichert sie in $nsg Variable. Der dritte Befehl weist die $nsg dem $nic. Schließlich wendet der vierte Befehl die Änderungen auf die Netzwerkschnittstelle an. Um Netzwerksicherheitsgruppen von einer Netzwerkschnittstelle zu trennen, ersetzen Sie einfach $nsg im dritten Befehl durch $null.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -NetworkInterface
Gibt ein Netzwerkschnittstellenobjekt an, das den Zustand darstellt, auf den die Netzwerkschnittstelle festgelegt werden soll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
