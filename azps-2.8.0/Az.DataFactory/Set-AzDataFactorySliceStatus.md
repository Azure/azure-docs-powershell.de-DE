---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: a7418dd1e0570d4e92310371e658dd130b36bc44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651680"
---
# Set-AzDataFactorySliceStatus

## Synopsis
Legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.

## Syntax

### ByFactoryName (Standard)
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzDataFactorySliceStatus** " legt den Status von Segmenten für ein Dataset in Azure Data Factory fest.

## Beispiele

### Beispiel 1: Einstellen des Status aller Segmente
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

Mit diesem Befehl wird der Status aller Segmente für das DataSet mit dem Namen DAWikiAggregatedData auf Waiting in der Data Factory mit dem Namen WikiADF festgelegt.
Der *UpdateType* -Parameter hat den Wert UpstreamInPipeline, und der Befehl legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest.
Abhängige Datasets werden als Eingabedatasets für Aktivitäten in der Pipeline verwendet.
Dieser Befehl gibt den Wert $true zurück.

## Parameter

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.
Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.

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
Dieses Cmdlet ändert den Status von Segmenten, die zu der Data Factory gehören, die dieser Parameter angibt.

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
Gibt den Namen des Datasets an, für das dieses Cmdlet Slices ändert.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enddatum
Gibt das Ende eines Zeitraums als **DateTime** -Objekt an.
Dieses Mal ist das Ende eines Datensegments.
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
Dieses Cmdlet ändert den Status von Segmenten, die zu der Gruppe gehören, die dieser Parameter angibt.

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
Dieser Zeitpunkt ist der Anfang eines Datensegments.

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

### -Status
Gibt einen Status an, der dem Datenslice zugewiesen werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Warten.
Der Datenslice wartet vor der Verarbeitung auf die Validierung anhand von Validierungsrichtlinien. 
- Bereit.
Die Datenverarbeitung ist abgeschlossen, und der Datenslice ist fertig.
- InProgress.
Die Datenverarbeitung ist in Bearbeitung. 
- Fehlgeschlagen.
Fehler bei der Datenverarbeitung.
- Übersprungen.
Die Verarbeitung des Datensegments wurde übersprungen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateType
Gibt den Typ des Updates für das Segment an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Einzelnen.
Legt den Status der einzelnen Segmente für das Dataset im angegebenen Zeitbereich fest. 
- UpstreamInPipeline.
Legt den Status jedes Segments für das DataSet und alle abhängigen Datasets fest, die als Eingabedatasets für Aktivitäten in der Pipeline verwendet werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
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

### System. Boolean

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Get-AzDataFactorySlice](./Get-AzDataFactorySlice.md)


