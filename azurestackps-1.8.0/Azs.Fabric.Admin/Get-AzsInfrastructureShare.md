---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827584"
---
# Get-AzsInfrastructureShare

## Synopsis
Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.

## Syntax

### Liste (Standard)
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### Erhalten
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## Beschreibung
Gibt eine Liste aller Fabric-Dateifreigaben an einer bestimmten Position zurück.

## Beispiele

### Beispiel 1
```
Get-AzsInfrastructureShare
```

Gibt eine Liste aller Dateifreigaben zurück.

### Beispiel 2
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

Gibt eine Dateifreigabe basierend auf dem Namen zurück.

## Parameter

### -Name
Name der Fabric-Dateifreigabe.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Filter
OData-Filterparameter

```yaml
Type: String
Parameter Sets: List
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

## Ausgaben

### Microsoft. AzureStack. Management. Fabric. admin. Models. FileShare

## Notizen

## Verwandte Links
