---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006034"
---
# Set-AzureOSDisk

## Synopsis
Ändert den Host Cachemodus eines Azure Virtual Machine.

## Syntax

### NORESIZE
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Größe
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureOSDisk** " ändert den Host Cachemodus des Betriebssystemdatenträgers einer virtuellen Azure-Maschine.
Die unterstützten Host Cache Modi sind ReadOnly und ReadWrite.
Wenn Sie dieses Cmdlet auf einem virtuellen Computer ausführen, der ausgeführt wird, wird dieser virtuelle Computer neu gestartet.

## Beispiele

### Beispiel 1: Einrichten des Host Cachemodus für ReadOnly mithilfe der Pipeline
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine02 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.
Der Befehl übergibt den virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet legt den Host Cachemodus des Betriebssystemdatenträgers dieses virtuellen Computers auf ReadOnly fest.

### Beispiel 2: Einrichten des Host Cachemodus auf ReadWrite
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine02 im Dienst mit dem Namen ContosoService ab und speichert ihn dann in der Variablen.

Mit dem zweiten Befehl wird der Host Cachemodus des Betriebssystemdatenträgers dieses virtuellen Computers auf ReadWrite festgelegt.

## Parameter

### -HostCaching
Gibt das Host Cache Attribut für den Betriebssystemdatenträger an.
Gültige Werte sind: 

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
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
Gibt eine neue Größe (in GB) für den Betriebssystemdatenträger an.
Die Größe muss größer als die aktuelle Größe sein.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, für den dieses Cmdlet den Datenträger des Betriebssystems ändert.
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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Satz-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


