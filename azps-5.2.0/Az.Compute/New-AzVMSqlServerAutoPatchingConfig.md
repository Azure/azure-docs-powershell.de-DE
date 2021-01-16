---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293698"
---
# New-AzVMSqlServerAutoPatchingConfig

## SYNOPSIS
Erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.

## SYNTAX

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzVMSqlServerAutoPatchingConfig"** erstellt ein Konfigurationsobjekt für das automatische Patchen auf einem virtuellen Computer.

## BEISPIELE

### Beispiel 1: Erstellen eines Konfigurationsobjekts zum Konfigurieren des automatischen Patchens
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

Mit diesem Befehl wird ein Konfigurationsobjekt zum Patchen erstellt.
Der Befehl gibt den Wochentag an und definiert das Wartungsfenster.
Diese Konfiguration ermöglicht Patching, das diese Werte verwendet.
Der Befehl speichert das Ergebnis in der $AutoBackupConfig Variable.
Sie können dieses Konfigurationselement für andere Cmdlets angeben, z. B. Set-AzVMSqlServerExtension Cmdlet.

## PARAMETERS

### -DayOfWeek
Gibt den Wochentag an, an dem Updates installiert werden sollen.
Die zulässigen Werte für diesen Parameter sind:
- Sonntag
- Montag
- Dienstag
- Mittwoch
- Donnerstag
- Freitag
- Samstag
- Jeden Tag

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Gibt an, dass automatisches Patchen für den virtuellen Computer aktiviert ist.
Wenn Sie automatisches Patchen aktivieren, versetzt das Cmdlet Windows Update in den interaktiven Modus.
Wenn Sie das automatische Patchen deaktivieren, ändern sich die Windows Update-Einstellungen nicht.

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

### -MaintenanceWindowDuration
Gibt die Dauer (in Minuten) des Wartungsfensters an.
Automatisches Patchen verhindert das Ausführen einer Aktion, die sich auf die Verfügbarkeit eines virtuellen Computers außerhalb dieses Fensters auswirken kann.
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

### -MaintenanceWindowStartingHour
Gibt die Stunde des Tages an, zu der das Wartungsfenster gestartet wird.
Dieses Mal wird festgelegt, wann updates mit der Installation beginnen.

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
Gibt an, ob wichtige Updates einbezogen werden sollen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Compute.AutoPatchingSettings

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Set-AzVMSqlServerExtension](./Set-AzVMSqlServerExtension.md)


