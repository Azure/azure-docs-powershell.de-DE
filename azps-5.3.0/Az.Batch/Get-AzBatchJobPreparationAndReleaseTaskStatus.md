---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471183"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## SYNOPSIS
Ruft die Batchauftragsvorbereitung ab und gibt den Vorgangsstatus frei.

## SYNTAX

### ID (Standard)
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzBatchJobPreparationAndReleaseTaskStatus"** ruft den Vorgangsvorbereitungs- und Freigabestatus von Azure Batch für einen Stapelauftrag ab.
Sie müssen den Parameter *"Id"* oder eine **"PSCloudJob"-Instanz** für dieses Cmdlet angeben.

## BEISPIELE

### Beispiel 1: Vorbereiten und Veröffentlichungsstatus eines Auftrags
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Dieser Befehl ruft die Auftragsvorbereitung und den Vorgangsstatus für "Test" ab.
Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.

### Beispiel 2: Vorbereiten eines Auftrags und Freigabestatus eines Auftrags mit angegebener Option "Filtern und auswählen"
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Dieser Befehl ruft den Vorgangsvorbereitungs- und Freigabestatus für den Auftrag "Test" für Knoten "tvm-2316545714_1-20170613t201733z" ab und verwendet die Select-Klausel, um nur die Informationen "JobPreparationTaskExecutionInformation" zurückzukehren.

## PARAMETERS

### -BatchContext
Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batchdienst verwendet wird.
Verwenden Sie Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Expand
Gibt eine Open Data Protocol (OData)-Erweiterungsklausel an.
Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der erhaltenen Hauptentität zu erhalten.

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

### -Filter
Gibt eine OData-Filterklausel an.
Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Arbeitsvorbereitungs- und Freigabestatus für den Auftrag zurück.

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

### -ID
Gibt die ID des Auftrags an, dessen Vorbereitungs- und Freigabeaufgaben abgerufen werden sollen.
Sie können keine Platzhalterzeichen angeben.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Gibt ein **PSCloudJob-Objekt** an, das den Auftrag darstellt, aus dem der Vorbereitungs- und Freigabestatus der Aufgabe zu erhalten ist.
Um ein **"PSCloudJob"-Objekt** zu erhalten, verwenden Sie das Get-AzBatchJob-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
Gibt die maximale Anzahl zurückzukehrenden Aufträge für die Vorbereitung und freigaben des Vorgangs an.
Wenn Sie einen Wert von null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.
Der Standardwert ist 1000.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Select
Gibt eine OData-Auswahlklausel an.
Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSJobPreparationAndReleaseTaskExecutionInformation

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure-Batch-Cmdlets](/powershell/module/Az.Batch/)
