---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174005"
---
# New-AzStorageBlobRangeToRestore

## Synopsis
Erstellt ein BLOB Range-Objekt, um ein Speicherkonto wieder zu speichern.

## Syntax

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzStorageBlobRangeToRestore** erstellt ein BLOB Range-Objekt, das in Restore-AzStorageBlobRange verwendet werden kann.

## Beispiele

### Beispiel 1: erstellt einen zu wiederherzustellenden BLOB-Bereich
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Dieser Befehl erstellt einen zu wiederherzustellenden BLOB-Bereich, der bei Container1/blob1 (Include) beginnt und bei container2/blob2 (Exclude) endet.

### Beispiel 2: erstellt einen BLOB-Bereich, der aus dem ersten BLOB in alphabetischer Reihenfolge wiederhergestellt wird, bis zu einem bestimmten BLOB (ausschließen).
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Dieser Befehl erstellt einen BLOB-Bereich, der aus dem ersten BLOB in alphabetischer Reihenfolge wiederhergestellt wird, bis zu einem bestimmten BLOB-container2/blob2 (ausschließen).

### Beispiel 3: erstellt einen BLOB-Bereich, der von einem bestimmten BLOB (Include) bis zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Mit diesem Befehl wird ein BLOB-Bereich erstellt, der von einem bestimmten BLOB-Container1/blob1 (Include) zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.

### Beispiel 4: erstellt einen BLOB-Bereich, in dem alle Blobs wiederhergestellt werden.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Mit diesem Befehl wird ein BLOB-Bereich erstellt, der alle Blobs wieder herstellt.

## Parameter

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

### -EndRange
Geben Sie den Endbereich der BLOB-Wiederherstellung an.
Der Endbereich wird in BLOB-wiederherstellen ausgeschlossen.
Legen Sie Sie als leere Strng-Datei zum Ende wieder her.

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

### -StartRange
Geben Sie den Startbereich für die BLOB-Wiederherstellung an.
Der Start Bereich wird in die BLOB-Wiederherstellung aufgenommen.
Als leere Zeichenfolge zum Wiederherstellen von Anfang an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange

## Notizen

## Verwandte Links
