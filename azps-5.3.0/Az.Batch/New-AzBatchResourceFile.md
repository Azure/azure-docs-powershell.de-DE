---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471133"
---
# New-AzBatchResourceFile

## SYNOPSIS
Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .

## SYNTAX

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

## BESCHREIBUNG
Erstellt eine Ressourcendatei zur Verwendung durch `New-AzBatchTask` .

## BEISPIELE

### Beispiel 1: Erstellen einer Ressourcendatei aus einer HTTP-URL, die auf eine einzelne Datei zeigt
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweisen auf eine HTTP-URL.

### Beispiel 2: Erstellen einer Ressourcendatei aus einer Azure Storage-Container-URL
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweisen auf eine Azure Storage-Container-URL. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

### Beispiel 3: Erstellen einer Ressourcendatei aus einem Containernamen für den automatischen Speicher
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Verweisen auf einen Containernamen für den automatischen Speicher. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

## PARAMETERS

### -AutoStorageContainerName
Der Name des Speichercontainers im Konto für den automatischen Speicher.

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
Ruft das BLOB-Präfix ab, das beim Herunterladen von Blobs aus einem Azure Storage-Container verwendet wird.
Nur blobs, deren Namen mit dem angegebenen Präfix beginnen, werden heruntergeladen.
Dieses Präfix kann ein Teildateiname oder ein Unterverzeichnis sein.
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

### -FileMode
Ruft das Attribut für den Dateiberechtigungsmodus im oktalen Format ab.
Diese Eigenschaft gilt nur, wenn die Ressourcendatei auf einen Linux-Knoten heruntergeladen wird.
Wenn diese Eigenschaft für einen Linux-Knoten nicht angegeben ist, ist der Standardwert 0770.

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
Der Speicherort auf dem Berechnungsknoten, an den die Datei(en) heruntergeladen werden, relativ zum Arbeitsverzeichnis der Aufgabe. Wenn der Parameter "HttpUrl" angegeben wird, ist "FilePath" erforderlich und beschreibt den Pfad, auf den die Datei heruntergeladen wird, einschließlich des Dateinamens. Wenn andernfalls die Parameter "AutoStorageContainerName" oder "StorageContainerUrl" angegeben werden, ist "FilePath" optional und das Verzeichnis, in das die Dateien heruntergeladen werden sollen. In dem Fall, in dem FilePath als Verzeichnis verwendet wird, wird jede Verzeichnisstruktur, die bereits mit den Eingabedaten verknüpft ist, vollständig aufbewahrt und an das angegebene Verzeichnis "FilePath" angefügt. Der angegebene relative Pfad kann nicht aus dem Arbeitsverzeichnis des Vorgangs herausbrechen (z. B. mithilfe von '..').

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
Die URL der herunterzuladende Datei.
Wenn es sich bei der URL um Azure Blob Storage handelt, muss sie über anonymen Zugriff lesbar sein. Das heißt, beim Herunterladen des BLOB werden vom Batchdienst keine Anmeldeinformationen angegeben.
Es gibt zwei Möglichkeiten, eine solche URL für ein BLOB im Azure-Speicher zu erhalten: Fügen Sie eine SAS (Shared Access Signature) hinzu, die Leseberechtigungen für das BLOB erteilt, oder legen Sie die ACL für das BLOB oder seinen Container so ein, dass der öffentliche Zugriff gewährt wird.

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
Die URL des BLOB-Containers im Azure Blob Storage.
Diese URL muss über anonymen Zugriff lesbar und auflistenbar sein. Das bedeutet, dass der Batchdienst beim Herunterladen von BLOBS aus dem Container keine Anmeldeinformationen enthält.
Es gibt zwei Möglichkeiten zum Erhalten einer solchen URL für einen Container im Azure-Speicher: Fügen Sie eine SAS (Shared Access Signature) hinzu, die Leseberechtigungen für den Container erteilt, oder legen Sie die ACL für den Container so ein, dass der öffentliche Zugriff zulässig ist.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzBatchTask](./New-AzBatchTask.md)