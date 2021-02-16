---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165705"
---
# New-AzStorageBlobRangeToRestore

## SYNOPSIS
Erstellt ein Blob Range-Objekt, um ein Speicherkonto wiederherzustellen.

## SYNTAX

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzStorageBlobRangeToRestore"** erstellt ein Blob Range-Objekt, das in Restore-AzStorageBlobRange verwendet werden kann.

## BEISPIELE

### Beispiel 1: Erstellt einen blob-Bereich, der wiederhergestellt werden soll
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Mit diesem Befehl wird ein blob-Bereich erstellt, der wiederhergestellt werden soll, der mit "container1/blob1" (include) beginnt und mit "container2/blob2" endet (ausschluss).

### Beispiel 2: Erstellt einen BLOB-Bereich, der vom ersten BLOB in alphabetischer Reihenfolge zu einem bestimmten BLOB wiederhergestellt wird (ausschließen)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Dieser Befehl erstellt einen BLOB-Bereich, der vom ersten BLOB alphabetischer Reihenfolge bis zu einem bestimmten BLOB Container2/BLOB2 wiederhergestellt wird (ausschließen)

### Beispiel 3: Erstellt einen BLOB-Bereich, der von einem bestimmten BLOB (include) zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Mit diesem Befehl wird ein BLOB-Bereich erstellt, der von einem bestimmten BLOB-Container1/BLOB1 (include) bis zum letzten BLOB in alphabetischer Reihenfolge wiederhergestellt wird.

### Beispiel 4: Erstellt einen BLOB-Bereich, der alle Blobs wiederhergestellt.
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Mit diesem Befehl wird ein BLOB-Bereich erstellt, mit dem alle BLOB wiederhergestellt werden.

## PARAMETERS

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

### -EndRange
Geben Sie den Endbereich für die Blobwiederherstellung an.
Der Endbereich wird in "Blobs wiederherstellen" ausgeschlossen.
Legen Sie die Strng als leere Strng für die Wiederherstellung am Ende des Felds ein.

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
Geben Sie den Startbereich für die Blobwiederherstellung an.
Der Startbereich wird in "Blobs wiederherstellen" eingeschlossen.
Legen Sie die Zeichenfolge als leere Zeichenfolge so ein, dass sie von Anfang an wiederhergestellt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
