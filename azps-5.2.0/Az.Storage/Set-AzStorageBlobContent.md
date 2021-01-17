---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d99bde2839e1b4e91d6299cd47319827a57f4f33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303320"
---
# Set-AzStorageBlobContent

## SYNOPSIS
Lädt eine lokale Datei in ein Azure Storage-BLOB hoch.

## SYNTAX

### SendManual (Standard)
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerPipeline
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobPipeline
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzStorageBlobContent"** lädt eine lokale Datei in ein Azure Storage-BLOB hoch.

## BEISPIELE

### Beispiel 1: Hochladen einer benannten Datei
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

Mit diesem Befehl wird die Datei mit dem Namen "PlanningData" in ein BLOB namens "Planning2015" hochgeladen.

### Beispiel 2: Hochladen aller Dateien unter dem aktuellen Ordner
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

Dieser Befehl verwendet das core Windows PowerShell-Cmdlet Get-ChildItem, um alle Dateien im aktuellen Ordner und in Unterordnern zu erhalten, und übergibt sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das **Cmdlet "Set-AzStorageBlobContent"** lädt die Dateien in den Container "ContosoUploads" hoch.

### Beispiel 3: Überschreiben eines vorhandenen BLOB
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

Dieser Befehl ruft das BLOB namens Planning2015 im Container "ContosoUploads" mithilfe des Cmdlets Get-AzStorageBlob ab und übergibt dieses BLOB dann an das aktuelle Cmdlet.
Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.
Dieser Befehl gibt den Parameter *"Force" nicht* an.
Der Befehl fordert Sie zur Bestätigung auf.
Wenn Sie den Befehl bestätigen, überschreibt das Cmdlet das vorhandene BLOB.

### Beispiel 4: Hochladen einer Datei in einen Container mithilfe der Pipeline
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

Dieser Befehl ruft den Container ab, der mit der Zeichenfolge "ContosoUpload" mit dem **Cmdlet "Get-AzStorageContainer"** beginnt, und übergibt dieses BLOB dann an das aktuelle Cmdlet.
Der Befehl lädt die Datei mit dem Namen "ContosoPlanning" als "Planning2015" hoch.

### Beispiel 5: Hochladen einer Datei auf den Seiten-BLOB mit Metadaten und PremiumPageBlobTier als P10
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

Der erste Befehl erstellt eine Hashtabelle, die Metadaten für ein BLOB enthält, und speichert diese Hashtabelle in der $Metadata Variable.
Mit dem zweiten Befehl wird die Datei mit dem Namen "ContosoPlanning" in den Container "ContosoUploads" hochgeladen.
Das BLOB enthält die metadaten, die in $Metadata gespeichert sind, und verfügt über PremiumPageBlobTier als P10.

### Beispiel 6: Hochladen einer Datei in blob mit angegebenen BLOB-Eigenschaften und Festlegen von "StandardBlobTier" auf "Cool"
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

Dieser Befehl lädt die Datei c:\temp\index.html in den Container mit dem Namen "contosouploads" mit angegebenen BLOB-Eigenschaften hoch, und legen Sie "StandardBlobTier" als "Cool" fest.
Mit diesem Befehl wird der ContentType-Wert von der [System.Web.MimeMapping]::GetMimeMapping()-API auf BLOB-Eigenschaften festgelegt.

## PARAMETERS

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus.

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

### -BLOB
Gibt den Namen eines BLOB an.
Dieses Cmdlet lädt eine Datei in das Azure Storage-BLOB hoch, das dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobType
Gibt den Typ für den BLOB an, den dieses Cmdlet hochlädt.
Die zulässigen Werte für diesen Parameter sind:
- Blockieren
- Seite
- Anfügen Der Standardwert ist "Block".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Gibt ein **CloudBlob-Objekt** an.
Verwenden Sie zum **Abrufen eines CloudBlob-Objekts** das Get-AzStorageBlob-Cmdlet.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Gibt ein **CloudBlobContainer-Objekt** aus der Azure Storage Client Library an.
Dieses Cmdlet lädt Inhalte in ein BLOB im Container hoch, den dieser Parameter angibt.
Verwenden Sie zum **Abrufen eines CloudBlobContainer-Objekts** das Get-AzStorageContainer Cmdlet.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

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

### -Container
Gibt den Namen eines Containers an.
Dieses Cmdlet lädt eine Datei in ein BLOB im Container hoch, den dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.
Wenn Sie einen Speicherkontext verwenden möchten, der aus einem SAS-Token ohne Leseberechtigung erstellt wurde, müssen Sie den Parameter "add -Force" verwenden, um das Vorhandensein von Blobs zu überspringen.

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

### -File
Gibt einen lokalen Dateipfad für eine Datei an, die als BLOB-Inhalt hochgeladen werden soll.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Gibt an, dass dieses Cmdlet ein vorhandenes BLOB überschreibt, ohne dass Sie zur Bestätigung aufgefordert werden.

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

### -Metadata
Gibt Die Metadaten für den hochgeladenen BLOB an.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PremiumPageBlobTier
Page Blob Tier

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Properties
Gibt Eigenschaften für den hochgeladenen BLOB an. Die unterstützten Eigenschaften sind: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
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

### System.String

### Microsoft.Azure.Storage.Blob.CloudBlobContainer

### Microsoft.Azure.Storage.Blob.CloudBlob

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Remove-AzStorageBlob](./Remove-AzStorageBlob.md)
