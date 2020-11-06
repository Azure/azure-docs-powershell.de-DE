---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474998"
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

### --------------------------Beispiel 1--------------------------
```
Get-AzsNetworkAdminOverview
```

Netzwerkadministrator-Übersicht abrufen.

### --------------------------Beispiel 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

Abrufen der Nutzung öffentlicher IP-Adressen.

## Parameter

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview

## Notizen

## Verwandte Links

