---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005857"
---
# Get-AzureDataDisk

## Synopsis
Ruft Azure-Daten Datenträger ab.

## Syntax

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureDataDisk** " Ruft ein Objekt ab, das die Datenlaufwerke auf einem Azure Virtual Machine darstellt.
Wenn Sie ein bestimmtes Daten Datenträgerobjekt abrufen möchten, geben Sie die logische Einheitsnummer (LUN) des Datenträgers an.

## Beispiele

### Beispiel 1: Abrufen aller Datenlaufwerke für einen virtuellen Computer
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft alle Datenlaufwerke für diesen virtuellen Computer ab.

### Beispiel 2: Abrufen einer bestimmten Datendiskette für ein vituralvirtual-machinevirtual
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst mit dem Namen ContosoService.
Der Befehl übergibt den virtuellen Computer an das aktuelle Cmdlet.
Das aktuelle Cmdlet ruft den Datenträger mit der LUN 2 ab.

## Parameter

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
Parameter Sets: (All)
Aliases: 

Required: False
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
Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet Datenlaufwerke erhält.
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

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Satz-AzureDataDisk](./Set-AzureDataDisk.md)


