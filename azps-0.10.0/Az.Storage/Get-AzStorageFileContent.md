---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843080"
---
# Get-AzStorageFileContent

## Synopsis
Lädt den Inhalt einer Datei herunter.

## Syntax

### Freigabename (Standard)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Freigeben
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Verzeichnis
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Datei
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.
Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.

## Beispiele

### Beispiel 1: Herunterladen einer Datei aus einem Ordner
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.

### Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen

## Parameter

### -CheckMd5
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

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

### -ClientTimeoutPerRequest
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ziel
Gibt den Zielpfad an.
Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Verzeichnis
Gibt einen Ordner als **CloudFileDirectory** -Objekt an.
Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.
Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.
Sie können auch das Get-AzStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Datei
Gibt eine Datei als **clouddatei** -Objekt an.
Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.
Verwenden Sie das Get-AzStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

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

### -PassThru
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

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

### -Path
Gibt den Pfad einer Datei an.
Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.
Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.
Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Freigeben
Gibt ein **CloudFileShare** -Objekt an.
Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.
Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.
Dieses Objekt enthält den Speicherkontext.
Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Freigabename
Gibt den Namen der Dateifreigabe an.
Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. WindowsAz. Storage. File. CloudFileShare
Parameter: freigeben (ByValue)

### Microsoft. WindowsAz. Storage. File. CloudFileDirectory
Parameter: Verzeichnis (ByValue)

### Microsoft. WindowsAz. Storage. File. clouddatei
Parameter: Datei (ByValue)

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAz. Storage. File. clouddatei

## Notizen

## Verwandte Links

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Satz-AzStorageFileContent](./Set-AzStorageFileContent.md)


