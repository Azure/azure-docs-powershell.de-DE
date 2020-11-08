---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997141"
---
# New-AzBatchResourceFile

## Synopsis
Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .

## Syntax

### HttpUrl (Standard)
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContainerUrl
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AutoStorageContainerName
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .

## Beispiele

### Beispiel 1: Erstellen einer Ressourcendatei aus einer HTTP-URL, die auf eine einzelne Datei zeigt
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweis auf eine HTTP-URL.

### Beispiel 2: Erstellen einer Ressourcendatei aus einer Azure-Speichercontainer-URL
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweis auf eine Azure-Speichercontainer-URL. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

### Beispiel 3: Erstellen einer Ressourcendatei aus dem Namen eines automatischen Speichercontainers
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweis auf den Namen eines automatischen Speichercontainers. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

## Parameter

### -AutoStorageContainerName
Der Name des Speichercontainers im Auto Speicherkonto.

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobPrefix
Ruft das BLOB-Präfix ab, das verwendet werden soll, wenn BLOBs aus einem Azure-Speichercontainer heruntergeladen werden.
Es werden nur die BLOBs heruntergeladen, deren Namen mit dem angegebenen Präfix beginnen.
Bei diesem Präfix kann es sich um einen partiellen Dateinamen oder ein Unterverzeichnis handeln.
Wenn kein Präfix angegeben ist, werden alle Dateien im Container heruntergeladen.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileMode
Ruft das Attribut "Datei-Berechtigungsmodus" im oktalen Format ab.
Diese Eigenschaft gilt nur, wenn die Ressourcendatei auf einen Linux-Knoten heruntergeladen wird.
Wenn diese Eigenschaft für einen Linux-Knoten nicht angegeben ist, lautet der Standardwert 0770.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
Die Position auf dem Compute-Knoten, an den die Datei (en) bezogen auf das Arbeitsverzeichnis der Aufgabe heruntergeladen werden soll. Wenn der HttpUrl-Parameter angegeben wird, ist der Dateipfad erforderlich und beschreibt den Pfad, in den die Datei heruntergeladen wird, einschließlich des Datei namens. Wenn andernfalls die AutoStorageContainerName-oder StorageContainerUrl-Parameter angegeben werden, ist filePath optional und das Verzeichnis, in das die Dateien heruntergeladen werden sollen. In dem Fall, in dem filePath als Verzeichnis verwendet wird, wird jede Verzeichnisstruktur, die den Eingabedaten bereits zugeordnet ist, vollständig aufbewahrt und an das angegebene filePath-Verzeichnis angefügt. Der angegebene relative Pfad kann nicht aus dem Arbeitsverzeichnis des Vorgangs ausbrechen (beispielsweise mit "..").

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpUrl
Die URL der Datei, die heruntergeladen werden soll.
Wenn die URL Azure-BLOB-Speicher ist, muss Sie mithilfe des anonymen Zugriffs lesbar sein. Das bedeutet, dass der Batch Dienst beim Herunterladen des BLOBs keine Anmeldeinformationen enthält.
Es gibt zwei Möglichkeiten zum Abrufen einer solchen URL für ein BLOB im Azure-Speicher: Fügen Sie eine freigegebene zugriffssignatur (SAS) mit Leseberechtigungen für das BLOB hinzu, oder legen Sie die ACL für das BLOB oder dessen Container so ein, dass der öffentliche Zugriff zulässig ist.

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerUrl
Die URL des BLOB-Containers im Azure BLOB-Speicher.
Diese URL muss mithilfe des anonymen Zugriffs lesbar und listenbar sein. Das bedeutet, dass der Batch Dienst beim Herunterladen von BLOBs aus dem Container keine Anmeldeinformationen darstellt.
Es gibt zwei Möglichkeiten zum Abrufen einer solchen URL für einen Container im Azure-Speicher: Fügen Sie eine freigegebene zugriffssignatur (SAS) mit Leseberechtigungen für den Container hinzu, oder legen Sie die ACL für den Container so ein, dass der öffentliche Zugriff zulässig ist.

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft.Azure.Commands.Batch. Models. PSResourceFile

## Notizen

## Verwandte Links

[Neu – AzBatchTask](./New-AzBatchTask.md)