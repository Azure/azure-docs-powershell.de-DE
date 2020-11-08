---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DBC4A0B8-A34A-47AC-930B-EFE23A95A216
online version: ''
schema: 2.0.0
ms.openlocfilehash: 178349299767eefb1d89c31a0199f53373bd2ae2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006201"
---
# New-AzureRemoteAppTemplateImage

## Synopsis
Uploads oder Importieren eines Azure RemoteApp-Vorlagenbilds

## Syntax

### UploadLocalVhd (Standard)
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> [-Path] <String> [-Resume]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVmUpload
```
New-AzureRemoteAppTemplateImage [-ImageName] <String> [-Location] <String> -AzureVmImageName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzureRemoteAppTemplateImage** wird ein Azure RemoteApp-Vorlagenbild hochgeladen oder importiert.

## Beispiele

### Beispiel 1: Hochladen einer VHD-Datei zum Erstellen eines Vorlagenbilds
```
PS C:\> New-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -Location "North Europe" -Path "C:\RemoteAppImages\ContosoApps.vhd"
```

Mit diesem Befehl wird C:\RemoteAppImages\ContosoApps.VHD zum Erstellen eines Vorlagenbilds mit dem Namen ContosoApps im Nordeuropa-Rechenzentrum hochgeladen.

## Parameter

### -AzureVmImageName
Gibt den Namen eines Azure-virtuellen Computers an, der als Vorlagenbild verwendet werden soll.

```yaml
Type: String
Parameter Sets: AzureVmUpload
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bildname
Gibt den Namen eines Azure RemoteApp-Vorlagenbilds an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Standort
Gibt den Azure-Bereich des Vorlagenbilds an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Dateipfad des Vorlagenbilds an.

```yaml
Type: String
Parameter Sets: UploadLocalVhd
Aliases: 

Required: True
Position: 3
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

### -Resume
Gibt an, dass dieses Cmdlet fortgesetzt wird, wenn der Upload eines Vorlagenbilds unterbrochen wird.

```yaml
Type: SwitchParameter
Parameter Sets: UploadLocalVhd
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

[Get-AzureRemoteAppTemplateImage](./Get-AzureRemoteAppTemplateImage.md)

[Remove-AzureRemoteAppTemplateImage](./Remove-AzureRemoteAppTemplateImage.md)

[Umbenennen – AzureRemoteAppTemplateImage](./Rename-AzureRemoteAppTemplateImage.md)


