---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944560"
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
Das **Cmdlet New-AzStorageBlobRangeToRestore** erstellt ein Blobbereichsobjekt, das in Restore-AzStorageBlobRange verwendet werden kann.

## BEISPIELE

### Beispiel 1: Erstellt einen Blobbereich, der wiederhergestellt werden soll
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

Mit diesem Befehl wird ein wiederherstellende Blobbereich erstellt, der bei container1/blob1 (include) beginnt und bei container2/blob2 (exclude) endet.

### Beispiel 2: Erstellt einen Blobbereich, der vom ersten Blob in alphabetischer Reihenfolge in einem bestimmten Blob wiederhergestellt wird (ausschließen)
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

Mit diesem Befehl wird ein Blobbereich erstellt, der aus dem ersten Blob alphabetischer Reihenfolge in einen bestimmten Blobcontainer2/Blob2 (ausschluss) wiederhergestellt wird.

### Beispiel 3: Erstellt einen Blobbereich, der von einem bestimmten Blob (include) zum letzten Blob in alphabetischer Reihenfolge wiederhergestellt wird
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

Mit diesem Befehl wird ein Blobbereich erstellt, der aus einem bestimmten Blobcontainer1/Blob1 (include) bis zum letzten Blob in alphabetischer Reihenfolge wiederhergestellt wird.

### Beispiel 4: Erstellt einen Blobbereich, der alle Blobs wiederherstellen wird
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

Mit diesem Befehl wird ein Blobbereich erstellt, der alle Blobs wiederherstellen wird.

## PARAMETER

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
Der Endbereich wird in Wiederherstellenblobs ausgeschlossen.
Legen Sie sie als leere Strg-Strg-Wiederherstellen bis zum Ende des Wiederherstellens ein.

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
Der Startbereich wird in Wiederherstellen-Blobs einbezogen.
Legen Sie die Zeichenfolge als leere Zeichenfolge für die Wiederherstellung von Anfang an ein.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange

## NOTIZEN

## VERWANDTE LINKS
