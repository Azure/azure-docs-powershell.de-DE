---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006821"
---
# Get-AzsNetworkAdminOverview

## Synopsis
Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters.

## Syntax

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## Beschreibung
Verschaffen Sie sich einen Überblick über den Zustand des Netzwerkressourcen Anbieters. Einzelne Eigenschaften bieten detaillierte Zählungen der Ressourcennutzung und des Status nach Komponenten.

## Beispiele

### Beispiel 1
```
Get-AzsNetworkAdminOverview
```

Netzwerkadministrator-Übersicht abrufen.

### Beispiel 2
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Abrufen der Nutzung öffentlicher IP-Adressen.

## Parameter

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Notizen

## Verwandte Links
