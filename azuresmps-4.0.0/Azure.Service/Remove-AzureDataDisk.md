---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006372"
---
# Remove-AzureDataDisk

## Synopsis
Entfernt einen Datenträger von einem Azure Virtual Machine.

## Syntax

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureDataDisk** entfernt einen Daten Datenträger von einem virtuellen Azure-Computer.
Standardmäßig entfernt dieses Cmdlet das Datenträger-BLOB nicht aus dem Speicherkonto.

## Beispiele

### Beispiel 1: Entfernen eines Daten Datenträgers
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt den Daten Datenträger mit der LUN 0.

### Beispiel 2: Entfernen eines Daten Datenträgers und der virtuellen Festplattendatei
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst mit dem Namen ContosoService.
Der Befehl übergibt den virtuellen Computer an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt den Daten Datenträger mit der LUN 0.
Der Befehl enthält den *DeleteVHD* -Parameter.
Daher wird auch die zugrunde liegende virtuelle Festplatte gelöscht.
Der Befehl aktualisiert den virtuellen Computer, um Ihre Änderungen mit dem Cmdlet **Update-AzureVM** wiederzugeben.

## Parameter

### -DeleteVHD
Gibt an, dass das Cmdlet den Datenträger und die virtuelle Festplatte (VHD) aus dem BLOB-Speicher entfernt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Satz-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


