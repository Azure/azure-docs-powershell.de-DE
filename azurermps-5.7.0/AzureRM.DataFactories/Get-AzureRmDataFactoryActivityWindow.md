---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 33deeafce23267d1b2dbc594251bc58de1914280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476858"
---
# Get-AzureRmDataFactoryActivityWindow

## Synopsis
Ruft Informationen zu Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByFactoryName (Standard)
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmDataFactoryActivityWindow** " Ruft Informationen zu den Aktivitäts Fenstern ab, die einer Data Factory zugeordnet sind.

## Beispiele

### Beispiel 1: Abrufen von Aktivitäts Fenstern, die einer Data Factory zugeordnet sind
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

Dieser Befehl ruft Informationen zu allen Aktivitäts Fenstern ab, die der Data Factory mit dem Namen WikiADF zugeordnet sind.

## Parameter

### -ActivityName
Gibt den Namen der Aktivität an.
Dieses Cmdlet ruft Aktivitätsfenster für die Aktivität ab, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactory
Gibt ein von einem Cmdlet zurückgegebenes **PSDataFactory** -Objekt an.
Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Datafactoryname
Gibt den Namen der Data Factory an.
Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Data Factory gehören, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataSetName
Gibt den Namen des Datasets an.
Dieses Cmdlet ruft Aktivitätsfenster ab, die zu dem DataSet gehören, das dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Filter
Gibt das Aktivitätsfenster an, das mithilfe der Azure-Suchfilter Grammatik ausgedrückt wird.
Informationen zur Grammatik finden Sie unter Syntax für OData-Ausdrücke für Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.
Die Liste der Aktivitätsfenster wird nach der Suchzeichenfolge gefiltert, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
Gibt an, dass die Antwort durch einen der Parameter der Aktivitätsfenster Liste angeordnet werden soll.
Hierbei handelt es sich um eine Liste mit durch Kommas getrennten Eigenschaften.
Beispiel: WindowStart, PercentComplete.

Standardmäßig ist die Reihenfolge in aufsteigender Reihenfolge (ASC).
Geben Sie DESC an, wenn Sie die Liste in absteigender Reihenfolge sortieren möchten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pipelinename
Gibt den Namen der Pipeline an.
Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Pipeline gehören, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.
Dieses Cmdlet ruft Aktivitätsfenster ab, die zu der Ressourcengruppe gehören, die dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunEnd
Gibt die Endzeit des ausgeführten Aktivitäts Fensters an.
Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunStart
Gibt die Startzeit des ausgeführten Aktivitäts Fensters an.
Dieses Cmdlet ruft Aktivitätsfenster ab, deren Ausführungszeiten zwischen *RunStart* -und *RunEnd* -Zeiten liegen.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Top
Gibt die maximale Anzahl von Aktivitäts Fenstern an, die dieses Cmdlet zurückgibt.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowEnd
Gibt das Fenster Endzeit des Vorgangs an.
Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowStart
Gibt das Fenster Startzeit der Aktivität an.
Dieses Cmdlet ruft Aktivitätsfenster ab, deren Zeiten zwischen *WindowStart* -und *WindowEnd* -Zeiten liegen.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowState
Gibt den Zustand des Aktivitäts Fensters an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Keine
- Warten
- InProgress
- Bereit
- Fehlgeschlagen
- Übersprungen

Dieses Cmdlet ruft Aktivitätsfenster ab, die sich in dem Zustand befinden, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowSubstate
Gibt den unter Status des Aktivitäts Fensters an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Storniert
- TimedOut
- Überprüfen

Dieses Cmdlet ruft Aktivitätsfenster ab, die sich im unter Zustand befinden, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSActivyWindow, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## Notizen

## Verwandte Links

[Azure Data Factories-Cmdlets](./AzureRM.DataFactories.md)


