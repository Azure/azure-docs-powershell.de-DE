---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303299"
---
# Set-AzStorageFileContent

## SYNOPSIS
Lädt den Inhalt einer Datei hoch.

## SYNTAX

### ShareName (Standard)
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Freigeben
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### Verzeichnis
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzStorageFileContent** lädt den Inhalt einer Datei in eine Datei auf einer angegebenen Freigabe hoch.

## BEISPIELE

### Beispiel 1: Hochladen einer Datei im aktuellen Ordner
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

Mit diesem Befehl wird eine Datei mit dem Namen "DataFile37" im aktuellen Ordner als Datei mit dem Namen "CurrentDataFile" im Ordner "ContosoWorkingFolder" hochgeladen.

### Beispiel 2: Hochladen aller Dateien im aktuellen Ordner
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

In diesem Beispiel werden mehrere Windows PowerShell cmdlets und das aktuelle Cmdlet verwendet, um alle Dateien aus dem aktuellen Ordner in den Stammordner des Container "ContosoShare06" hochzuladen.
Der erste Befehl ruft den Namen des aktuellen Ordners ab und speichert ihn in der $CurrentFolder Variable.
Der zweite Befehl verwendet das **Cmdlet "Get-AzStorageShare",** um die Dateifreigabe namens "ContosoShare06" zu erhalten, und speichert sie dann in der $Container Variable.
Der letzte Befehl ruft den Inhalt des aktuellen Ordners ab und übergibt jeden mit dem Pipelineoperator Where-Object an das cmdlet "Where-Object".
Dieses Cmdlet filtert Objekte heraus, die keine Dateien sind, und übergibt die Dateien dann an ForEach-Object Cmdlet.
Dieses Cmdlet führt einen Skriptblock für jede Datei aus, die den entsprechenden Pfad dafür erstellt und dann das aktuelle Cmdlet zum Hochladen der Datei verwendet.
Das Ergebnis hat denselben Namen und dieselbe relative Position in Bezug auf die anderen Dateien, die in diesem Beispiel hochgeladen werden.
Weitere Informationen zu Skriptblöcken erhalten Sie, wenn Sie `Get-Help about_Script_Blocks` ".

### Beispiel 3: Laden Sie eine lokale Datei in eine Azure-Datei hoch, und reservieren Sie die lokalen Datei-SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der Azure-Datei.
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

In diesem Beispiel wird eine lokale Datei in eine Azure-Datei hochgeladen, und die lokalen Datei-SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der Azure-Datei werden gespeichert.

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
Gibt einen Azure-Speicherkontext an.
Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)

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

### -Directory
Gibt einen Ordner als **CloudFileDirectory-Objekt** an.
Dieses Cmdlet lädt die Datei in den Ordner hoch, den dieser Parameter angibt.
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

### -Force
Gibt an, dass dieses Cmdlet eine vorhandene Azure -Speicherdatei überschreibt.

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
Gibt an, dass dieses Cmdlet das **azureStorageFile-Objekt** zurückgibt, das erstellt oder hochgeladen wird.

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
Gibt den Pfad einer Datei oder eines Ordners an.
Dieses Cmdlet lädt Inhalte in die Datei hoch, die dieser Parameter angibt, oder in eine Datei in dem Ordner, den dieser Parameter angibt.
Wenn Sie einen Ordner angeben, erstellt dieses Cmdlet eine Datei mit demselben Namen wie die Quelldatei.
Wenn Sie einen Pfad für eine Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in dieser Datei.
Wenn Sie eine Datei angeben, die bereits vorhanden ist, und den Parameter _"Erzwingen"_ angeben, überschreibt dieses Cmdlet den Inhalt der Datei.
Wenn Sie eine Datei angeben, die bereits vorhanden ist, aber nicht "Erzwingen" _angeben,_ nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.
Wenn Sie einen Pfad eines Ordners angeben, der nicht vorhanden ist, nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.

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
Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.

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
Dieses Cmdlet lädt in eine Datei in der Dateifreigabe hoch, die dieser Parameter angibt.
Verwenden Sie zum Abrufen **eines CloudFileShare-Objekts** das Get-AzStorageShare Cmdlet.
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
Dieses Cmdlet lädt in eine Datei in der Dateifreigabe hoch, die dieser Parameter angibt.

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

### -Source
Gibt die Quelldatei an, die von diesem Cmdlet hochgeladen wird.
Wenn Sie eine Datei angeben, die nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Remove-AzStorageDirectory](./Remove-AzStorageDirectory.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)

[Get-AzStorageFileContent](./Get-AzStorageFileContent.md)
