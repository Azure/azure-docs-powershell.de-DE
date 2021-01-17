---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470593"
---
# Get-AzDataFactoryPipeline

## SYNOPSIS
Ruft Informationen zu Pipelines in Azure Data Factory ab.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Get-AzDataFactoryPipeline"** ruft Informationen zu Pipelines in Azure Data Factory ab.
Wenn Sie den Namen einer Pipeline angeben, ruft dieses Cmdlet Informationen zu dieser Pipeline ab.
Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Pipelines in der Daten factory ab.

## BEISPIELE

### Beispiel 1: Informationen zu allen Pipelines
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

Dieser Befehl ruft Informationen zu allen Pipelines in der Daten factory namens WikiADF ab.
Sie können einen der folgenden Beispielbefehle verwenden.
Im zweiten Parameter wird ein **DataFactory-Objekt** als Parameter verwendet.

### Beispiel 2: Informationen zu einer bestimmten Pipeline
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

Dieser Befehl ruft Informationen über die Pipeline mit dem Namen DPWikisample in der Daten factory namens WikiADF ab.
Der Befehl übergibt diese Informationen mithilfe des Pipelineoperators Format-List an das Format-List Cmdlet.
Mit diesem Cmdlet werden die Ergebnisse formatiert.
Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Format-List` eingeben" aus.

### Beispiel 3: Erhalten der Eigenschaften für eine bestimmte Pipeline
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory namens WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die der Pipeline zugeordnete Eigenschaft **"Properties"** (Eigenschaften) zu sehen.

### Beispiel 4: Erhalten der Aktivitäten für eine bestimmte Pipeline
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

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft **"Activities"** anzeigen.

### Beispiel 5: Erhalten der Laufzeitinformationen für eine bestimmte Pipeline
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete **RuntimeInfo-Eigenschaft** anzeigen.

### Beispiel 6: Informationen zu Eingaben für die erste Aktivität
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

Dieser Befehl ruft Informationen für die Pipeline mit dem Namen DPWikisample in der Daten factory mit dem Namen WikiADF ab und verwendet dann die standardmäßige Punkt-Notation, um die dieser Pipeline zugeordnete Eigenschaft **"Activities"** anzeigen.
Der Befehl zeigt **mithilfe** von **"Format-List"** die Eingabeeigenschaft des ersten Elements des Arrays "Aktivitäten" an. 

## PARAMETERS

### -DataFactory
Gibt ein **"PSDataFactory"-Objekt** an.
Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.

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
Dieses Cmdlet ruft Pipelines ab, die zu der von diesem Parameter angegebenen Daten factory gehören.

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

### -Name
Gibt den Namen der Pipeline an, über die Informationen angezeigt werden sollen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

## AUSGABEN

### Microsoft.Azure.Commands.DataFactories.Models.PSPipeline

## HINWEISE
* Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys

## LINKS ZU VERWANDTEN THEMEN

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Resume-AzDataFactoryPipeline](./Resume-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


