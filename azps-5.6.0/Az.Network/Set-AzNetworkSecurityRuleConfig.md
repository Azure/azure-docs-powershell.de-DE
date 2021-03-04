---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944813"
---
# Set-AzNetworkSecurityRuleConfig

## SYNOPSIS
Aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet Set-AzNetworkSecurityRuleConfig** aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.

## BEISPIELE

### Beispiel 1: Ändern der Zugriffskonfiguration in einer Netzwerksicherheitsregel
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

Der erste Befehl ruft die Netzwerksicherheitsgruppe NSG-FrontEnd ab und speichert sie dann in der variablen $nsg.
Der zweite Befehl verwendet den Pipelineoperator, um die Sicherheitsgruppe in $nsg an Get-AzNetworkSecurityRuleConfig zu übergeben, die die Sicherheitsregelkonfiguration namens rdp-rule erhält.
Mit dem dritten Befehl wird die Zugriffskonfiguration von rdp-rule in "Verweigern" geändert. Dadurch wird die Regel jedoch überschrieben und nur die Parameter festgelegt, die an die Funktion Set-AzNetworkSecurityRuleConfig werden.   HINWEIS: Es gibt keine Möglichkeit, ein einzelnes Attribut zu ändern

### Beispiel 2

Aktualisiert eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe. (automatisch generiert)

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## PARAMETER

### -Access
Gibt an, ob Netzwerkdatenverkehr zulässig oder verweigert ist. Die zulässigen Werte für diesen Parameter sind: Zulassen und Verweigern.

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
Gibt ein Zieladressenpräfix an.
Die zulässigen Werte für diesen Parameter sind:
- Eine klassenloses domänenübergreifendes Routing (CIDR) 
- Ziel-IP-Adressbereich 
- Platzhalterzeichen (*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.

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
Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde. Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.

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
Die Anwendungssicherheitsgruppe, die als Ziel für die Regel festgelegt wurde. Sie kann nicht mit dem Parameter "DestinationAddressPrefix" verwendet werden.

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
Gibt einen Zielport oder -bereich an.
Die zulässigen Werte für diesen Parameter sind:
- Eine ganze Zahl 
- Ein Ganzzahlbereich zwischen 0 und 65535
- Ein Platzhalterzeichen (*) zur Übereinstimmung mit einem beliebigen Port

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
Die zulässigen Werte für diesen Parameter sind: Ein- und Ausgehend.

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
Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet festgelegt wird.

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
Gibt das **NetworkSecurityGroup-Objekt** an, das die netzwerksicherheitsregelkonfiguration enthält, die festgelegt werden soll.

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
Die zulässigen Werte für diesen Parameter sind:Eine ganze Zahl zwischen 100 und 4096.
Die Prioritätsnummer muss für jede Regel in der Auflistung eindeutig sein.
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
Gibt das Netzwerkprotokoll an, für das eine Regelkonfiguration gilt.
Die zulässigen Werte für diesen Parameter sind: --Tcp
- Udp
- Ein Platzhalterzeichen (*) für beides

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
- Platzhalterzeichen (*) zur Übereinstimmung mit einer beliebigen IP-Adresse Sie können auch Tags wie VirtualNetwork, AzureLoadBalancer und Internet verwenden.

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
Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde. Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.

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
Die Anwendungssicherheitsgruppe, die als Quelle für die Regel festgelegt wurde. Sie kann nicht mit dem Parameter "SourceAddressPrefix" verwendet werden.

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
- Ein Ganzzahlbereich zwischen 0 und 65535
- Ein Platzhalterzeichen (*) zur Übereinstimmung mit einem beliebigen Port

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## NOTIZEN

## VERWANDTE LINKS

[Add-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Get-AzNetworkSecurityRuleConfig](./Get-AzNetworkSecurityRuleConfig.md)

[New-AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)


