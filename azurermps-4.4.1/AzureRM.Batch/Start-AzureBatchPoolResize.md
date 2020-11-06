---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82DC8DC4-D8EC-4847-A54C-B779256FD590
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Start-AzureBatchPoolResize.md
ms.openlocfilehash: 558f8c062e60f6e9f7c18c05be8f1ccb2eafa9fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499201"
---
# Start-AzureBatchPoolResize

## Synopsis
Beginnt, die Größe eines Pools zu ändern.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Start-AzureBatchPoolResize [-Id] <String> -TargetDedicated <Int32> [-ResizeTimeout <TimeSpan>]
 [-ComputeNodeDeallocationOption <ComputeNodeDeallocationOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzureBatchPoolResize** startet eine Azure Batch-Größenänderung in einem Pool.

## Beispiele

### Beispiel 1: Ändern der Größe eines Pools auf 12 Knoten
```
PS C:\>Start-AzureBatchPoolResize -Id "ContosoPool06" -TargetDedicated 12 -BatchContext $Context
```

Mit diesem Befehl wird ein Größen Änderungsvorgang für den Pool mit der ID ContosoPool06 gestartet.
Das Ziel des Vorgangs ist 12 dedizierte Compute-Knoten.
Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.

### Beispiel 2: Ändern der Größe eines Pools mithilfe einer Option für die Freigabe
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Start-AzureBatchPoolResize -TargetDedicated 5 -ResizeTimeout ([TimeSpan]::FromHours(1)) -ComputeNodeDeallocationOption ([Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]::Terminate) -BatchContext $Context
```

Dieses Cmdlet ändert die Größe eines Pools auf fünf dedizierte Compute-Knoten.
Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzureBatchPool-Cmdlets ab.
Der Befehl übergibt das Pool-Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Mit dem Befehl wird ein Größen Änderungsvorgang für den Pool gestartet.
Das Ziel sind fünf dedizierte Compute-Knoten.
Der Befehl gibt einen Timeoutzeitraum von einer Stunde an.
Der Befehl gibt eine Option zum Aufheben der Zuweisung von Terminate an.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.

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

### -ComputeNodeDeallocationOption
Gibt eine Option für die Freigabe für die Größenänderung an, die von diesem Cmdlet gestartet wird.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID des Pools an, in dem dieses Cmdlet die Größe ändert.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResizeTimeout
Gibt einen Timeoutzeitraum für den Größen Änderungsvorgang an.
Wenn der Pool bis zu diesem Zeitpunkt nicht die Zielgröße erreicht, wird der Vorgang zum Ändern der Größe angehalten.

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDedicated
Gibt die Ziel Anzahl dedizierter Compute-Knoten an.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### BatchAccountContext
Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.

### Zeichenfolge
Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchPool](./Get-AzureBatchPool.md)

[Stopp-AzureBatchPoolResize](./Stop-AzureBatchPoolResize.md)

[Azure Batch-Cmdlets](./AzureRM.Batch.md)


