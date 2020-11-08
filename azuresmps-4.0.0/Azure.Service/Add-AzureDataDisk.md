---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005941"
---
# Add-AzureDataDisk

## Synopsis
Fügt einen Daten Datenträger zu einem virtuellen Computer hinzu.

## Syntax

### CreateNew (Standard)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Importieren
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureDataDisk** wird ein neuer oder vorhandener Daten Datenträger zu einem Azure Virtual Machine-Objekt hinzugefügt.
Verwenden Sie den *CreateNew* -Parameter, um einen neuen Daten Datenträger mit einer angegebenen Größe und Beschriftung zu erstellen.
Verwenden Sie den Parameter *importieren* , um einen vorhandenen Datenträger aus dem Image-Repository anzufügen.
Verwenden Sie den *ImportFrom* -Parameter, um einen vorhandenen Datenträger von einem BLOB in einem Speicherkonto anzufügen.
Sie können den Host-Cache-Modus für den angefügten Datenträger angeben.

## Beispiele

### Beispiel 1: Importieren einer Datendiskette aus dem Repository
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen "VirtualMachine07" im ContosoService-clouddienst ab, indem Sie das Cmdlet " **Get-AzureVM** " verwenden.
Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieser Befehl fügt eine vorhandene Datendiskette aus dem Repository an den virtuellen Computer an.
Der Datenträger hat eine LUN von 0.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.

### Beispiel 2: Hinzufügen eines neuen Daten Datenträgers
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen VirtualMachine08 ab.
Der Befehl übergibt ihn an das aktuelle Cmdlet.
Dieser Befehl fügt einen neuen Daten Datenträger mit dem Namen "MyNewDisk. VHD" an.
Das Cmdlet erstellt den Datenträger im VHD-Container im Standardspeicher Konto des aktuellen Abonnements.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.

### Beispiel 3: Hinzufügen eines Daten Datenträgers von einem angegebenen Speicherort
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Dieser Befehl ruft ein Objekt eines virtuellen Computers für den virtuellen Computer mit dem Namen Database ab.
Der Befehl übergibt ihn an das aktuelle Cmdlet.
Mit diesem Befehl wird eine vorhandene Datendiskette mit dem Namen Disk14. VHD vom angegebenen Speicherort angefügt.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.

## Parameter

### -CreateNew
Gibt an, dass dieses Cmdlet einen Daten Datenträger erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Gibt die Datenträgerbeschriftung für einen neuen Datenträger an.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Daten Trägername
Gibt den Namen eines Daten Datenträgers im Datenträger-Repository an.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Gibt die Größe des logischen Datenträgers in Gigabyte für einen neuen Daten Datenträger an.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Gibt die Einstellungen für die Zwischenspeicherung auf Hostebene des Datenträgers an.
Gültige Werte sind: 

- Keine 
- ReadOnly 
- ReadWrite

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

### -Import
Gibt an, dass dieses Cmdlet einen vorhandenen Daten Datenträger aus dem Image-Repository importiert.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Gibt an, dass dieses Cmdlet einen vorhandenen Daten Datenträger aus einem BLOB in einem Speicherkonto importiert.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
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

### -LUN
Gibt die logische Einheitsnummer (LUN) für das Datenlaufwerk auf dem virtuellen Computer an.
Gültige Werte sind: 0 bis 15.
Jeder Datenträger muss über eine eindeutige LUN verfügen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Gibt den Speicherort des BLOB in einem Azure Storage-Konto an, in dem dieses Cmdlet den Daten Datenträger speichert.
Wenn Sie keinen Speicherort angeben, speichert das Cmdlet den Daten Datenträger im VHD-Container im Standardspeicher Konto für das aktuelle Abonnement.
Wenn kein VHD-Container vorhanden ist, erstellt das Cmdlet einen VHD-Container.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
Gibt das Objekt des virtuellen Computers an, an das dieses Cmdlet einen Daten Datenträger anfügt.
Verwenden Sie das Cmdlet **Get-AzureVM** , um ein Objekt eines virtuellen Computers zu erhalten.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Satz-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


