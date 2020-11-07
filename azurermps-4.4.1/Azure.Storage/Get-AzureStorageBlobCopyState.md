---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6a61e076bf91d1ed994f9745d18a6f4832925250
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663628"
---
# Get-AzureStorageBlobCopyState

## Synopsis
Ruft den Kopierstatus eines Azure Storage-BLOBs ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### NamePipeline (Standard)
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageBlobCopyState** " Ruft den Kopierstatus eines Azure Storage-BLOBs ab.

## Beispiele

### Beispiel 1: Abrufen des Kopierstatus eines BLOB
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

Dieser Befehl ruft den Kopierstatus des BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads ab.

### Beispiel 2: Abrufen des Kopierstatus für ein BLOB mithilfe der Pipeline
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

Dieser Befehl ruft das BLOB mit dem Namen ContosoPlanning2015 im Container ContosoUploads mit dem Cmdlet **Get-AzureStorageBlob** ab und übergibt dann das Ergebnis mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das Cmdlet " **Get-AzureStorageBlobCopyState** " Ruft den Kopierstatus für diesen BLOB ab.

### Beispiel 3: Abrufen des Kopierstatus für ein BLOB in einem Container mithilfe der Pipeline
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

Dieser Befehl ruft den mit dem Cmdlet **Get-AzureStorageBlob** benannten Container ab und übergibt dann das Ergebnis an das aktuelle Cmdlet.
Das Cmdlet " **Get-AzureStorageContainer** " Ruft den Kopierstatus für das BLOB mit dem Namen ContosoPlanning2015 in diesem Container ab.

## Parameter

### -BLOB
Gibt den Namen eines BLOB an.
Dieses Cmdlet ruft den Zustand des BLOB-Kopiervorgangs für das Azure Storage-BLOB ab, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.
Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.
Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
Gibt ein **CloudBlob** -Objekt aus der Azure Storage-Client Bibliothek an.
Verwenden Sie das Get-AzureStorageBlob-Cmdlet, um ein **CloudBlob** -Objekt zu erhalten.

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Gibt ein **CloudBlobContainer** -Objekt aus der Azure Storage-Client Bibliothek an.
Dieses Cmdlet ruft den Kopierstatus eines BLOB im Container ab, das dieser Parameter angibt.
Verwenden Sie das Get-AzureStorageContainer-Cmdlet, um ein **CloudBlobContainer** -Objekt zu erhalten.

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.
Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.
Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.
Der Standardwert ist 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Container
Gibt den Namen eines Containers an.
Dieses Cmdlet ruft den Kopierstatus für ein BLOB im Container ab, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie das New-AzureStorageContext-Cmdlet, um einen Speicherkontext zu erhalten.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das Timeoutintervall für dienstseitige Dienste für eine Anforderung in Sekunden an.
Wenn das angegebene Intervall verstreicht, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Gibt an, dass das Cmdlet auf die Fertigstellung der Kopie wartet.
Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### IStorageContext

Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

## Ausgaben

### CopyState

## Notizen

## Verwandte Links

[Anfang-AzureStorageBlobCopy](./Start-AzureStorageBlobCopy.md)

[Stopp-AzureStorageBlobCopy](./Stop-AzureStorageBlobCopy.md)


