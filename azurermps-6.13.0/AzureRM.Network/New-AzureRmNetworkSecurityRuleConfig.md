---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 0950e09185783f0b352defafb7673a2f97461c74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505337"
---
# New-AzureRmNetworkSecurityRuleConfig

## Synopsis
Erstellt eine Netzwerk Sicherheitsregel-Konfiguration.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### SetByResource (Standard)
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResourceId
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmNetworkSecurityRuleConfig** erstellt eine Azure Network Security Rule-Konfiguration für eine Netzwerksicherheitsgruppe.

## Beispiele

### 1: Erstellen einer Netzwerk Sicherheitsregel zum Zulassen von RDP
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 3389 ermöglicht.

### 2: Erstellen einer Netzwerk Sicherheitsregel, die http zulässt
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff aus dem Internet auf Port 80 ermöglicht.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Beschreibung
Gibt eine Beschreibung der zu erstellenden Netzwerk Sicherheitsregel Konfiguration an.

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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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
Gibt den Namen der von diesem Cmdlet erstellten Konfiguration der Netzwerk Sicherheitsregel an.

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
Gibt das Netzwerkprotokoll an, für das eine neue Regelkonfiguration gilt.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- TCP
- UDP
- Platzhalterzeichen (*), um beide zu entsprechen.

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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
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
Type: System.Collections.Generic.List`1[System.String]
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
Type: System.Collections.Generic.List`1[System.String]
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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSSecurityRule

## Notizen

## Verwandte Links

[Add-AzureRmNetworkSecurityRuleConfig](./Add-AzureRmNetworkSecurityRuleConfig.md)

[Get-AzureRmNetworkSecurityRuleConfig](./Get-AzureRmNetworkSecurityRuleConfig.md)

[Remove-AzureRmNetworkSecurityRuleConfig](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[Satz-AzureRmNetworkSecurityRuleConfig](./Set-AzureRmNetworkSecurityRuleConfig.md)


