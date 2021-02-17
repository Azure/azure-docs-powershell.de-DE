---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156889"
---
# New-AzNetworkSecurityRuleConfig

## SYNOPSIS
Erstellt eine Konfiguration für Netzwerksicherheitsregel.

## SYNTAX

### SetByResource (Standard)
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzNetworkSecurityRuleConfig"** erstellt eine Konfiguration einer Azure-Netzwerksicherheitsregel für eine Netzwerksicherheitsgruppe.

## BEISPIELE

### Beispiel 1: Erstellen einer Netzwerksicherheitsregel zum Zulassen von RDP
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff über das Internet auf Port 3389 zu erlaubt.

### Beispiel 2: Erstellen einer Netzwerksicherheitsregel, die HTTP zulässt
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

Mit diesem Befehl wird eine Sicherheitsregel erstellt, die den Zugriff über das Internet auf Port 80 zu erlaubt.

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
Gibt eine Beschreibung der Konfiguration der Netzwerksicherheitsregel an, die erstellt werden soll.

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
Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet erstellt wird.

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
Gibt das Netzwerkprotokoll an, auf das eine neue Regelkonfiguration angewendet wird.
Die zulässigen Werte für diesen Parameter sind:
- Tcp
- Udp
- Platzhalterzeichen (*) für beides.

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
- Ein Platzhalterzeichen (*) zur Übereinstimmung mit einer beliebigen IP-Adresse.
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
Gibt den Quellport oder -bereich an.
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSSecurityRule

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


