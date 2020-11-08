---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167277"
---
# Add-AzVhd

## Synopsis
Lädt eine virtuelle Festplatte von einem lokalen virtuellen Computer zu einem BLOB in einem Cloud-Speicherkonto in Azure hoch.

## Syntax

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Add-AzVhd** lädt lokale virtuelle Festplatten im VHD-Dateiformat in ein BLOB-Speicherkonto als feste virtuelle Festplatten hoch.
Sie können die Anzahl der Uploader-Threads konfigurieren, die verwendet werden sollen, oder ein vorhandenes BLOB im angegebenen Ziel-URI überschreiben.
Unterstützt wird auch die Möglichkeit, eine gepatchte Version einer lokalen VHD-Datei hochzuladen.
Wenn eine virtuelle Basisfestplatte bereits hochgeladen wurde, können Sie differenzierende Datenträger hochladen, die das basisimage als übergeordnetes Bild verwenden.
SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.

## Beispiele

### Beispiel 1: Hinzufügen einer VHD-Datei
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.

### Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.
Mit dem Befehl wird eine vorhandene Datei überschrieben.

### Beispiel 3: Hinzufügen einer VHD-Datei und angeben der Anzahl der Threads
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.
Der Befehl gibt die Anzahl der Threads an, mit denen die Datei hochgeladen werden soll.

### Beispiel 4: Hinzufügen einer VHD-Datei und angeben des SAS-URIs
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt und der SAS-URI angegeben.

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### System. Uri

### System. IO. FileInfo

### System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Management. Automation. Switchparameter

## Ausgaben

### Microsoft. Azure. Commands. Compute. Models. VhdUploadContext

## Notizen

## Verwandte Links

[Save-AzVhd](./Save-AzVhd.md)


