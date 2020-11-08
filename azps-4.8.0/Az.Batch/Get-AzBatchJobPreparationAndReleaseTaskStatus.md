---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: ffc89f298715f9e878bb3283c99e794f92662e84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009405"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## Synopsis
Ruft die Vorbereitung des stapelverarbeitungsauftrags ab und gibt den Aufgabenstatus frei.

## Syntax

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

## Beschreibung
Das Cmdlet " **Get-AzBatchJobPreparationAndReleaseTaskStatus** " Ruft den Azure Batch Job Preparation ab und gibt den Aufgabenstatus für einen Stapelverarbeitungsauftrag frei.
Sie müssen den *ID-* Parameter oder eine **PSCloudJob** -Instanz für dieses Cmdlet angeben.

## Beispiele

### Beispiel 1: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

Dieser Befehl ruft die Job-Vorbereitung ab und gibt den Aufgabenstatus für Job "Test" frei.
Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.

### Beispiel 2: Abrufen des Auftrags Vorbereitungs-und Freigabestatus eines Auftrags mit Filter und Auswählen von "angegeben"
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

Dieser Befehl ruft den Job-Vorbereitungs-und Freigabe Aufgabenstatus für Job "Test" auf dem Knoten "TVM-2316545714_1-20170613t201733z" ab und verwendet die SELECT-Klausel, um anzugeben, dass nur die JobPreparationTaskExecutionInformation-Informationen zurückgegeben werden sollen.

## Parameter

### -Batchcontext
Die BatchAccountContext-Instanz, die bei der Interaktion mit dem Batch Dienst verwendet werden soll.
Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.

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

### – Erweitern
Gibt eine Open Data Protocol (OData) expand-Klausel an.
Geben Sie einen Wert für diesen Parameter an, um zugeordnete Entitäten der Haupt Entität abzurufen, die Sie erhalten.

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
Wenn Sie keinen Filter angeben, gibt dieses Cmdlet alle Job-Vorbereitungen zurück und gibt den Aufgabenstatus für den Auftrag frei.

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
Gibt die ID des Auftrags an, dessen Vorbereitungs-und Freigabe Aufgaben abgerufen werden sollen.
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

### -Inputobject
Gibt ein **PSCloudJob** -Objekt an, das den Auftrag darstellt, aus dem der Status der Vorbereitung und Freigabe des Vorgangs abgerufen werden soll.
Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **PSCloudJob** -Objekt zu erhalten.

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
Gibt die maximale Anzahl von Aufträgen für die Vorbereitung und Freigabe des Vorgangsstatus zurück.
Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.
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

### -Wählen Sie
Gibt eine OData-Auswahl Klausel an.
Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft.Azure.Commands.Batch. Models. PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Ausgaben

### Microsoft.Azure.Commands.Batch. Models. PSJobPreparationAndReleaseTaskExecutionInformation

## Notizen

## Verwandte Links

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
