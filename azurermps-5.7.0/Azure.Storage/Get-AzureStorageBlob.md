---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478825"
---
# Get-AzureStorageBlob

## Synopsis
Listet BLOBs in einem Container auf.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Blobname (Standard)
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPrefix
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureStorageBlob** " listet BLOBs im angegebenen Container in einem Azure Storage-Konto auf.

## Beispiele

### Beispiel 1: Abrufen eines BLOB nach BLOB-Namen
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

Dieser Befehl verwendet einen BLOB-Namen und Platzhalter, um einen BLOB abzurufen.

### Beispiel 2: Abrufen von BLOBs in einem Container mithilfe der Pipeline
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

Dieser Befehl verwendet die Pipeline, um alle BLOBs (einschließlich BLOBs im gelöschten Status) in einem Container abzurufen.

### Beispiel 3: Abrufen von BLOBs nach Namen Präfix
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

Dieser Befehl verwendet ein Namenspräfix, um BLOBs abzurufen.

### Beispiel 4: Auflisten von BLOBs in mehreren Batches
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

In diesem Beispiel werden die *MaxCount* -und *ContinuationToken* -Parameter verwendet, um Azure-Speicher-BLOBs in mehreren Batches aufzulisten.
Die ersten vier Befehle weisen Variablenwerte zu, die im Beispiel verwendet werden sollen.

Der fünfte Befehl gibt eine **do-while-** Anweisung an, die das Cmdlet **Get-AzureStorageBlob** zum Abrufen von BLOBs verwendet.
Die Anweisung enthält das Fortsetzungstoken, das in der $Token Variablen gespeichert ist.
$Token ändert den Wert während der Ausführung der Schleife.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help About_Do` .

Der endgültige Befehl verwendet den Befehl **Echo** , um die Summe anzuzeigen.

## Parameter

### -BLOB
Gibt ein Name-oder Name-Muster an, das für eine Platzhaltersuche verwendet werden kann.
Wenn kein BLOB-Name angegeben wird, listet das Cmdlet alle Blobs im angegebenen Container auf.
Wenn für diesen Parameter ein Wert angegeben wird, listet das Cmdlet alle Blobs mit Namen auf, die diesem Parameter entsprechen.

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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
Gibt den Namen des Containers an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Context
Gibt das Azure-Speicherkonto an, aus dem Sie eine Liste von BLOBs abrufen möchten.
Sie können das New-AzureStorageContext-Cmdlet verwenden, um einen Speicherkontext zu erstellen.

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

### -ContinuationToken
Gibt ein Fortsetzungstoken für die BLOB-Liste an.
Verwenden Sie diesen Parameter und den *MaxCount* -Parameter, um BLOBs in mehreren Batches aufzulisten.

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDeleted
BLOB für gelöschte Elemente einbeziehen Standardmäßig wird BLOB nicht gelöscht.

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

### -MaxCount
Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.

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

### -Prefix
Gibt ein Präfix für die BLOB-Namen an, die Sie abrufen möchten.
Dieser Parameter unterstützt nicht die Verwendung regulärer Ausdrücke oder Platzhalterzeichen für die Suche.
Wenn der Container nur BLOBs mit dem Namen "My", "MyBlob1" und "MyBlob2" enthält und Sie "-prefix My *" angeben, gibt das Cmdlet keine BLOBs zurück.
Wenn Sie jedoch "-prefix My" angeben, gibt das Cmdlet "My", "MyBlob1" und "MyBlob2" zurück.

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### IStorageContext
Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.

## Ausgaben

### AzureStorageBlob

## Notizen

## Verwandte Links

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Remove-AzureStorageBlob](./Remove-AzureStorageBlob.md)

[Satz-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)


