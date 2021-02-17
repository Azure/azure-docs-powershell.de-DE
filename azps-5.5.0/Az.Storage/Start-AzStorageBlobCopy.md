---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: ba8131ba496d51ba5597995e24f873fe2e186435
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164724"
---
# Start-AzStorageBlobCopy

## SYNOPSIS
Beginnt mit dem Kopieren eines BLOB.

## SYNTAX

### ContainerName (Standard)
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobInstance
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobInstanceToBlobInstance
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ContainerInstance
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ShareName
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ShareInstance
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DirInstance
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FileInstance
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FileInstanceToBlobInstance
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UriPipeline
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Start-AzStorageBlobCopy"** beginnt mit dem Kopieren eines BLOB.

## BEISPIELE

### Beispiel 1: Kopieren eines benannten BLOB
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

Mit diesem Befehl wird der Kopiervorgang des BLOB namens "ContosoPlanning2015" aus dem Container "ContosoUploads" in den Container "ContosoArchives" gestartet.

### Beispiel 2: Get a container to specify blobs to copy
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

Dieser Befehl ruft den Container "ContosoUploads" mit dem **Cmdlet "Get-AzStorageContainer"** ab und übergibt den Container dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet startet den Kopiervorgang des BLOB namens "ContosoPlanning2015".
Im vorherigen Cmdlet wird der Quellcontainer verwendet.
Der *Parameter "DestContainer"* gibt "ContosoArchives" als Zielcontainer an.

### Beispiel 3: Alle Blobs in einem Container erhalten und kopieren
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

Dieser Befehl ruft die BLOBS im Container mit dem Namen "ContosoUploads" mithilfe des **Cmdlets "Get-AzStorageBlob"** ab und übergibt dann die Ergebnisse mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Dieses Cmdlet startet den Kopiervorgang der Blobs in den Container "ContosoArchives".

### Beispiel 4: Kopieren eines blobs, das als Objekt angegeben ist
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

Der erste Befehl ruft das BLOB namens "ContosoPlanning2015" im Container "ContosoUploads" ab.
Der Befehl speichert dieses Objekt in der $SrcBlob Variable.
Der zweite Befehl ruft das BLOB namens "ContosoPlanning2015Archived" im Container "ContosoArchives" ab.
Der Befehl speichert dieses Objekt in der $DestBlob Variable.
Der letzte Befehl startet den Kopiervorgang aus dem Quellcontainer in den Zielcontainer.
Der Befehl verwendet die standardmäßige Punktformatierung, um die **ICloudBlob-Objekte** für die $SrcBlob und $DestBlob anzugeben.

### Beispiel 5: Kopieren eines BLOB aus einem URI
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

Dieser Befehl erstellt einen Kontext für das Konto "ContosoGeneral", das den angegebenen Schlüssel verwendet, und speichert diesen Schlüssel dann in der $Context Variable.
Der zweite Befehl kopiert die Datei aus dem angegebenen URI in das BLOB namens "ContosoPlanning" im Container "ContosoArchive".
Der Befehl startet den Kopiervorgang in den Zielkontext, der in $Context.
Es gibt keinen Quellspeicherkontext, daher muss der Quell-URI Zugriff auf das Quellobjekt haben. Beispiel: Wenn es sich bei der Quelle um kein öffentliches Azure-BLOB handelt, sollte der URI das SAS-Token enthalten, das Lesezugriff auf das BLOB hat.

### Beispiel 6: Kopieren eines Block-BLOB-in-Zielcontainers mit einem neuen BLOB-Namen und Festlegen des Ziel-BLOB StandardBlobTier als "Hot", "ResdatumePriority" auf "High"
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

Mit diesem Befehl wird der Kopiervorgang eines Block-BLOB-zu-Zielcontainers mit einem neuen BLOB-Namen gestartet und das Ziel-BLOB StandardBlobTier als "Hot", "RenervePriority" auf "High" festgelegt.

## PARAMETERS

### -AbsoluteUri
Gibt den absoluten URI einer Datei an, die in ein Azure Storage-BLOB kopiert werden soll.

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BlobBaseClient
BlobBaseClient-Objekt

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -CloudBlob
Gibt ein **CloudBlob-Objekt** aus der Azure Storage Client Library an.
Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -CloudBlobContainer
Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.
Dieses Cmdlet kopiert ein BLOB aus dem Container, den dieser Parameter angibt.
Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -DestBlob
Gibt den Namen des Ziel-BLOB an.

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestCloudBlob
Gibt ein **Ziel-CloudBlob-Objekt** an.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestContainer
Gibt den Namen des Zielcontainers an.

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestContext
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Gibt an, dass dieses Cmdlet den Ziel-BLOB überschreibt, ohne dass Sie zur Bestätigung aufgefordert werden.

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

### -PremiumPageBlobTier
Premium-Seite-BLOB-Stufe

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReoreePriority
Block BLOB Re hexadePriority. Gibt die Priorität an, mit der ein archiviertes BLOB neu auf ihre BloBs umgekniert werden soll. Gültige Werte sind "Hoch/Standard".

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an.
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

### -SrcBlob
Gibt den Namen des Quell-BLOB an.

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SrcContainer
Gibt den Namen des Quellcontainers an.

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SrcDir
Gibt ein **CloudFileDirectory-Objekt** aus der Azure Storage Client Library an.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SrcFile
Gibt ein **CloudFile-Objekt** aus der Azure Storage Client Library an.
Sie können das Cmdlet erstellen oder Get-AzStorageFile verwenden.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SrcFilePath
Gibt den relativen Pfad der Quelldatei des Quellverzeichnisses oder der Quellfreigabe an.

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SrcShare
Gibt ein **CloudFileShare-Objekt** aus der Azure Storage Client Library an.
Sie können das Cmdlet erstellen oder Get-AzStorageShare verwenden.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SrcShareName
Gibt den Quellfreigabenamen an.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardBlobTier
Block BLOB Tier, gültige Werte sind Hot/Cool/Archive.
Details finden Sie unter https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Storage.Blob.CloudBlob

### Microsoft.Azure.Storage.Blob.CloudBlobContainer

### Microsoft.Azure.Storage.File.CloudFile

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageBlobCopyState](./Get-AzStorageBlobCopyState.md)

[Stop-AzStorageBlobCopy](./Stop-AzStorageBlobCopy.md)
