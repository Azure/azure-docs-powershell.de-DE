---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: 497899400c05697fb9b273a89743172b672e4892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930272"
---
# Get-AzDataFactorySlice

## SYNOPSIS
Ruft Datenschnitte für ein Dataset in Azure Data Factory ab.

## SYNTAX

### ByFactoryName (Standard)
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzDataFactorySlice-Cmdlet** ruft Datenschnitte für ein Dataset in Azure Data Factory ab.
Geben Sie eine Startzeit und eine Endzeit an, um einen Datenbereich zu definieren, der angezeigt werden soll.
Der Status eines Datenschnitts ist einer der folgenden Werte: 
- PendingExecution.
Die Datenverarbeitung wurde noch nicht gestartet. 
- InProgress.
Die Datenverarbeitung wird ausgeführt. 
- Fertig.
Die Datenverarbeitung ist abgeschlossen.
Das Datendatenschnitt ist für abhängige Segmente bereit, um es zu nutzen. 
- Fehler.
Die Ausführung, die das Segment erzeugt, ist fehlgeschlagen. 
- Überspringen.
Data Factory überspringt die Verarbeitung des Datenschnitts. 
- Wiederholen Sie den Vorgang.
Data Factory führt die Ausführung aus, mit der das Segment erzeugt wird. 
- Timed Out. Die Datenverarbeitung hat ein Zeit-Out. 
- PendingValidation.
Das Datendatenschnitt wartet auf die Überprüfung, bevor es verarbeitet wird. 
- Wiederholen Sie die Überprüfung.
Data Factory gibt die Überprüfung des Datenschnitts zurück. 
- Fehlgeschlagene Überprüfung.
Die Überprüfung des Datenschnitts ist fehlgeschlagen.
Für jedes der Segmente können Sie weitere Informationen zum Ausführen sehen, mit dem das Segment mithilfe des cmdlets Get-AzDataFactoryRun wird.

## BEISPIELE

### Beispiel 1: Datenschnitte für ein Dataset erhalten
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

Dieser Befehl ruft alle Datenschnitte für das Dataset mit dem Namen WikiAggregatedData in der Daten factory mit dem Namen WikiADF ab.
Der Befehl ruft Segmente ab, die nach der vom Parameter StartDateTime angegebenen Zeit erstellt werden.
Der folgende Beispielcode legt die Verfügbarkeit für dieses Dataset stündlich in der Datei JavaScript Object Notation (JSON) fest.
Verfügbarkeit: { Zeitraum: "Stunde", ZeitraumMultiplier: 1 } Einige der Ergebnisse sind Bereit, und andere sind PendingExecution.
Fertige Segmente wurden bereits ausgeführt.
Die ausstehenden Segmente warten darauf, am Ende jeder Stunde in dem Intervall ausgeführt zu werden, das vom cmdlet Set-AzDataFactoryPipelineActivePeriod angegeben wird.
In diesem Beispiel haben sowohl Start- als auch Endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).

### Beispiel 2

Ruft Datenschnitte für ein Dataset in Azure Data Factory ab. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETER

### -DataFactory
Gibt ein **PSDataFactory-Objekt** an.
Dieses Cmdlet ruft Segmente ab, die zur Daten factory gehören, die dieser Parameter angibt.

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

### -DataFactoryName
Gibt den Namen einer Daten factory an.
Dieses Cmdlet ruft Segmente ab, die zur Daten factory gehören, die dieser Parameter angibt.

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

### -DatasetName
Gibt den Namen des Datasets an, für das dieses Cmdlet Segmente erhält.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -EndDateTime
Gibt das Ende eines Zeitraums als **DateTime-Objekt** an.
Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter angegebenen Zeitpunkt erstellt werden.
Weitere Informationen zu **DateTime-Objekten** finden Sie unter `Get-Help Get-Date` .
*EndDateTime* muss wie in den folgenden Beispielen im ISO8601-Format angegeben werden: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standardmäßige Zeitzonenentwurfer ist UTC.

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
Dieses Cmdlet ruft Segmente ab, die zu der Gruppe gehören, die von diesem Parameter angegeben wird.

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

### -StartDateTime
Gibt den Anfang eines Zeitraums als **DateTime-Objekt** an.
Dieses Cmdlet ruft Segmente ab, die nach der von diesem Parameter angegebenen Zeit erstellt werden.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice

## NOTIZEN
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory

## VERWANDTE LINKS

[Set-AzDataFactorySliceStatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


