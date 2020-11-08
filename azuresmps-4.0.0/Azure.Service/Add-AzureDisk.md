---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006599"
---
# Add-AzureDisk

## Synopsis
Fügt dem Azure Disk Repository einen Datenträger hinzu.

## Syntax

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureDisk** fügt dem Azure Disk Repository im aktuellen Abonnement einen Datenträger hinzu.
Mit diesem Cmdlet kann ein Systemdatenträger oder ein Daten Datenträger hinzugefügt werden.
Geben Sie zum Hinzufügen eines Systemdatenträgers einen Betriebssystemtyp mithilfe des Parameters " *OS* " an.

## Beispiele

### Beispiel 1: Hinzufügen einer Startdiskette, die das Windows-Betriebssystem verwendet
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

Mit diesem Befehl wird dem Datenträger-Repository ein Systemdatenträger hinzugefügt.
Auf dem Systemdatenträger wird das Windows-Betriebssystem verwendet.

### Beispiel 2: Hinzufügen eines Daten Datenträgers
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

Mit diesem Befehl wird ein Daten Datenträger hinzugefügt.

### Beispiel 3: Hinzufügen eines Linux-Systemdatenträgers
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

Mit diesem Befehl wird ein Linux-Systemdatenträger hinzugefügt.

## Parameter

### -Daten Trägername
Gibt den Namen des Datenträgers an, der vom Cmdlet hinzugefügt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Label
Gibt eine Datenträgerbeschriftung für den Datenträger an, den dieses Cmdlet hinzufügt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MediaLocation
Gibt den physikalischen Speicherort des Datenträgers im Azure-Speicher an.
Dieser Wert bezieht sich auf eine BLOB-Seite im aktuellen Abonnement-und Speicherkonto.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OS
Gibt den Typ des Betriebssystems für einen Systemdatenträger an.
Gültige Werte sind: 

- Windows 
- Linux 

Wenn Sie diesen Parameter nicht angeben, fügt das Cmdlet den Datenträger als Datenträger hinzu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## Ausgaben

### Daten trägercontext

## Notizen

## Verwandte Links

[Get-AzureDisk](./Get-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


