---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166580"
---
# Add-AzVhd

## SYNOPSIS
Lädt eine virtuelle Festplatte von einem lokalen virtuellen Computer in ein BLOB in einem Cloudspeicherkonto in Azure hoch.

## SYNTAX

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Add-AzVhd-Cmdlet** lädt lokale virtuelle Festplatten im VHD-Dateiformat als feste virtuelle Festplatten in ein BLOB-Speicherkonto hoch.
Sie können die Anzahl der Uploaderthreads konfigurieren, die verwendet werden, oder ein vorhandenes BLOB im angegebenen Ziel-URI überschreiben.
Außerdem wird die Möglichkeit unterstützt, eine patchierte Version einer lokalen VHD-Datei hochzuladen.
Wenn bereits eine virtuelle Basisfestplatte hochgeladen wurde, können Sie andere Datenträger hochladen, die das Basisbild als übergeordnetes Bild verwenden.
Der SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.

## BEISPIELE

### Beispiel 1: Hinzufügen einer VHD-Datei
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.

### Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.
Der Befehl überschreibt eine vorhandene Datei.

### Beispiel 3: Hinzufügen einer VHD-Datei und Angeben der Anzahl von Threads
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.
Der Befehl gibt die Anzahl der Threads an, die zum Hochladen der Datei verwendet werden.

### Beispiel 4: Hinzufügen einer VHD-Datei und Angeben des SAS-URI
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

Dieser Befehl fügt einem Speicherkonto eine vhd-Datei hinzu und gibt den SAS-URI an.

## PARAMETERS

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.

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
Gibt den URI für ein Basisbild-BLOB im Azure Blob Storage an.
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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Destination
Gibt den URI eines BLOB im Blob Storage an.
Der Parameter unterstützt SAS-URI, obwohl das Ziel für Patchszenarien kein SAS-URI sein kann.

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
Gibt die Anzahl der Uploadthreads an, die beim Hochladen der VHD-Datei verwendet werden sollen.

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
Gibt an, dass dieses Cmdlet ein vorhandenes BLOB im angegebenen Ziel-URI überschreibt( sofern vorhanden).

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.URI

### System.IO.FileInfo

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.Compute.Models.VhdUploadContext

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Save-AzVhd](./Save-AzVhd.md)


