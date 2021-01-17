---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467447"
---
# Add-AzNetworkSecurityRuleConfig

## SYNOPSIS
Fügt einer Netzwerksicherheitsgruppe eine Konfiguration von Netzwerksicherheitsregel hinzu.

## SYNTAX

### SetByResource (Standard)
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzNetworkSecurityRuleConfig"** fügt einer Azure-Netzwerksicherheitsgruppe eine Netzwerksicherheitsregelkonfiguration hinzu.

## BEISPIELE

### 1: Hinzufügen einer Netzwerksicherheitsgruppe
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Der erste Befehl ruft eine Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" aus der Ressourcengruppe "rg1" ab. Der zweite Befehl fügt eine Netzwerksicherheitsregel namens "rdp-rule" hinzu, die Datenverkehr aus dem Internet über Port 3389 zum abgerufenen Netzwerksicherheitsgruppeobjekt zulässt. Die geänderte Azure-Netzwerksicherheitsgruppe wird beibehalten.

### 2: Hinzufügen einer neuen Sicherheitsregel mit Anwendungssicherheitsgruppen
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Zuerst erstellen wir zwei neue Anwendungssicherheitsgruppen. Anschließend rufen wir eine Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" aus der Ressourcengruppe "rg1" ab. und fügen Sie ihr eine Netzwerksicherheitsregel namens "rdp-rule" hinzu. Die Regel ermöglicht Datenverkehr von allen IP-Konfigurationen in der Anwendungssicherheitsgruppe "srcAsg" zu allen IP-Konfigurationen in "destAsg" für Port 3389. Nach dem Hinzufügen der Regel wird die geänderte Azure-Netzwerksicherheitsgruppe beibehalten.

## PARAMETERS

### -Access
Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert wird.
Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

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

### -Beschreibung
Gibt eine Beschreibung der Konfiguration einer Netzwerksicherheitsregel an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAddressPrefix
Gibt ein Zieladressenpräfix an.
Die zulässigen Werte für diesen Parameter sind:
- Eine klassenloses domänenübergreifendes Routing (CIDR)
- Ziel-IP-Adressbereich
- Ein Platzhalterzeichen (*) zur Übereinstimmung mit beliebigen IP-Adressen. Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroup
Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist. Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationApplicationSecurityGroupId
Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt ist. Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPortRange
Gibt einen Zielport oder Zielbereich an.
Die zulässigen Werte für diesen Parameter sind:
- Eine ganze Zahl
- Ein Bereich ganzer Zahlen zwischen 0 und 65535
- Ein Platzhalterzeichen (*) zur Übereinstimmung mit einem Port

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Direction
Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.
Die zulässigen Werte für diesen Parameter sind: "Ein- und ausgehend".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen einer Konfiguration für Netzwerksicherheitsregel an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Gibt ein **NetworkSecurityGroup-Objekt** an.
Dieses Cmdlet fügt dem mit diesem Parameter angegebenen Objekt eine Konfiguration für Netzwerksicherheitsregel hinzu.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Priority
Gibt die Priorität einer Regelkonfiguration an.
Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.
Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.
Je niedriger die Prioritätsnummer, desto höher die Priorität der Regel.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Gibt das Netzwerkprotokoll an, auf das eine Regelkonfiguration angewendet wird.
Die zulässigen Werte für diesen Parameter sind:
- Tcp
- Udp
- Platzhalterzeichen (*) für beides

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddressPrefix
Gibt ein Quelladressenpräfix an.
Die zulässigen Werte für diesen Parameter sind:
- A CIDR
- Ein Quell-IP-Bereich
- Ein Platzhalterzeichen (*) für eine beliebige IP-Adresse.
Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroup
Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist. Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceApplicationSecurityGroupId
Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt ist. Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePortRange
Gibt einen Quellport oder -bereich an.
Dieser Wert wird als ganze Zahl, als Bereich zwischen 0 und 65535 oder als Platzhalterzeichen (*) ausgedrückt, um einem beliebigen Quellport zu entsprechen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


