---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 106f6d9ed794ac2e4595f480616fa2c64663e554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505221"
---
# Add-AzureRmVhd

## Synopsis
Lädt eine virtuelle Festplatte von einem lokalen virtuellen Computer zu einem BLOB in einem Cloud-Speicherkonto in Azure hoch.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzureRmVhd** lädt lokale virtuelle Festplatten im VHD-Dateiformat in ein BLOB-Speicherkonto als feste virtuelle Festplatten hoch.
Sie können die Anzahl der Uploader-Threads konfigurieren, die verwendet werden sollen, oder ein vorhandenes BLOB im angegebenen Ziel-URI überschreiben.
Unterstützt wird auch die Möglichkeit, eine gepatchte Version einer lokalen VHD-Datei hochzuladen.
Wenn eine virtuelle Basisfestplatte bereits hochgeladen wurde, können Sie differenzierende Datenträger hochladen, die das basisimage als übergeordnetes Bild verwenden.
SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.

## Beispiele

### Beispiel 1: Hinzufügen einer VHD-Datei
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.

### Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.
Mit dem Befehl wird eine vorhandene Datei überschrieben.

### Beispiel 3: Hinzufügen einer VHD-Datei und angeben der Anzahl der Threads
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.
Der Befehl gibt die Anzahl der Threads an, mit denen die Datei hochgeladen werden soll.

### Beispiel 4: Hinzufügen einer VHD-Datei und angeben des SAS-URIs
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt und der SAS-URI angegeben.

## Parameter

### -BaseImageUriToPatch
Gibt den URI für ein Basis Bild-BLOB im Azure BLOB-Speicher an.
Eine SAS kann als Wert für diesen Parameter angegeben werden.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ziel
Gibt den URI eines BLOB im BLOB-Speicher an.
Der Parameter unterstützt SAS-URI, auch wenn es sich bei Patching-Szenarien nicht um einen SAS-URI handeln kann.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
Gibt den Pfad der lokalen VHD-Datei an.

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
Gibt die Anzahl der zu verwendenden Uploader-Threads an, wenn die VHD-Datei hochgeladen wird.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
Gibt an, dass mit diesem Cmdlet ein vorhandenes BLOB im angegebenen Ziel-URI überschrieben wird, sofern vorhanden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des virtuellen Computers an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

[Save-AzureRmVhd](./Save-AzureRmVhd.md)


