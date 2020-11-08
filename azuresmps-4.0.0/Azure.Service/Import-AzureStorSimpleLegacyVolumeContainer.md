---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006464"
---
# Import-AzureStorSimpleLegacyVolumeContainer

## Synopsis
Startet die Migration von Volumen Containern.

## Syntax

### MigrateSpecificContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureStorSimpleLegacyVolumeContainer** " wird die Migration von Volumen Containern von einer Legacy-Appliance zur Ziel-Appliance gestartet.

## Beispiele

### Beispiel 1: Importieren eines Legacy-Volumen Containers
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

Mit diesem Befehl wird ein Legacy-Volumen Container für den benannten Container importiert.
Das Cmdlet startet den Import und gibt dann eine Nachricht zurück.

### Beispiel 2: Importieren aller Legacy-Volumen Container
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

Mit diesem Befehl werden alle Legacy-Volumen Container aus der importierten Konfigurationsdatei importiert.
Das Cmdlet startet den Import und gibt dann eine Nachricht zurück.

## Parameter

### – Alle
Gibt an, dass dieses Cmdlet alle Volumen Container in der importierten Konfigurationsdatei auf das Zielgerät importiert.

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

### -Force
Gibt an, dass dieses Cmdlet den Volumen Container auf einem anderen Gerät importiert, auch wenn der Volumen Container auf einem anderen Gerät importiert wurde.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
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
Gibt ein Array von Volumen Containernamen an, für die der Migrationsplan gilt.

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

### -SkipACRs
Gibt an, dass der Importvorgang die Zugriffssteuerungseinträge für die Migration überspringt.

```yaml
Type: SwitchParameter
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

## Ausgaben

### Zeichenfolge
Dieser Befehl gibt den Status des Container Auftrags für den Migrationsimport Volumen zurück, wenn er erfolgreich in der Appliance gestartet wurde.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Importieren-AzureStorSimpleLegacyApplianceConfig](./Import-AzureStorSimpleLegacyApplianceConfig.md)


