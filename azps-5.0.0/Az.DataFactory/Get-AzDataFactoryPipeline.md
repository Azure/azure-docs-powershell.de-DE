---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298581"
---
# Get-AzDataFactoryPipeline

## Synopsis
Ruft Informationen zu Pipelines in Azure Data Factory ab.

## Syntax

### ByFactoryName (Standard)
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzDataFactoryPipeline** " Ruft Informationen zu Pipelines in Azure Data Factory ab.
Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Data Factory ab.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Pipelines
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Dieser Befehl ruft Informationen zu allen Pipelines in der Data Factory mit dem Namen WikiADF ab.
Sie können entweder einen der folgenden Beispielbefehle ausführen.
Bei der zweiten wird ein **DataFactory** -Objekt als Parameter verwendet.

### Beispiel 2: Abrufen von Informationen zu einer bestimmten Pipeline
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Dieser Befehl ruft Informationen zur Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab.
Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators an das Format-List-Cmdlet.
Dieses Cmdlet formatiert die Ergebnisse.
Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Format-List` .

### Beispiel 3: Abrufen der Eigenschaften für eine bestimmte Pipeline
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Eigenschaften** Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.

### Beispiel 4: Abrufen der Aktivitäten für eine bestimmte Pipeline
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Aktivitäten** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.

### Beispiel 5: Abrufen der Laufzeitinformationen für eine bestimmte Pipeline
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **RuntimeInfo** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.

### Beispiel 6: Abrufen von Informationen zu Eingaben für die erste Aktivität
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Data Factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punktnotation, um die **Aktivitäten** -Eigenschaft anzuzeigen, die dieser Pipeline zugeordnet ist.
Der Befehl zeigt die **Inputs** -Eigenschaft des ersten Elements des **Activities** -Arrays mithilfe von **Format-List** an.

## Parameter

### -DataFactory
Gibt ein **PSDataFactory** -Objekt an.
Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.

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
Dieses Cmdlet ruft Pipelines ab, die zu der Data Factory gehören, die dieser Parameter angibt.

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

### -Name
Gibt den Namen der Pipeline an, über die Informationen abgerufen werden sollen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.
Dieses Cmdlet ruft Pipelines ab, die zu der Gruppe gehören, die dieser Parameter angibt.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## Ausgaben

### Microsoft. Azure. Commands. datafactoring. Models. PSPipeline

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys

## Verwandte Links

[Neu – AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Lebenslauf-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Satz-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


