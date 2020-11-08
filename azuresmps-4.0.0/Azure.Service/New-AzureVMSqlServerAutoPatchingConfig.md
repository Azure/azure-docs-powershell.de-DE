---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006397"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Synopsis
Erstellt ein Konfigurationsobjekt für das automatische Patchen virtueller Maschinen.

## Syntax

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureVMSqlServerAutoPatchingConfig** erstellt ein Configuration-Objekt für das automatische Patchen virtueller Maschinen.

## Beispiele

### Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

Mit diesem Befehl wird ein Configuration-Objekt erstellt, mit dem das automatische Patchen mithilfe von AzureVMSqlServerExtension konfiguriert werden kann.

## Parameter

### -DayOfWeek
Gibt den Wochentag an, zu dem Updates installiert werden sollen.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Sonntag
- Montag
- Dienstag
- Mittwoch
- Donnerstag
- Freitag
- Samstag
- Alltags

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.
Wenn Sie das automatische Patchen aktivieren, wird Windows Update vom Cmdlet in den interaktiven Modus versetzt.
Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.

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

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Gibt die Dauer des Wartungsfensters an.
Durch automatisches Patchen wird eine Aktion verhindert, die sich auf die Verfügbarkeit eines virtuellen Computers außerhalb dieses Fensters auswirken kann.
Es sind nur 30 Minuten Inkremente zulässig.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowStartingHour
Gibt die Stunde des Tages an, an dem das Wartungsfenster gestartet wird.
Dieses Mal wird definiert, wann Updates mit der Installation beginnen und auf die Stunde gerundet werden.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PatchCategory
Gibt an, ob wichtige Updates enthalten sein sollen.

```yaml
Type: String
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

### AutoPatchingSettings
Dieses Cmdlet gibt das Objekt zurück, das Einstellungen für automatisiertes Patchen enthält.

## Notizen

## Verwandte Links

[Satz-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)

[Remove-AzureVMSqlServerExtension](./Remove-AzureVMSqlServerExtension.md)

[Satz-AzureVMSqlServerExtension](./Set-AzureVMSqlServerExtension.md)


