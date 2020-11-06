---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499873"
---
# Import-AzureRmDataLakeStoreItem

## Synopsis
Lädt eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hoch.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### NoDiagnosticLogging (Standard)
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IncludeDiagnosticLogging
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Import-AzureRmDataLakeStoreItem** " wird eine lokale Datei oder ein lokales Verzeichnis in einen Data Lake Store hochgeladen.

## Beispiele

### Beispiel 1: Hochladen einer Datei
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

Mit diesem Befehl wird die Datei SrcFile.csv hochgeladen und dem Ordner "meine Dateien" im Data Lake Store als File.csv mit einer Parallelität von 4 hinzugefügt.

## Parameter

### -Konto
Gibt den Namen des Data Lake Store-Kontos an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parallelität
Gibt die Anzahl der Dateien oder Chunks an, die parallel hochgeladen werden sollen. Der Standardwert wird basierend auf den Systemspezifikationen als optimaler Aufwand berechnet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentFileCount
Gibt die maximale Anzahl von Dateien an, die parallel für einen Ordner Upload hochgeladen werden sollen.  Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ziel
Gibt den Daten See-Speicherpfad an, zu dem eine Datei oder ein Ordner hochgeladen werden soll, beginnend mit dem Stammverzeichnis (/).

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogLevel
Gibt optional die Diagnoseprotokoll Ebene an, die zum Aufzeichnen von Ereignissen während des Datei-oder Ordner Imports verwendet wird. Standard ist der Fehler.

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogPath
Gibt den Pfad für das Diagnoseprotokoll an, in dem Ereignisse während des Datei-oder Ordner Imports aufgezeichnet werden.

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceBinary
Gibt an, dass die zu kopierenden Dateien ohne Rücksicht auf die Beibehaltung der neuen Zeile über appends kopiert werden sollen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den lokalen Pfad der Datei oder des Ordners an, die hochgeladen werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PerFileThreadCount
Gibt die maximale Anzahl von Threads an, die pro Datei verwendet werden sollen.  Der Standardwert wird als optimaler Aufwand basierend auf Ordner-und Dateigröße berechnet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekursiv
Gibt an, dass dieser Vorgang alle Elemente in allen Unterordnern hochladen soll.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resume
Gibt an, dass die zu kopierenden Dateien eine Fortsetzung eines vorherigen Uploads sind. Dies bewirkt, dass das System versucht, aus der letzten Datei, die nicht vollständig hochgeladen wurde, fortzufahren.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### Zeichenfolge
Der vollständige Pfad im Daten Lake Store-Konto für die hochgeladene Datei oder den geuploadeten Ordner.

## Notizen

## Verwandte Links

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

[Export-AzureRmDataLakeStoreItem](./Export-AzureRmDataLakeStoreItem.md)

[Teilnehmen – AzureRmDataLakeStoreItem](./Join-AzureRmDataLakeStoreItem.md)

[Verschieben-AzureRmDataLakeStoreItem](./Move-AzureRmDataLakeStoreItem.md)

[Neu – AzureRmDataLakeStoreItem](./New-AzureRmDataLakeStoreItem.md)

[Remove-AzureRmDataLakeStoreItem](./Remove-AzureRmDataLakeStoreItem.md)

[Test-AzureRmDataLakeStoreItem](./Test-AzureRmDataLakeStoreItem.md)


