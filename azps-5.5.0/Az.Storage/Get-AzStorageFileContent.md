---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143889"
---
# Get-AzStorageFileContent

## SYNOPSIS
Lädt den Inhalt einer Datei herunter.

## SYNTAX

### ShareName (Standard)
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Freigeben
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Verzeichnis
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### Datei
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzStorageFileContent"** lädt den Inhalt einer Datei herunter und speichert ihn dann an einem von Ihnen angegebenen Ziel.
Dieses Cmdlet gibt den Inhalt der Datei nicht zurück.

## BEISPIELE

### Beispiel 1: Herunterladen einer Datei aus einem Ordner
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Mit diesem Befehl wird eine Datei mit dem Namen "CurrentDataFile" im Ordner "ContosoWorkingFolder" aus der Dateifreigabe "ContosoShare06" in den aktuellen Ordner heruntergeladen.

### Beispiel 2: Herunterladen der Dateien unter "Beispieldateifreigabe"
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

In diesem Beispiel werden die Dateien unter "Beispieldateifreigabe" heruntergeladen.

### Beispiel 3: Laden Sie eine Azure-Datei in eine lokale Datei herunter, und reservieren Sie die Azure File -SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der lokalen Datei.
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

In diesem Beispiel wird eine Azure-Datei in eine lokale Datei heruntergeladen, und die Azure File -SMB-Eigenschaften ("File Attributtes", "File Creation Time", "File Last Write Time") werden in der lokalen Datei gespeichert.

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

### -CheckMd5
Gibt an, ob die Md5-Summe für die heruntergeladene Datei überprüft werden soll.

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

### -ClientTimeoutPerRequest
Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an. Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt. Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.

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
Gibt die maximalen gleichzeitigen Netzwerkanrufe an. Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben. Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert. Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde. Der Standardwert ist 10.

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
Gibt einen Azure Storage-Kontext an. Verwenden Sie zum Abrufen eines Kontexts das New-AzStorageContext Cmdlet.

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

### -Destination
Gibt den Zielpfad an.
Dieses Cmdlet lädt die Dateiinhalte an den von diesem Parameter angegebenen Speicherort herunter.
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und den Parameter *"Force"* angeben, überschreibt das Cmdlet die Datei.
Wenn Sie einen Pfad für eine vorhandene Datei und nicht "Erzwingen" *angeben,* werden Sie vom Cmdlet vor dem Fortlauf dazu aufgefordert.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure -Speicherdatei zu erstellen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Directory
Gibt einen Ordner als **CloudFileDirectory-Objekt** an.
Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.
Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.
Sie können das cmdlet Get-AzStorageFile auch zum Abrufen eines Verzeichnisses verwenden.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -File
Gibt eine Datei als **CloudFile-Objekt** an.
Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.
Verwenden Sie zum Abrufen eines **CloudFile-Objekts** das Get-AzStorageFile-Cmdlet.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in der neuen Datei.
Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und den Parameter *"Force"* angeben, überschreibt das Cmdlet die Datei.
Wenn Sie einen Pfad für eine vorhandene Datei und nicht "Erzwingen" *angeben,* werden Sie vom Cmdlet vor dem Fortlauf dazu aufgefordert.
Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei mit dem Namen der Azure -Speicherdatei zu erstellen.

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

### -PassThru
Gibt an, dass dieses Cmdlet das **heruntergeladene "AzureStorageFile"-Objekt** zurückgibt.

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

### -Path
Gibt den Pfad einer Datei an.
Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.
Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreserveSMBAttribute
Behalten Sie die Eigenschaften des Quelldatei-SMB (File Attributtes, File Creation Time, File Last Write Time) in der Zieldatei bei. Dieser Parameter ist nur unter Windows verfügbar.

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

### -ServerTimeoutPerRequest
Gibt das dienstseitige Zeitintervall (in Sekunden) für eine Anforderung an. Wenn das angegebene Intervall verstrichen ist, bevor der Dienst die Anforderung verarbeitet, gibt der Speicherdienst einen Fehler zurück.

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

### -Teilen
Gibt ein **CloudFileShare-Objekt** an.
Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Dateifreigabe herunter.
Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.
Dieses Objekt enthält den Speicherkontext.
Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ShareName
Gibt den Namen der Dateifreigabe an.
Dieses Cmdlet lädt den Inhalt der Datei in der von diesem Parameter angegebenen Dateifreigabe herunter.

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

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzStorageFile](./Get-AzStorageFile.md)

[Set-AzStorageFileContent](./Set-AzStorageFileContent.md)


