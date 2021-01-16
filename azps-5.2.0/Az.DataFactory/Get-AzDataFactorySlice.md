---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307451"
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
Das **Cmdlet "Get-AzDataFactoryS slice"** ruft Datenschnitte für ein Dataset in Azure Data Factory ab.
Geben Sie eine Anfangszeit und eine Endzeit an, um einen Bereich von Datenschnitten zum Anzeigen zu definieren.
Der Status eines Datenschnitts ist einer der folgenden Werte: 
- PendingExecution.
Die Datenverarbeitung wurde nicht gestartet. 
- InProgress.
Die Datenverarbeitung wird ausgeführt. 
- "Bereit".
Die Datenverarbeitung ist abgeschlossen.
Das Datenschnitt kann von abhängigen Segmenten verwendet werden. 
- Fehler.
Die Ausführung, die das Segment erzeugt, ist fehlgeschlagen. 
- Überspringen.
Data Factory überspringt die Verarbeitung des Datenschnitts. 
- Wiederholen Sie den Vorgang.
Data Factory führt die Ausführung aus, die das Segment erzeugt. 
- "Timed Out" aus. Die Datenverarbeitung ist nicht mehr Zeit. 
- PendingValidation.
Das Datendatenschnitt wartet auf die Überprüfung, bevor es verarbeitet wird. 
- Wiederholen Sie die Überprüfung.
Data Factory rechiert die Überprüfung des Datenschnitts. 
- Fehler bei der Überprüfung.
Fehler bei der Überprüfung des Segments.
Für jedes der Segmente werden weitere Informationen zur Ausführung des Segments mithilfe des cmdlets Get-AzDataFactoryRun segmentiert.

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

Dieser Befehl ruft alle Datenschnitte für das Dataset mit dem Namen "WikiAggregatedData" in der Daten factory namens WikiADF ab.
Der Befehl ruft Segmente ab, die nach der vom Parameter "StartDateTime" angegebenen Zeit erstellt werden.
Der folgende Beispielcode legt die Verfügbarkeit für dieses Dataset stündlich in der JavaScript Object Notation (JSON)-Datei fest.
availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready, and others are PendingExecution.
Fertige Segmente wurden bereits ausgeführt.
Die ausstehenden Segmente werden am Ende jeder Stunde in dem vom cmdlet Set-AzDataFactoryPipelineActivePeriod festgelegten Intervall ausgeführt.
In diesem Beispiel haben sowohl Start- als auch Endzeiträume für die Pipeline und das Segment einen Wert von einem Tag (24 Stunden).

### Beispiel 2

Ruft Datenschnitte für ein Dataset in Azure Data Factory ab. (automatisch generiert)

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## PARAMETERS

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.
Dieses Cmdlet ruft Segmente ab, die zu der von diesem Parameter angegebenen Daten factory gehören.

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
Dieses Cmdlet ruft Segmente ab, die zu der von diesem Parameter angegebenen Daten factory gehören.

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
Gibt das Ende eines Zeitraums als **"DateTime"-Objekt** an.
Dieses Cmdlet ruft Segmente ab, die vor dem von diesem Parameter angegebenen Zeitpunkt erstellt wurden.
Weitere Informationen zu **"DateTime"-Objekten** erhalten Sie, wenn Sie `Get-Help Get-Date` ".
*EndDateTime* muss im ISO8601-Format angegeben werden, wie in den folgenden Beispielen: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) Der Standard-Zeitzonen-Designator ist UTC.

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

### -StartDateTime
Gibt den Anfang eines Zeitraums als **"DateTime"-Objekt** an.
Dieses Cmdlet ruft Segmente nach dem von diesem Parameter angegebenen Zeitpunkt ab.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSDataSverbinder

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[Set-AzDataFactorySstatus](./Set-AzDataFactorySliceStatus.md)

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)


