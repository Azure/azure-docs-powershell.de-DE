---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166804"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Deaktiviert die Aufgabenplanung für den angegebenen Rechenknoten.

## SYNTAX

### ID (Standard)
```
Disable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String>
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Disable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>]
 [-DisableSchedulingOption <DisableComputeNodeSchedulingOption>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Disable-AzBatchComputeNodeScheduling"** deaktiviert die Aufgabenplanung für den angegebenen Rechenknoten.
Ein Rechenknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.
Wenn Sie die Aufgabenplanung für einen Rechenknoten deaktivieren, haben Sie auch die Möglichkeit zu bestimmen, was mit Aufträgen zu tun ist, die sich aktuell in der Aufgabenwarteschlange des Knotens befinden.
**Disable-AzBatchComputeNodeScheduling** ermöglicht Folgendes: 
- Beenden Sie die Aufgaben, und setzen Sie sie wieder in die Auftragswarteschlange ein.
Dadurch können diese Aufgaben auf einem anderen Rechenknoten neu geplant werden. 
- Beenden Sie die Aufgaben, und entfernen Sie sie aus der Auftragswarteschlange.
Auf diese Weise beendete Vorgänge werden nicht neu geplant. 
- Warten Sie, bis alle derzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung für den Rechenknoten. 
- Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Datenaufbewahrungszeiträume ablaufen, und deaktivieren Sie dann die Aufgabenplanung für den Rechenknoten.

## BEISPIELE

### Beispiel 1: Deaktivieren der Vorgangsplanung für einen Rechenknoten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Mit diesen Befehlen wird der Aufgabenzeitplan auf dem berechneten Knoten "tvm-1783593343_34-20151117t222514z" deaktiviert.
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto "contosobatchaccount".
Dieser Objektverweis wird in einer Variablen namens "$context.
Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Disable-AzBatchComputeNodeScheduling",** um eine Verbindung mit dem Pool "myPool" herzustellen und die Aufgabenplanung auf node tvm-1783593343_34-20151117t222514z zu deaktivieren.
Da der *Parameter "DisableComputeNodeSchedulingOptions"* nicht enthalten war, werden alle derzeit auf dem Rechenknoten ausgeführten Aufgaben neu ausgeführt.

### Beispiel 2: Deaktivieren der Vorgangsplanung für alle Rechenknoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Mit diesen Befehlen wird die Aufgabenplanung für alle Computerknoten im Batchpoolpool06 deaktiviert.
Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto "contosobatchaccount".
Dieser Objektverweis wird in einer Variablen namens "$context.
Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **"Get-AzBatchComputeNode",** um eine Sammlung aller In Pool06 gefundenen Berechnungsknoten zurückzukehren.
Diese Sammlung wird dann an das Cmdlet **"Disable-AzBatchComputeNodeScheduling"** weiterverteilt, um die Aufgabenplanung für jeden Rechenknoten in der Sammlung zu deaktivieren.
Da der *Parameter "DisableComputeNodeSchedulingOptions"* nicht enthalten war, werden die derzeit für die Berechnungsknoten ausgeführten Aufgaben neu ausgeführt.

## PARAMETERS

### -BatchContext
Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.
Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet. Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten. Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet. Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.

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

### -ComputeNode
Gibt einen Objektverweis auf den Rechenknoten an, in dem die Aufgabenplanung deaktiviert ist.
Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchComputeNode erstellt und das zurückgegebene Rechenknotenobjekt in einer Variablen gespeichert.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
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

### -DisableSchedulingOption
Gibt an, wie dieses Cmdlet mit aufgaben behandelt wird, die derzeit auf dem Computerknoten ausgeführt werden, in dem die Planung deaktiviert ist.
Die zulässigen Werte für diesen Parameter sind:
- Requeue.
Aufgaben werden sofort beendet und an die Auftragswarteschlange zurückgegeben.
Dadurch können die Aufgaben auf einem anderen Rechenknoten neu geplant werden.
Dies ist der Standardwert. 
- "Beenden" aus.
Aufgaben werden sofort beendet und aus der Auftragswarteschlange entfernt.
Diese Vorgänge werden nicht neu geplant. 
- TaskCompletion.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Aufgabenplanung auf dem Rechenknoten deaktiviert wird.
Für diesen Knoten werden keine neuen Aufgaben geplant. 
- RetainedData.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung für den Rechenknoten deaktiviert wird.
Für diesen Knoten werden keine neuen Aufgaben geplant.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.DisableComputeNodeSchedulingOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID des Rechenknotens an, für den die Aufgabenplanung deaktiviert ist.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Gibt die ID des Batchpools an, der den Rechenknoten enthält, für den die Aufgabenplanung deaktiviert ist.
Wenn Sie den Parameter *"PoolId"* verwenden, verwenden Sie den Parameter *"ComputeNode"* nicht in demselben Befehl.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### System.Void

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


