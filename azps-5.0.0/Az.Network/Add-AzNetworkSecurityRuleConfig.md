---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177260"
---
# Add-AzNetworkSecurityRuleConfig

## Synopsis
Fügt eine Netzwerk Sicherheitsregel-Konfiguration zu einer Netzwerksicherheitsgruppe hinzu.

## Syntax

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

## Beschreibung
Mit dem Cmdlet **Add-AzNetworkSecurityRuleConfig** wird eine Netzwerk Sicherheitsregel-Konfiguration zu einer Azure Network Security-Gruppe hinzugefügt.

## Beispiele

### 1: Hinzufügen einer Netzwerksicherheitsgruppe
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

Der erste Befehl ruft eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab. Der zweite Befehl fügt eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu, die den Datenverkehr vom Internet auf Port 3389 zum abgerufenen Netzwerk Sicherheitsgruppenobjekt ermöglicht. Behält die geänderte Azure Network Security-Gruppe bei.

### 2: Hinzufügen einer neuen Sicherheitsregel mit Anwendungs Sicherheitsgruppen
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

Zunächst erstellen wir zwei neue Anwendungs Sicherheitsgruppen. Anschließend rufen wir eine Azure Network Security-Gruppe mit dem Namen "nsg1" aus der Ressourcengruppe "RG1" ab. und fügen Sie eine Netzwerk Sicherheitsregel mit dem Namen "RDP-Regel" hinzu. Die Regel ermöglicht den Datenverkehr von allen IP-Konfigurationen in der Anwendungs Sicherheitsgruppe "srcAsg" zu allen IP-Konfigurationen in "destAsg" auf Port 3389. Nach dem Hinzufügen der Regel behalten wir die geänderte Azure Network Security-Gruppe bei.

## Parameter

### -Access
Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird.
Zulässige Werte für diesen Parameter sind: allow und Deny.

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

### -Beschreibung
Gibt eine Beschreibung der Konfiguration einer Netzwerk Sicherheitsregel an.

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
Gibt ein Ziel Adresspräfix an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Eine CIDR-Adresse (classlos InterDomain Routing)
- Ein Ziel-IP-Adressbereich
- Ein Platzhalterzeichen (*), das einer beliebigen IP-Adresse entspricht, die Sie mit Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden können.

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
Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist. Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.

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
Die Anwendungs Sicherheitsgruppe, die als Ziel für die Regel definiert ist. Sie kann nicht mit dem "DestinationAddressPrefix"-Parameter verwendet werden.

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
Gibt einen Zielport oder einen Zielbereich an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Eine ganze Zahl
- Ein Bereich von ganzen Zahlen zwischen 0 und 65535
- Ein Platzhalterzeichen (*), das mit einem beliebigen Port übereinstimmt

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

### -Richtung
Gibt an, ob eine Regel für eingehenden oder ausgehenden Datenverkehr ausgewertet wird.
Die zulässigen Werte für diesen Parameter lauten: ein-und ausgehende.

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
Gibt den Namen einer Netzwerk Sicherheitsregel Konfiguration an.

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
Gibt ein **NetworkSecurityGroup** -Objekt an.
Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, eine Konfiguration für die Netzwerk Sicherheitsregel hinzu.

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

### -Priorität
Gibt die Priorität einer Regelkonfiguration an.
Die zulässigen Werte für diesen Parameter sind: eine ganze Zahl zwischen 100 und 4096.
Die Prioritätsnummer muss für jede Regel in der Sammlung eindeutig sein.
Je niedriger die Prioritätszahl ist, desto höher ist die Priorität der Regel.

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

### -Protokoll
Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- TCP
- UDP
- Platzhalterzeichen (*) zur Übereinstimmung mit beiden

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
Gibt das Präfix einer Quelladresse an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- ein CIDR
- Ein Quell-IP-Bereich
- Ein Platzhalterzeichen (*), das einer beliebigen IP-Adresse entspricht.
Sie können auch Tags wie "VirtualNetwork", "AzureLoadBalancer" und "Internet" verwenden.

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
Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist. Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.

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
Die Anwendungs Sicherheitsgruppe, die als Quelle für die Regel definiert ist. Sie kann nicht mit dem "SourceAddressPrefix"-Parameter verwendet werden.

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
Gibt einen Quell Port oder-Bereich an.
Dieser Wert wird als ganze Zahl ausgedrückt, als ein Bereich zwischen 0 und 65535, oder als Platzhalterzeichen (*), um einem beliebigen Quell-Port zu entsprechen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Notizen

## Verwandte Links

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Neu – AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Satz-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


