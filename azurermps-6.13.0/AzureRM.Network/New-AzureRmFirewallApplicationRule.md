---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664822"
---
# New-AzureRmFirewallApplicationRule

## Synopsis
Erstellt eine Firewallregel für eine Firewall-Anwendung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### TargetFqdn (Standard)
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FqdnTag
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmFirewallApplicationRule** erstellt eine Anwendungsregel für Azure Firewall.

## Beispiele

### 1: Erstellen einer Regel zum Zulassen des gesamten HTTPS-Datenverkehrs von 10.0.0.0
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

In diesem Beispiel wird eine Regel erstellt, die den gesamten HTTPS-Datenverkehr auf Port 443 von 10.0.0.0 aus ermöglicht.

### 2: Erstellen einer Regel zum Zulassen von Windows für 10.0.0.0/24-Subnetz
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

In diesem Beispiel wird eine Regel erstellt, mit der Datenverkehr für Windows-Updates für 10.0.0.0/24-Domäne zugelassen wird.

## Parameter

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
Gibt eine optionale Beschreibung dieser Regel an.

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

### -FqdnTag
Gibt eine Liste von FQDN-Tags für diese Regel an. Die verfügbaren Tags können mit dem Cmdlet [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) abgerufen werden.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen dieser Anwendungsregel an. Der Name muss innerhalb einer Regelsammlung eindeutig sein.

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

### -Protokoll
Gibt den Typ des Datenverkehrs an, der nach dieser Regel gefiltert werden soll. Das Format lautet <protocol type> : <port> . Beispielsweise "http: 80" oder "https: 443".
Das Protokoll ist bei Verwendung von TargetFqdn obligatorisch, kann jedoch nicht mit FqdnTag verwendet werden. Die unterstützten Protokolle sind http und HTTPS.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAddress
Die Quelladressen der Regel

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

### -TargetFqdn
Gibt eine Liste der Domänennamen an, die nach dieser Regel gefiltert werden.
Das Asterik-Zeichen ' *' wird nur als erstes Zeichen eines FQDN in der Liste akzeptiert. Wenn Sie verwendet wird, entspricht die Asterik einer beliebigen Anzahl von Zeichen. (Beispiel: "* MSN.com" entspricht MSN.com und allen zugehörigen Unterdomänen)

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRule

## Notizen

## Verwandte Links

[Neu – AzureRmFirewallApplicationRuleCollection](./New-AzureRmFirewallApplicationRuleCollection.md)

[Neu – AzureRmFirewall](./New-AzureRmFirewall.md)

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md)
