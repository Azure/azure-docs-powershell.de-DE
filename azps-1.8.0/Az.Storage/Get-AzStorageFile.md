---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 72cd3388c69947b0209c224943a3eda583e306b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658869"
---
# Get-AzStorageFile

## Synopsis
Listet Verzeichnisse und Dateien für einen Pfad auf.

## Syntax

### Freigabename (Standard)
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Freigeben
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Verzeichnis
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzStorageFile** " listet Verzeichnisse und Dateien für die von Ihnen angegebene Freigabe oder das Verzeichnis auf.
Geben Sie den *path* -Parameter an, um eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad abzurufen.
Dieses Cmdlet gibt **AzureStorageFile** -und **AzureStorageDirectory** -Objekte zurück.
Sie können die **IsDirectory** -Eigenschaft verwenden, um zwischen Ordnern und Dateien zu unterscheiden.

## Beispiele

### Beispiel 1: Auflisten von Verzeichnissen in einer Freigabe
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

Dieser Befehl listet nur die Verzeichnisse in der Freigabe-ContosoShare06 auf.
Sie ruft zunächst beide Dateien und Verzeichnisse ab, übergibt Sie mithilfe des Pipelineoperators an den **Where** -Operator und verwirft dann alle Objekte, deren Typ nicht "CloudFileDirectory" ist.

### Beispiel 2: Auflisten eines Dateiverzeichnisses
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

Dieser Befehl listet die Dateien und Ordner im Verzeichnis ContosoWorkingFolder unter der Freigabe ContosoShare06 auf.
Zuerst wird die Verzeichnisinstanz abgerufen und anschließend an das Cmdlet " **Get-AzStorageFile** " weitergeleitet, um das Verzeichnis aufzulisten.

## Parameter

### -ClientTimeoutPerRequest
Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.
Wenn der vorherige Aufruf innerhalb des angegebenen Intervalls fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.
Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.

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
Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.
Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.
Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.
Der Standardwert ist 10.

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
Gibt einen Azure-Speicherkontext an.
Verwenden Sie das New-AzStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

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

### -Verzeichnis
Gibt einen Ordner als **CloudFileDirectory** -Objekt an.
Dieses Cmdlet ruft den Ordner ab, den dieser Parameter angibt.
Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.
Sie können auch das Cmdlet **Get-AzStorageFile** verwenden, um ein Verzeichnis abzurufen.

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

### -Path
Gibt den Pfad eines Ordners an.
Wenn Sie den *path* -Parameter nicht angeben, listet **Get-AzStorageFile** die Verzeichnisse und Dateien in der angegebenen Dateifreigabe oder dem angegebenen Verzeichnis auf.
Wenn Sie den *path* -Parameter einbeziehen, gibt **Get-AzStorageFile** eine Instanz eines Verzeichnisses oder einer Datei im angegebenen Pfad zurück.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das dienstseitige Timeoutintervall für eine Anforderung in Sekunden an.
Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.

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
Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.
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
Dieses Cmdlet ruft eine Datei oder ein Verzeichnis aus der Dateifreigabe ab, die dieser Parameter angibt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. WindowsAzure. Storage. File. CloudFileShare

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Storage. File. clouddatei

## Notizen

## Verwandte Links

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)

[Neu – AzStorageDirectory](./New-AzStorageDirectory.md)

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[Remove-AzStorageFile](./Remove-AzStorageFile.md)

[Satz-AzStorageFileContent](./Set-AzStorageFileContent.md)


