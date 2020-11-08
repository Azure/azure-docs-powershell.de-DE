---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006218"
---
# Stop-AzureStorSimpleJob

## Synopsis
Beendet einen StorSimple-Auftrag.

## Syntax

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzureStorSimpleJob** beendet einen laufenden StorSimple-Auftrag.
Sie können Aufträge angeben, indem Sie eine Instanz-ID oder einen Auftragsnamen angeben.

## Beispiele

### Beispiel 1: Beenden von Aufträgen für ein Gerät
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

Dieser Befehl ruft die Aufträge für das Gerät mit dem Namen Device07 mit dem Cmdlet **Get-AzureStorSimpleJob** ab.
Der Befehl übergibt die Aufträge mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet beendet alle Aufträge, die der Befehl an ihn übergibt.
Der Befehl gibt den Parameter *Force* an und fordert Sie daher nicht zur Bestätigung auf, bevor ein Auftrag beendet wird.

### Beispiel 2: Beenden eines bestimmten Auftrags
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

Dieser Befehl beendet den Auftrag mit der angegebenen Instanz-ID.

## Parameter

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -InstanceId
Gibt die ID des Geräte Auftrags an, der beendet werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt ein Azure-Profil an.

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

### Keine

## Ausgaben

### DeviceJobDetails
Dieses Cmdlet ruft Details des **DeviceJob** ab, das mit diesem Cmdlet beendet wird.

## Notizen

## Verwandte Links

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


