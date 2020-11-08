---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006363"
---
# Remove-AzureDisk

## Synopsis
Entfernt einen Datenträger aus dem Azure Disk Repository.

## Syntax

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureDisk** entfernt einen Datenträger aus dem Azure Disk Repository im aktuellen Abonnement.
Standardmäßig wird mit diesem Cmdlet keine VHD-Datei (Virtual Hard Disk) aus dem BLOB-Speicher gelöscht.
Um die VHD zu löschen, geben Sie den Parameter *DeleteVHD* an.

## Beispiele

### Beispiel 1: Entfernen eines Datenträgers
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

Dieser Befehl entfernt den Datenträger mit dem Namen ContosoDataDisk Disk aus dem Datenträger-Repository.
Der Befehl löscht die VHD nicht.

### Beispiel 2: entfernen und Löschen eines Datenträgers
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

Dieser Befehl entfernt den Datenträger mit dem Namen ContosoDataDisk Disk aus dem Datenträger-Repository.
Mit diesem Befehl wird der DeleteVHD-Parameter angegeben.
Daher löscht der Befehl die VHD aus dem Azure-Speicher.

## Parameter

### -DeleteVHD
Gibt an, dass dieses Cmdlet die VHD aus dem BLOB-Speicher entfernt.

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

### -Daten Trägername
Gibt den Namen des Daten Datenträgers im Datenträger-Repository an, den dieses Cmdlet entfernt.

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

[Get-AzureDisk](./Get-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


