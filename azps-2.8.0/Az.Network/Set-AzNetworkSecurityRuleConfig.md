---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821184"
---
# Set-AzNetworkSecurityRuleConfig

## Synopsis
Aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.

## Syntax

### SetByResource (Standard)
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzNetworkSecurityRuleConfig** " aktualisiert eine Netzwerk Sicherheitsregel-Konfiguration für eine Netzwerksicherheitsgruppe.

## Beispiele

### Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerk Sicherheitsregel
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Der erste Befehl ruft die Netzwerksicherheitsgruppe mit dem Namen NSG-Frontend ab und speichert Sie dann in der Variablen $NSG.
Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $NSG an Get-AzNetworkSecurityRuleConfig zu übergeben, wodurch die Sicherheitsregel Konfiguration mit dem Namen RDP-Rule abgerufen wird.
Der dritte Befehl ändert die Zugriffskonfiguration der RDP-Regel in Deny.

## Parameter

### -Access
Gibt an, ob der Netzwerkdatenverkehr zugelassen oder verweigert wird. Zulässige Werte für diesen Parameter sind: allow und Deny.

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
Gibt eine Beschreibung für eine Regelkonfiguration an.
Die maximale Größe beträgt 140 Zeichen.

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
Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die dieses Cmdlet festlegt.

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
Gibt das **NetworkSecurityGroup** -Objekt an, das die festzulegende Netzwerk Sicherheitsregel Konfiguration enthält.

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
Die akzeptablen Werte für diesen Parameter sind:--TCP
- UDP
- Ein Platzhalterzeichen (*), das mit beiden übereinstimmt

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
- Ein Platzhalterzeichen (*), das einer beliebigen IP-Adresse entspricht Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.

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
Gibt den Quell Port oder-Bereich an.
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup

## Notizen

## Verwandte Links

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Neu – AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


