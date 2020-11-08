---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005924"
---
# Add-AzureVhd

## Synopsis
Lädt eine VHD-Datei von einem lokalen Computer zu einem BLOB in einem Cloud-Speicherkonto in Azure hoch.

## Syntax

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Add-AzureVhd** " werden virtuelle Festplatten (VHD)-Bilder in einem BLOB-Speicherkonto als feste VHD-Bilder hochgeladen.
Er verfügt über Parameter zum Konfigurieren des Upload-Vorgangs, beispielsweise zum Angeben der Anzahl der Uploader-Threads, die verwendet werden, oder zum Überschreiben eines BLOB, das bereits im angegebenen Ziel-URI vorhanden ist.
Für lokale VHD-Bilder wird ein Patch-Szenario ebenfalls unterstützt, damit unterschiedlich festgestellte Datenträger Bilder hochgeladen werden können, ohne dass die bereits hochgeladenen Basisbilder hochgeladen werden müssen. SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.

## Beispiele

### Beispiel 1: Hinzufügen einer VHD-Datei
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.

### Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.

### Beispiel 3: Hinzufügen einer VHD-Datei und angeben der Anzahl der Threads
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt, und es wird die Anzahl der Threads angegeben, die zum Hochladen der Datei verwendet werden sollen.

### Beispiel 4: Hinzufügen einer VHD-Datei und angeben des SAS-URIs
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt und der SAS-URI angegeben.

## Parameter

### -BaseImageUriToPatch
Gibt einen URI für ein Basis Bild-BLOB im Azure BLOB-Speicher an.
SAS in URI-Eingabe wird ebenfalls unterstützt.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ziel
Gibt einen URI für ein BLOB im Microsoft Azure BLOB-Speicher an.
SAS in URI-Eingabe wird unterstützt.
In Patch-Szenarien kann das Ziel jedoch kein SAS-URI sein.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
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

### -LocalFilePath
Art der Dateipfad der lokalen VHD-Datei.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Gibt die Anzahl der Threads an, die für den Upload verwendet werden sollen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Gibt an, dass dieses Cmdlet das vorhandene BLOB im angegebenen Ziel-URI löscht, wenn es vorhanden ist.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Save-AzureVhd](./Save-AzureVhd.md)


