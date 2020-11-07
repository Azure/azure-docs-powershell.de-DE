---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663960"
---
# Get-AzureRmDataLakeStoreItemContent

## Synopsis
Ruft den Inhalt einer Datei im Data Lake Store ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Vorschau des Dateiinhalts (Standard)
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Vorschau der Datei Zeilen vom Anfang der Datei
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### Vorschau der Datei Zeilen vom Ende der Datei
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDataLakeStoreItemContent** " Ruft den Inhalt einer Datei im Data Lake Store ab.

## Beispiele

### Beispiel 1: Abrufen des Inhalts einer Datei
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

Dieser Befehl ruft den Inhalt der Datei MyFile.txt im ContosoADL-Konto ab.

### Beispiel 2: Abrufen der ersten beiden Zeilen einer Datei
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

Dieser Befehl ruft die ersten beiden Zeilen in der Datei MyFile.txt im ContosoADL-Konto getrennt ab.

## Parameter

### -Konto
Gibt den Namen des Data Lake Store-Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Encoding
Gibt die Codierung für das zu erstellende Element an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Unbekannten
- Zeichenfolge
- Unicode
- Byte
- BigEndianUnicode
- UTF8
- UTF7
- ASCII
- Standard
- OEM
- BigEndianUTF32

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Head
Die Anzahl der Zeilen (neue Zeile getrennt) vom Anfang der Datei bis zur Vorschau. Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Length
Gibt die Länge des abzurufenden Inhalts in Bytes an.

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Offset
Gibt die Anzahl der Bytes an, die vor dem Abrufen von Inhalten in einer Datei übersprungen werden sollen.

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Gibt den Daten See-Speicherpfad einer Datei an, beginnend mit dem Stammverzeichnis (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tail
Die Anzahl der Zeilen (neue Zeile getrennt) vom Ende der Datei bis zur Vorschau. Wenn in den ersten 4MB-Daten keine neue Zeile gefunden wird, werden nur die Daten zurückgegeben.

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Byte []
Die Bytedatenstrom Darstellung des abgerufenen Dateiinhalts.

### Zeichenfolge
Die Zeichenfolgendarstellung (in der angegebenen Codierung) des abgerufenen Dateiinhalts.

## Notizen

## Verwandte Links

