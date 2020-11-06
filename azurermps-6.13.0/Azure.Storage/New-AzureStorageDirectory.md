---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: b5d28a2c156572909f5d1e943473dbbf2c527d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498622"
---
# New-AzureStorageDirectory

## Synopsis
Erstellt ein Verzeichnis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Freigabename (Standard)
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Freigeben
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### Verzeichnis
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureStorageDirectory** erstellt ein Verzeichnis.
Dieses Cmdlet gibt ein **CloudFileDirectory** -Objekt zurück.

## Beispiele

### Beispiel 1: Erstellen eines Ordners in einer Dateifreigabe
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Dieser Befehl erstellt einen Ordner mit dem Namen ContosoWorkingFolder in der Dateifreigabe mit dem Namen ContosoShare06.

### Beispiel 2: Erstellen eines Ordners in einer Dateifreigabe, die in einem Dateifreigabe Objekt angegeben ist
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

Dieser Befehl verwendet das Cmdlet " **Get-AzureStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet erstellt den Ordner mit dem Namen ContosoWorkingFolder in ContosoShare06.

## Parameter

### -ClientTimeoutPerRequest
Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.
Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.
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
Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
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
Mit diesem Cmdlet wird der Ordner an dem Speicherort erstellt, den dieser Parameter angibt.
Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.
Sie können auch das Get-AzureStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.

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
Dieses Cmdlet erstellt einen Ordner für den von diesem Cmdlet festgelegten Pfad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.

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
Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.
Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.
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
Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.

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
Parameter: freigeben (ByValue)

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory
Parameter: Verzeichnis (ByValue)

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Storage. File. CloudFileDirectory

## Notizen

## Verwandte Links

[Get-AzureStorageFile](./Get-AzureStorageFile.md)

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[Neu – AzureStorageContext](./New-AzureStorageContext.md)

[Neu – AzureStorageDirectory](./New-AzureStorageDirectory.md)

[Remove-AzureStorageDirectory](./Remove-AzureStorageDirectory.md)
