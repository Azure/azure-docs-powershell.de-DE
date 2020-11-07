---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 50942dfc9b31b96a796b0a77df8b1ffc1a4cbd36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664871"
---
# Get-AzureRmDataFactorySlice

## Synopsis
Ruft Datensegmente für ein Dataset in Azure Data Factory ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDataFactorySlice** " ruft Datensegmente für ein Dataset in Azure Data Factory ab.
Geben Sie eine Startzeit und eine Endzeit an, um einen Bereich von Datensegmenten zu definieren, die angezeigt werden sollen.
Der Status eines Datensegments entspricht einem der folgenden Werte: 
- PendingExecution.
Die Datenverarbeitung wurde nicht gestartet. 
- InProgress.
Die Datenverarbeitung wird ausgeführt. 
- Bereit.
Die Datenverarbeitung ist abgeschlossen.
Der Datenslice ist für abhängige Slices bereit, um ihn zu verwenden. 
- Fehlgeschlagen.
Fehler beim Ausführen des Segments. 
- Skip.
Data Factory überspringt die Verarbeitung des Segments. 
- Wiederholen.
Data Factory versucht die Ausführung, die das Segment produziert, erneut. 
- Timeout. Die Datenverarbeitung hat ein Zeitlimit überschritten. 
- PendingValidation.
Datenslice wartet auf die Validierung, bevor Sie verarbeitet wird. 
- Überprüfung erneut versuchen.
Data Factory versucht erneut, die Validierung des Segments zu überprüfen. 
- Fehler bei der Überprüfung.
Fehler bei der Überprüfung des Segments.
Für jedes der Segmente können Sie mithilfe des Get-AzureRmDataFactoryRun-Cmdlets Weitere Informationen zur Ausführung des Segments anzeigen.

## Beispiele

### Beispiel 1: Abrufen von Datensegmenten für ein DataSet
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

Dieser Befehl ruft alle Datensegmente für das DataSet mit dem Namen WikiAggregatedData in der Data Factory mit dem Namen WikiADF ab.
Der Befehl ruft die Segmente ab, die nach dem Zeitpunkt erstellt wurden, an dem der Parameter StartDate Time angegeben ist.
Im folgenden Beispielcode wird die Verfügbarkeit für dieses DataSet stündlich in der JSON-Datei (JavaScript Object Notation) festgelegt.
Verfügbarkeit: {period: "Hour", periodMultiplier: 1} einige Ergebnisse sind bereit, andere sind PendingExecution.
Fertige Slices wurden bereits ausgeführt.
Die ausstehenden Segmente warten auf die Ausführung am Ende jeder Stunde in dem Intervall, das das Set-AzureRmDataFactoryPipelineActivePeriod-Cmdlet angibt.
In diesem Beispiel haben Start-und endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).

## Parameter

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.
Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Gibt den Namen einer Data Factory an.
Dieses Cmdlet ruft Segmente ab, die zu der Data Factory gehören, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataSetName
Gibt den Namen des Datasets an, für das dieses Cmdlet Slices erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Enddatum
Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.
Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.
Wenn Sie weitere Informationen zu **DateTime** -Objekten wünschen, geben Sie `Get-Help Get-Date` .
*Enddatum* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00-08:00 (Pazifik-Standardzeit) der standardmäßige Zeitzonenbezeichner ist UTC.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ruft Segmente ab, die zu der Gruppe gehören, die dieser Parameter angibt.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startdatum
Gibt den Anfang eines Zeitraums als **DateTime** -Objekt an.
Dieses Cmdlet ruft Segmente ab, die nach dem von diesem Parameter festgelegten Zeitpunkt erstellt wurden.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System. String

## Ausgaben

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Satz-AzureRmDataFactorySliceStatus](./Set-AzureRmDataFactorySliceStatus.md)

[Get-AzureRmDataFactoryRun](./Get-AzureRmDataFactoryRun.md)

[Satz-AzureRmDataFactoryPipelineActivePeriod](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


