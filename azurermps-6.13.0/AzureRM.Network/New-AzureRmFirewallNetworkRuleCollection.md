---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498306"
---
# New-AzureRmFirewallNetworkRuleCollection

## Synopsis
Erstellt eine Azure Firewall-Netzwerksammlung von Netzwerkregeln.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmFirewallNetworkRuleCollection** erstellt eine Sammlung von Firewall-Netzwerkregeln.

## Beispiele

### 1: Erstellen einer Netzwerksammlung mit zwei Regeln
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

In diesem Beispiel wird eine Sammlung erstellt, die den gesamten Datenverkehr zulässt, der einer der beiden Regeln entspricht.
Die erste Regel gilt für den gesamten UDP-Datenverkehr.
Die zweite Regel ist der TCP-Datenverkehr von 10.0.0.0 zu 60.1.5.0:4040.
Wenn eine andere Netzwerkregel Sammlung mit höherer Priorität (geringere Zahl) vorhanden ist, die auch dem in $Rule 1 oder $Rule 2 angegebenen Datenverkehr entspricht, wird stattdessen die Aktion der Regelsammlung mit höherer Priorität wirksam. 

### 2: Hinzufügen einer Regel zu einer Regelsammlung
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit einer Regel erstellt, und anschließend wird der Regelsammlung mithilfe der AddRule-Methode für das Rule Collection-Objekt eine zweite Regel hinzugefügt. Jeder Regelname in einer bestimmten Regelsammlung muss einen eindeutigen Namen haben und die Groß-/Kleinschreibung wird nicht berücksichtigt.

### 3: Abrufen einer Regel aus einer Regelsammlung
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit einer Regel erstellt, und dann wird die Regel nach Namen abgerufen, und die GetRuleByName-Methode wird für das Rule Collection-Objekt aufgerufen. Der Regelname für Methoden-GetRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

### 4: Entfernen einer Regel aus einer Regelsammlung
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

In diesem Beispiel wird eine neue Netzwerkregel Sammlung mit zwei Regeln erstellt, und dann wird die erste Regel aus der Regelsammlung entfernt, indem die RemoveRuleByName-Methode für das Rule Collection-Objekt aufgerufen wird. Der Regelname für Methoden-RemoveRuleByName ist keine Unterscheidung nach Groß-/Kleinschreibung.

## Parameter

### -ActionType
Gibt die Aktion an, die für Datenverkehrs Übereinstimmungsbedingungen dieser Regel ausgeführt werden soll. Akzeptierte Aktionen sind "zulassen" oder "ablehnen".

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
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

### -Name
Gibt den Namen dieser Netzwerkregel Sammlung an. Der Name muss für alle Netzwerkregel Sammlung eindeutig sein.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priorität
Gibt die Priorität dieser Regelsammlung an. Priority ist eine Zahl zwischen 100 und 65000. Je kleiner die Zahl, desto höher die Priorität.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rule
Gibt die Liste der Regeln an, die unter dieser Sammlung gruppiert werden sollen.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRuleCollection

## Notizen

## Verwandte Links

[Neu – AzureRmFirewallNetworkRule](./New-AzureRmFirewallNetworkRule.md)

[Neu – AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)
