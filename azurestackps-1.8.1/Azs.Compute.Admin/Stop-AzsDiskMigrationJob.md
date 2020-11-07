---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee1a9ae5a4d5ef7545ee9a3e071fcc06475034f4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828299"
---
# Stop-AzsDiskMigrationJob

## Synopsis
Abbrechen eines verwalteten Datenträger Migrationsauftrags

## Syntax

```
Stop-AzsDiskMigrationJob [[-Location] <String>] [[-Name] <String>] [<CommonParameters>]
```

## Beschreibung
Abbrechen eines Datenträger Migrationsauftrags

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Stop-AzsDiskMigrationJob -Location local -MigrationId $migration.MigrationId
```

Abbrechen eines verwalteten Datenträger Migrationsauftrags

## Parameter

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der GUID-Name des Migrationsauftrags.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob

## Notizen

## Verwandte Links

