---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458091"
---
# Get-AzDataLakeStoreDeletedItem

## SYNOPSIS
Sucht nach gelöschten Einträgen im Papierkorb, die dem Filter entsprechen.

## SYNTAX

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzDataLakeStoreDeletedItem"** durchsucht die gelöschten Dateien oder Ordner im Data Lake Store, die dem angegebenen Filter entsprechen.
Es zeigt die folgenden Attribute der gelöschten Elemente an– "OriginalPath", "TrashDirPath", "Type", "CreationTime".
Dies kann ein Vorgang mit langer Dauer sein, da er möglicherweise Millionen von Dateien im Papierkorb durchsuchen muss und als Auftrag ausgeführt werden kann.
Vorsicht: Das Wiederherstellen von Dateien ist ein Vorgang nach bestem Aufwand. Es gibt keine Garantie dafür, dass eine Datei nach dem Löschen wiederhergestellt werden kann. Die Verwendung dieser API wird über Whitelisting aktiviert. Wenn Ihr ADL-Konto nicht in der Whiteliste aufgeführt ist, wird mit dieser API die Ausnahme "Nicht implementiert" ausgelöst. Für weitere Informationen und Unterstützung wenden Sie sich bitte an den Microsoft-Support.

## BEISPIELE

### Beispiel: Details zu einer Datei aus dem Data Lake Store
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## PARAMETERS

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

### -Count
Gibt die Anzahl der Ergebnisse an, die der Benutzer suchen möchte. Die Abfrage wird ausgeführt, bis sie die Ergebnisse für "Anzahl" findet, oder sie durchsucht den gesamten Papierkorb, ganz gleich, was zuerst geschieht.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Filter
Gibt die Suchabfrage an. Ein spezifischerer Wert führt zu relevanteren Ergebnissen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### System.Collections.generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem>

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Restore-AzDataLakeStoreDeletedItem](./Restore-AzDataLakeStoreDeletedItem.md)