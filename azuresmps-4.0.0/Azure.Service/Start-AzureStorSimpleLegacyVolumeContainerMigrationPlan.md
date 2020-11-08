---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005979"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## Synopsis
Startet die Erstellung eines Migrationsplans.

## Syntax

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan-** Cmdlet wird die Erstellung eines Migrationsplans gestartet.
Die Erstellung eines Migrationsplans ist asynchron.
Wenn Sie den Status des Migrationsplans anzeigen möchten, verwenden Sie das Cmdlet **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .

## Beispiele

### Beispiel 1: Starten eines Migrationsplans
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Mit diesem Befehl wird die Erstellung eines Migrationsplans für den Legacy Container mit dem Namen OneSDKAzureCloud gestartet.
Der Befehl gibt eine Meldung zum Status des Plans zurück und verwendet das Cmdlet " **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** " für aktuelle Informationen.

### Beispiel 2: Starten des Migrationsplans für alle Volumen Container
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

Mit diesem Befehl wird die Erstellung des Migrationsplans für alle Legacy-Volumen Container in der importierten Konfigurationsdatei gestartet.

## Parameter

### – Alle
Gibt an, dass dieses Cmdlet Migrationszeit Schätzungen für alle Volumen Container in der importierten Konfigurationsdatei startet.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
Gibt die eindeutige ID der Konfiguration der Legacy-Appliance an.

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

### -LegacyContainerNames
Gibt ein Array von Volumen Containernamen an, für die ein Migrationsplan erstellt werden soll.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
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

### Zeichenfolge
Dieses Cmdlet gibt den Status des Migrationsplan Auftrags zurück, wenn er erfolgreich in der Appliance gestartet wurde.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


