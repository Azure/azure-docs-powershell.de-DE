---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006272"
---
# Set-AzureDataDisk

## Synopsis
Ändert die Host Zwischenspeicherung eines vorhandenen Datenlaufwerks auf einem virtuellen Azure-Computer.

## Syntax

### NORESIZE
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Größe
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureDataDisk** " ändert die Cache Attribute eines vorhandenen Datenlaufwerks auf einem Azure Virtual Machine.
Geben Sie an, welcher Datenträger durch die logische einheitennummer (Logical Unit Number, LUN) aktualisiert werden soll.

## Beispiele

### Beispiel 1: Ändern der Host Zwischenspeicherung für einen Datenträger
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Dieser Befehl ruft die virtuellen Computer ab, die mit dem Cmdlet **Get-AzureVM** auf dem Dienst mit dem Namen ContosoService ausgeführt werden.
Der Befehl übergibt Sie mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet legt den Datenträger bei LUN 2 des virtuellen Computers mit dem Namen "VirtualMachine07" so fest, dass die ReadOnly-Host Zwischenspeicherung verwendet wird.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.

### Beispiel 2: Ändern der Host Zwischenspeicherung für alle Datenlaufwerke auf einem virtuellen Computer
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Dieser Befehl ruft ein Objekt für den virtuellen Computer mit dem Namen VirtualMachine07 im ContosoService-clouddienst ab.
Der Befehl übergibt ihn an das Cmdlet " **Get-AzureDataDisk** ", das die Datenlaufwerke für diesen virtuellen Computer abruft.
Das aktuelle Cmdlet legt dann den Host Zwischenspeichermodus für jeden Datenträger auf ReadWrite fest.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen wiederzugeben.

## Parameter

### -Daten Trägername
Gibt den Namen der Daten Datenträgerkonfiguration an, die von diesem Cmdlet geändert wird.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> Datenträgerzwischenspeicherung wird für Datenträger 4 tib und größer nicht unterstützt. Wenn mehrere Datenträger an Ihren Computer angeschlossen sind, unterstützt jeder Datenträger, der kleiner als 4 tib ist, die Zwischenspeicherung.
>
> Durch Ändern der Cacheeinstellung eines Azure-Datenträgers wird der Zieldatenträger abgetrennt und erneut angefügt. Wenn es sich um den Betriebssystemdatenträger handelt, wird der VM neu gestartet. Beenden Sie alle Anwendungen/Dienste, die von dieser Unterbrechung betroffen sein könnten, bevor Sie die Festplatten-Cache-Einstellung ändern. Wenn Sie diese Empfehlungen nicht befolgen, kann dies zu Datenbeschädigungen führen.

Gibt die Einstellungen für die Zwischenspeicherung auf Hostebene des Datenträgers an.
Gültige Werte sind:

- Keine
- ReadOnly
- ReadWrite

```yaml
Type: String
Parameter Sets: NoResize
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
Gibt die LUN für das Datenlaufwerk auf dem virtuellen Computer an.
Gültige Werte sind: 0 bis 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
Gibt die neue Größe (in GB) für den Daten Datenträger an.
Die neue Größe muss größer als die aktuelle Größe sein.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt das Objekt des virtuellen Computers an, das an den Daten Datenträger angefügt ist.
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


