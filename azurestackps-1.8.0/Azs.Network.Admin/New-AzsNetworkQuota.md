---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827776"
---
# New-AzsNetworkQuota

## Synopsis
Erstellen oder Aktualisieren eines Kontingents

## Syntax

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Erstellen oder Aktualisieren eines Kontingents

## Beispiele

### Beispiel 1
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

Erstellen Sie ein neues Netzwerk Kontingent mit allen Standardwerten.

### Beispiel 2
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

Erstellen Sie ein neues Netzwerk Kontingent mit nicht Standardwerten für Kontingent.

## Parameter

### -Name
Der Name der Netzwerk Kontingent Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxNicsPerSubscription
Die maximal zulässige Anzahl von NICs pro Abonnement.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPublicIpsPerSubscription
Die maximal zulässige öffentliche IP-Adresse pro Abonnement.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Die maximale Anzahl der pro Abonnement zulässigen virtuellen Netzwerk-Gateway-Verbindungen.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVnetsPerSubscription
Die maximal-Anzahl der pro Abonnement zulässigen virtuellen Netzwerke.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxVirtualNetworkGatewaysPerSubscription
Die maximale Anzahl von virtuellen Netzwerkgateways, die pro Abonnement zulässig sind.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSecurityGroupsPerSubscription
Die maximal zulässige Anzahl von Sicherheitsgruppen pro Abonnement.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxLoadBalancersPerSubscription
Die maximal zulässige Anzahl von Lasten ausgleichseinheiten pro Abonnement.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationPhase
Migrationsstatus wie "keine", "vorbereiten", "Commit" und "Abbrechen".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: Prepare
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Network. admin. Models. Quota

## Notizen

## Verwandte Links
