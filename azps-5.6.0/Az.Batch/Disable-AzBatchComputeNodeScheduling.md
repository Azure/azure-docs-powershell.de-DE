---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 1e7438195b0749dabc5206238a32bc00be03ea31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940595"
---
# Disable-AzBatchComputeNodeScheduling

## SYNOPSIS
Deaktiviert die Vorgangsplanung für den angegebenen Computeknoten.

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
Das **Cmdlet Disable-AzBatchComputeNodeScheduling** deaktiviert die Aufgabenplanung für den angegebenen Computeknoten.
Ein Computeknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.
Wenn Sie die Aufgabenplanung auf einem Computeknoten deaktivieren, haben Sie auch die Möglichkeit zu bestimmen, was mit Aufträgen zu tun ist, die sich derzeit in der Aufgabenwarteschlange des Knotens befinden.
**Mit Disable-AzBatchComputeNodeScheduling** können Sie folgendes tun: 
- Beenden Sie die Aufgaben, und setzen Sie sie wieder in die Auftragswarteschlange.
Dadurch können diese Aufgaben auf einem anderen Computeknoten neu geplant werden. 
- Beenden Sie die Aufgaben, und entfernen Sie sie aus der Auftragswarteschlange.
Aufgaben, die auf diese Weise beendet wurden, werden nicht neu geplant. 
- Warten Sie, bis alle derzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Computeknoten. 
- Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Aufbewahrungszeiträume ablaufen, und deaktivieren Sie dann die Aufgabenplanung auf dem Computeknoten.

## BEISPIELE

### Beispiel 1: Deaktivieren der Vorgangsplanung auf einem Computeknoten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Mit diesen Befehlen wird der Vorgangszeitplan im Computeknoten tvm-1783593343_34-20151117t222514z deaktiviert.
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $context.
Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet Disable-AzBatchComputeNodeScheduling,** um eine Verbindung mit dem Pool myPool herzustellen und die Aufgabenplanung für node tvm-1783593343_34-20151117t222514z zu deaktivieren.
Da der *Parameter DisableComputeNodeSchedulingOptions* nicht enthalten war, werden alle Aufgaben, die derzeit auf dem Computeknoten ausgeführt werden, erneut zurückgesennet.

### Beispiel 2: Deaktivieren der Vorgangsplanung auf allen Computeknoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Mit diesen Befehlen wird die Aufgabenplanung auf allen Computerknoten im BatchpoolPool06 deaktiviert.
Um diese Aufgabe auszuführen, erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $context.
Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzBatchComputeNode,** um eine Sammlung aller in Pool06 gefundenen Computeknoten zurückzukehren.
Diese Sammlung wird dann an das **Cmdlet Disable-AzBatchComputeNodeScheduling** verschoben, um die Aufgabenplanung für jeden Computeknoten in der Sammlung zu deaktivieren.
Da der *Parameter DisableComputeNodeSchedulingOptions* nicht enthalten war, werden aufgaben, die derzeit auf den Computeknoten ausgeführt werden, erneut zurückgesennet.

## PARAMETER

### -BatchContext
Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.
Wenn Sie das Get-AzBatchAccount verwenden, um Ihren BatchAccountContext zu erhalten, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet. Wenn Sie stattdessen die Authentifizierung für freigegebene Schlüssel verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten. Bei Verwendung der Authentifizierung mit gemeinsam genutzten Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet. Um den zu verwendende Schlüssel zu ändern, legen Sie die BatchAccountContext.KeyInUse-Eigenschaft ein.

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
Gibt einen Objektbezug auf den Computeknoten an, auf dem die Aufgabenplanung deaktiviert ist.
Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchComputeNode erstellt und das zurückgegebene Computeknotenobjekt in einer Variablen gespeichert.

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
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt an, wie dieses Cmdlet mit aufgaben behandelt wird, die derzeit auf dem Computerknoten ausgeführt werden, auf dem die Planung deaktiviert wird.
Die zulässigen Werte für diesen Parameter sind:
- Requeue.
Aufgaben werden sofort beendet und an die Auftragswarteschlange zurückgegeben.
Dadurch können die Aufgaben auf einem anderen Computeknoten neu geplant werden.
Dies ist der Standardwert. 
- Beenden.
Aufgaben werden sofort beendet und aus der Auftragswarteschlange entfernt.
Diese Vorgänge werden nicht neu geplant. 
- TaskCompletion.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Vorgangsplanung auf dem Computeknoten deaktiviert ist.
Für diesen Knoten werden keine neuen Aufgaben geplant. 
- RetainedData.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Aufbewahrungszeiträume für Daten können ablaufen, bevor die Aufgabenplanung auf dem Computeknoten deaktiviert wird.
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
Gibt die ID des Computeknotens an, in dem die Vorgangsplanung deaktiviert ist.

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
Gibt die ID des Batchpools an, der den Computeknoten enthält, in dem die Vorgangsplanung deaktiviert ist.
Wenn Sie den *Parameter PoolId verwenden,* verwenden Sie den *Parameter ComputeNode* nicht in demselben Befehl.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### System.Void

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


