---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850904"
---
# Save-AzureRmVhd

## Synopsis
Speichert heruntergeladene VHD-Bilder lokal.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ResourceGroupParameterSetName
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### StorageKeyParameterSetName
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das **Save-AzureRmVhd-** Cmdlet speichert VHD-Bilder aus einem BLOB, in dem Sie in einer Datei gespeichert sind.
Sie können die Anzahl der Downloader-Threads angeben, die der Prozess verwendet, und angeben, ob eine bereits vorhandene Datei ersetzt werden soll.

Mit diesem Cmdlet werden Inhalte so heruntergeladen, wie Sie sind.
Es wird keine VHD-Formatkonvertierung (Virtual Hard Disk) angewendet.

## Beispiele

### Beispiel 1: Herunterladen eines Bilds
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad C:\vhd\Win7Image.vhd.

### Beispiel 2: Herunterladen eines Bilds und Überschreiben der lokalen Datei
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.
Der Befehl enthält den Parameter *overwrite* .
Wenn C:\vhd\Win7Image.VHD bereits vorhanden ist, wird es durch diesen Befehl ersetzt.

### Beispiel 3: Herunterladen eines Bilds mithilfe einer angegebenen Anzahl von Threads
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.
Der Befehl gibt einen Wert von 32 für den *NumberOfThreads* -Parameter an.
Daher verwendet das Cmdlet 32-Threads für diese Aktion.

### Beispiel 4: Herunterladen eines Bilds und angeben des Speicher Schlüssels
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

Mit diesem Befehl wird eine VHD-Datei heruntergeladen und der Speicherschlüssel angegeben.

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Gibt den lokalen Dateipfad des gespeicherten Bilds an.

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfThreads
Gibt die Anzahl der Download-Threads an, die dieses Cmdlet während des Downloads verwendet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverWrite
Gibt an, dass dieses Cmdlet die durch *LocalFilePath* -Datei angegebene Datei ersetzt, falls vorhanden.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe des speicherkontos an.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceUri
Gibt den Uniform Resource Identifier (URI) des BLOB in an `Azure` .

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Gibt den Speicherschlüssel des BLOB-speicherkontos an.
Wenn Sie keinen Schlüssel angeben, versucht dieses Cmdlet, den Speicherschlüssel des Kontos in *SourceUri* aus Azure zu ermitteln.

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. VhdDownloadContext

## Notizen

## Verwandte Links

[Add-AzureRmVhd](./Add-AzureRMVhd.md)


