---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 87e8792697093182d3ccd36d75ac072239f76e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931600"
---
# Remove-AzStorageDirectory

## SYNOPSIS
Löscht ein Verzeichnis.

## SYNTAX

### ShareName (Standard)
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Freigeben
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Verzeichnis
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Remove-AzStorageDirectory** löscht ein Verzeichnis.

## BEISPIELE

### Beispiel 1: Löschen eines Ordners
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

Mit diesem Befehl wird der Ordner ContosoWorkingFolder aus der Dateifreigabe namens ContosoShare06 gelöscht.

## PARAMETER

### -ClientTimeoutPerRequest
Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.
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
Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.
Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.
Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.
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
Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)

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
Dieses Cmdlet entfernt den Ordner, den dieser Parameter angibt.
Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.
Sie können auch das **Get-AzStorageFile-Cmdlet** verwenden, um ein Verzeichnis zu erhalten.

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

### -PassThru
Gibt an, dass, wenn dieses Cmdlet erfolgreich ist, ein Wert von $True.
Wenn Sie diesen Parameter angeben und das Cmdlet aufgrund eines  unangemessenen Werts für den Parameter Pfad nicht erfolgreich ist, gibt das Cmdlet einen Fehler zurück.
Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet keinen Wert zurück.

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
Gibt den Pfad eines Ordners an.
Wenn der ordner, den dieser Parameter angibt, leer ist, löscht dieses Cmdlet diesen Ordner.
Wenn der Ordner nicht leer ist, nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.

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
Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.
Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.
Dieses Objekt enthält den Speicherkontext.
Wenn Sie diesen Parameter angeben, geben Sie den Parameter *Kontext nicht* an.

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
Dieses Cmdlet entfernt einen Ordner unter der Dateifreigabe, die dieser Parameter angibt.

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

### -Bestätigen
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

### -WhatIf
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Storage.File.CloudFileShare

### Microsoft.Azure.Storage.File.CloudFileDirectory

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory

## NOTIZEN

## VERWANDTE LINKS

[Get-AzStorageShare](./Get-AzStorageShare.md)

[New-AzStorageContext](./New-AzStorageContext.md)

[New-AzStorageDirectory](./New-AzStorageDirectory.md)
