---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 76490987a6a4d016a1d07b29cd69484305ddf849
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651561"
---
# Get-AzDataLakeStoreChildItemSummary

## Synopsis
Ruft die Zusammenfassung der Gesamtgröße, Dateien und Verzeichnisse ab, die in dem angegebenen Pfad enthalten sind.

## Syntax

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Der **Get-AzDataLakeStoreChildItemSummary** Ruft die Inhaltszusammenfassung für einen angegebenen Pfad ab. Die Gesamtzahl der Dateien, Verzeichnisse und die Gesamtgröße aller Dateien unter dem angegebenen Pfad werden rekursiv berechnet.

## Beispiele

### Beispiel 1: Abrufen der Inhaltszusammenfassung eines Ordners
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

In dieser Liste sind die Gesamtzahl der Verzeichnisse, Dateien und deren Größe unter/a aufgeführt.

## Parameter

### -Konto
Das Data Lake Store-Konto zum Ausführen des Dateisystem Vorgangs in

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

### -Parallelität
Gibt an, wie viele Dateien/Verzeichnisse parallel verarbeitet werden.
Der Standardwert wird basierend auf der Systemspezifikation als optimaler Aufwand berechnet.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Path
Der Pfad im angegebenen Data Lake-Konto, das abgerufen werden soll.
Kann eine Datei oder ein Ordner im Format "/Folder/file.txt" sein, wobei der erste "/" nach dem DNS den Stamm des Dateisystems angibt.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. Int32

## Ausgaben

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary

## Notizen

## Verwandte Links
