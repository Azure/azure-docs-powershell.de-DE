---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006560"
---
# Get-AzureDisk

## Synopsis
Ruft Informationen zu Datenträgern im Azure Disk Repository ab.

## Syntax

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureDisk** " Ruft Informationen zu den Datenträgern ab, die im Azure Disk Repository für das aktuelle Abonnement gespeichert sind.
Dieses Cmdlet gibt eine Liste der Informationen für alle Datenträger im Repository zurück.
Wenn Sie Informationen zu einem bestimmten Datenträger anzeigen möchten, geben Sie den Namen des Datenträgers an.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu einem Datenträger
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Dieser Befehl ruft Informationsdaten über den Datenträger mit dem Namen ContosoDataDisk aus dem Datenträger-Repository ab.

### Beispiel 2: Abrufen von Informationen zu allen Datenträgern
```
PS C:\> Get-AzureDisk
```

Dieser Befehl ruft Informationen zu allen Datenträgern im Datenträger-Repository ab.

### Beispiel 3: Abrufen von Informationen zu einem Datenträger
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Dieser Befehl ruft Daten für alle Datenträger im Datenträger-Repository ab, die derzeit nicht an einen virtuellen Computer angefügt sind.
Der Befehl ruft Informationen zu allen Datenträgern ab und übergibt die einzelnen Objekte an das Cmdlet **Where-Object** .
Dieses Cmdlet löscht alle Datenträger, die keinen Wert von $NULL für die **in** -Eigenschaft aufweisen.
Der Befehl formatiert die Liste mit dem Cmdlet **Format-Table** als Tabelle.

## Parameter

### -Daten Trägername
Gibt den Namen des Datenträgers im Datenträger-Repository an, über den dieses Cmdlet Informationen erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

## Notizen

## Verwandte Links

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


