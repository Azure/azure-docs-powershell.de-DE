---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006712"
---
# Get-AzureWebsiteLog

## Synopsis
Ruft Protokolle für die angegebene Website ab.

## Syntax

### Schwanz
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.
Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .

Ruft das Protokoll für die angegebene Website ab.

## Beispiele

### Beispiel 1: Starten des Streaming von Protokollen
```
PS C:\> Get-AzureWebsiteLog -Tail
```

In diesem Beispiel wird das Protokoll Streaming für alle Anwendungsprotokolle gestartet.

### Beispiel 2: Starten des Streaming von Protokollen für HTTP-Protokolle
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

In diesem Beispiel wird das Protokoll Streaming für HTTP-Protokolle gestartet.

### Beispiel 3: Starten des Protokoll-Streams für Fehlerprotokolle
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

In diesem Beispiel wird das Streaming von Protokollen gestartet und nur Fehlerprotokolle angezeigt.

### Beispiel 4: Anzeigen von Anzeige Protokollen
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

In diesem Beispiel werden alle verfügbaren Protokollpfade auf der Website aufgelistet.

## Parameter

### -ListPath
Gibt an, ob die Protokollpfade aufgelistet werden sollen.

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nachricht
Gibt eine Zeichenfolge an, die zum Filtern der Protokollnachricht verwendet wird.
Es werden nur Protokolle abgerufen, die diese Zeichenfolge enthalten.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der Website.

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

### -Path
Der Pfad, aus dem das Protokoll abgerufen werden soll.
Standardmäßig handelt es sich um root, was bedeutet, dass alle Pfade eingeschlossen werden.

```yaml
Type: String
Parameter Sets: Tail
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

### -Slot
Gibt den Namen des Steckplatzes an.

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

### -Tail
Gibt an, ob die Protokolle gestreamt werden sollen.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Neu – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Anfang-AzureWebsite](./Start-AzureWebsite.md)


