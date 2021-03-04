---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946337"
---
# New-AzBatchResourceFile

## SYNOPSIS
Erstellt eine Ressourcendatei für die Verwendung von `New-AzBatchTask` .

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
Erstellt eine Ressourcendatei für die Verwendung von `New-AzBatchTask` .

## BEISPIELE

### Beispiel 1: Erstellen einer Ressourcendatei aus einer HTTP-URL, die auf eine einzelne Datei verweist
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Bezug auf eine HTTP-URL.

### Beispiel 2: Erstellen einer Ressourcendatei aus einer Azure Storage-Container-URL
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Bezug auf eine Azure Storage-Container-URL. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

### Beispiel 3: Erstellen einer Ressourcendatei aus einem Namen des Automatischen Speichercontainers
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

Erstellt einen `PSResourceFile` Bezug auf einen Namen des Containernamens für den automatischen Speicher. Alle Dateien im Container werden in den angegebenen Ordner heruntergeladen.

## PARAMETER

### -AutoStorageContainerName
Der Name des Speichercontainers im automatischen Speicherkonto.

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
Ruft das Blobpräfix ab, das beim Herunterladen von Blobs aus einem Azure Storage-Container verwendet werden soll.
Es werden nur die Blobs heruntergeladen, deren Namen mit dem angegebenen Präfix beginnen.
Dieses Präfix kann ein teilweiser Dateiname oder ein Unterverzeichnis sein.
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
Der Speicherort auf dem Computeknoten, in den die Datei(en) heruntergeladen werden soll, relativ zum Arbeitsverzeichnis der Aufgabe. Wenn der Parameter HttpUrl angegeben ist, ist filePath erforderlich und beschreibt den Pfad, in den die Datei heruntergeladen wird, einschließlich des Dateinamens. Wenn andernfalls die Parameter AutoStorageContainerName oder StorageContainerUrl angegeben werden, ist FilePath optional und das Verzeichnis zum Herunterladen der Dateien. In dem Fall, in dem FilePath als Verzeichnis verwendet wird, wird jede Verzeichnisstruktur, die bereits mit den Eingabedaten verknüpft ist, vollständig beibehalten und an das angegebene FilePath-Verzeichnis angefügt. Der angegebene relative Pfad kann nicht aus dem Arbeitsverzeichnis der Aufgabe herausbrechen (z. B. mithilfe von "..")..

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
Wenn es sich bei der URL um Azure Blob Storage handelt, muss sie mit anonymen Zugriffen lesbar sein. Das heißt, der Batchdienst stellt beim Herunterladen des Blobs keine Anmeldeinformationen bereit.
Es gibt zwei Möglichkeiten, um eine solche URL für einen Blob im Azure-Speicher zu erhalten: eine SAS (Shared Access Signature), die Leseberechtigungen für den Blob erteilt, oder die ACL für den Blob oder dessen Container festlegen, um den öffentlichen Zugriff zu ermöglichen.

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
Die URL des Blobcontainers in Azure Blob Storage.
Diese URL muss mit anonymen Zugriffen lesbar und auflistend sein. Das heißt, der Batchdienst stellt beim Herunterladen von Blobs aus dem Container keine Anmeldeinformationen bereit.
Es gibt zwei Möglichkeiten, um eine solche URL für einen Container im Azure-Speicher zu erhalten: eine SAS (Shared Access Signature), die Leseberechtigungen für den Container erteilt, oder die ACL für den Container festlegen, um den öffentlichen Zugriff zu ermöglichen.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSResourceFile

## NOTIZEN

## VERWANDTE LINKS

[New-AzBatchTask](./New-AzBatchTask.md)