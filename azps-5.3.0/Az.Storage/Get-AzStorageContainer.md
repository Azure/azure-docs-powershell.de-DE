---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458215"
---
# Get-AzStorageContainer

## SYNOPSIS
Listet die Speichercontainer auf.

## SYNTAX

### ContainerName (Standard)
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPrefix
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageContainer"** listet die Speichercontainer auf, die dem Speicherkonto in Azure zugeordnet sind.

## BEISPIELE

### Beispiel 1: Azure Storage BLOB nach Name erhalten
```
PS C:\>Get-AzStorageContainer -Name container*
```

In diesem Beispiel wird ein Platzhalterzeichen verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit dem Container beginnt.

### Beispiel 2: Azure Storage Container nach Containernamenpräfix erhalten
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

In diesem Beispiel wird der *Präfixparameter* verwendet, um eine Liste aller Container mit einem Namen zurückzukehren, der mit dem Container beginnt.

## PARAMETERS

### -ClientTimeoutPerRequest
Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.
Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.
Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Gibt die maximalen gleichzeitigen Netzwerkanrufe an.
Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.
Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.
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
Gibt den Speicherkontext an.
Zum Erstellen können Sie das cmdlet New-AzStorageContext erstellen.
Die Containerberechtigungen werden nicht abgerufen, wenn Sie einen aus dem SAS-Token erstellten Speicherkontext verwenden, da für Abfragecontainerberechtigungen die Schlüsselberechtigung für das Speicherkonto erforderlich ist.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
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

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -MaxCount
Gibt die maximale Anzahl von Objekten an, die dieses Cmdlet zurückgibt.

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

### -Name
Gibt den Containernamen an.
Wenn der Containername leer ist, werden im Cmdlet alle Container aufgeführt.
Andernfalls werden alle Container aufgeführt, die dem angegebenen Namen oder dem normalen Namensmuster entsprechen.

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Gibt ein Präfix an, das im Namen des Containers oder der Container verwendet wird, den bzw. die Sie erhalten möchten.
Sie können dies verwenden, um alle Container zu finden, die mit derselben Zeichenfolge beginnen, z. B. "my" oder "test".

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das intervallseitige Dienstzeitintervall (in Sekunden) für eine Anforderung an.
Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)

[Set-AzStorageContainerAcl](./Set-AzStorageContainerAcl.md)


