---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505162"
---
# New-AzureVMSqlServerAutoPatchingConfig

## Synopsis
Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureVMSqlServerAutoPatchingConfig** wird ein Configuration-Objekt für das automatische Patchen auf einem virtuellen Computer erstellt.

## Beispiele

### Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patches
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Mit diesem Befehl wird ein Configuration-Objekt für Patches erstellt.
Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.
Diese Konfiguration ermöglicht das Patchen, das diese Werte verwendet.
Der Befehl speichert das Ergebnis in der $AutoBackupConfig-Variablen.
Sie können dieses Konfigurationselement für andere Cmdlets angeben, beispielsweise das Cmdlet "Set-AzureRmVMSqlServerExtension".

## Parameter

### -Enable
Gibt an, dass automatisiertes Patchen für den virtuellen Computer aktiviert ist.
Wenn Sie das automatische Patchen aktivieren, setzt das Cmdlet Windows Update in den interaktiven Modus.
Wenn Sie das automatische Patchen deaktivieren, werden die Windows Update-Einstellungen nicht geändert.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Type: System.String
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
Dieses Mal wird definiert, wann Updates zu installieren beginnen.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceWindowDuration
Gibt die Dauer in Minuten des Wartungsfensters an.
Durch automatisches Patchen wird verhindert, dass eine Aktion ausgeführt wird, die sich auf die Verfügbarkeit einer virtuellen Maschine außerhalb dieses Fensters auswirkt.
Geben Sie ein Vielfaches von 30 Minuten an.

```yaml
Type: System.Int32
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
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Information
@ {Text =}

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@ {Text =}

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

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

[Neu – AzureVMSqlServerAutoBackupConfig](./New-AzureVMSqlServerAutoBackupConfig.md)

[Satz-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


