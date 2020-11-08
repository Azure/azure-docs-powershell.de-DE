---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2DF5FB4D-A5CB-439C-AC6F-DF2130AF33EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9e93d6fd17d4ba308e6d5752554fb03639fce769
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176635"
---
# Disable-AzBatchComputeNodeScheduling

## Synopsis
Deaktiviert die Vorgangsplanung auf dem angegebenen Compute-Knoten.

## Syntax

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

## Beschreibung
Das Cmdlet **Disable-AzBatchComputeNodeScheduling** deaktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.
Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.
Wenn Sie die Vorgangsplanung auf einem Compute-Knoten deaktivieren, können Sie auch bestimmen, was zu den Aufträgen aktuell in der Aufgabenwarteschlange des Knotens zu tun ist.
Mit **Disable-AzBatchComputeNodeScheduling** können Sie die folgenden Aktionen ausführen: 
- Kündigen Sie die Aufgaben, und setzen Sie Sie wieder in die Job-Warteschlange.
Dadurch können diese Aufgaben auf einem anderen Compute-Knoten neu geplant werden. 
- Kündigen Sie die Aufgaben, und entfernen Sie Sie aus der Job-Warteschlange.
Auf diese Weise gestoppte Aufgaben werden nicht neu geplant. 
- Warten Sie, bis alle zurzeit ausgeführten Aufgaben abgeschlossen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten. 
- Warten Sie, bis alle ausgeführten Aufgaben abgeschlossen sind und alle Datenaufbewahrungszeiträume abgelaufen sind, und deaktivieren Sie dann die Aufgabenplanung auf dem Compute-Knoten.

## Beispiele

### Beispiel 1: Deaktivieren der Vorgangsplanung auf einem Compute-Knoten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Disable-AzBatchComputeNodeScheduling -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Diese Befehle deaktivieren den Aufgabenplan auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.
Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **Disable-AzBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf dem Knoten TVM-1783593343_34-20151117t222514z zu deaktivieren.
Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle zurzeit auf dem Compute-Knoten ausgeführten Aufgaben erneut in die Warteschlange gestellt.

### Beispiel 2: Deaktivieren der Vorgangsplanung für alle Compute-Knoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Disable-AzBatchComputeNodeScheduling -BatchContext $Context
```

Diese Befehle deaktivieren die Aufgabenplanung auf allen Computerknoten im Batch Pool Pool06.
Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für die contosobatchaccount des Batch Kontos.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.
Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.
Diese Sammlung wird dann an das Cmdlet **Disable-AzBatchComputeNodeScheduling** umgeleitet, um die Aufgabenplanung für jeden Compute-Knoten in der Sammlung zu deaktivieren.
Da der *DisableComputeNodeSchedulingOptions* -Parameter nicht enthalten war, werden alle Aufgaben, die derzeit auf den Compute-Knoten ausgeführt werden, erneut in die Warteschlange gestellt.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet. Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen. Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet. Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.

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
Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung deaktiviert ist.
Dieser Objektverweis wird mithilfe des Get-AzBatchComputeNode-Cmdlets erstellt und speichert das zurückgegebene Compute-Knotenobjekt in einer Variablen.

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

### -DisableSchedulingOption
Gibt an, wie sich dieses Cmdlet auf alle Aufgaben bezieht, die derzeit auf dem Computerknoten ausgeführt werden, auf dem die Planung deaktiviert ist.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Erneute Warteschlange.
Aufgaben werden sofort angehalten und an die Job-Warteschlange zurückgegeben.
Dadurch können die Aufgaben auf einem anderen Compute-Knoten neu geplant werden.
Dies ist der Standardwert. 
- Beenden.
Aufgaben werden sofort angehalten und aus der Job-Warteschlange entfernt.
Diese Aufgaben werden nicht neu geplant. 
- TaskCompletion.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, bevor die Vorgangsplanung auf dem Compute-Knoten deaktiviert ist.
Auf diesem Knoten werden keine neuen Aufgaben geplant. 
- RetainedData.
Derzeit ausgeführte Aufgaben können abgeschlossen werden, und Datenaufbewahrungszeiträume können ablaufen, bevor die Aufgabenplanung auf dem Compute-Knoten deaktiviert wird.
Auf diesem Knoten werden keine neuen Aufgaben geplant.

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
Gibt die ID des Compute-Knotens an, in dem die Aufgabenplanung deaktiviert ist.

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

### -Pool-Nr
Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Aufgabenplanung deaktiviert ist.
Wenn Sie den *Pool* -Parameter verwenden, verwenden Sie den *ComputeNode* -Parameter nicht in demselben Befehl.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft.Azure.Commands.Batch. Models. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Enable-AzBatchComputeNodeScheduling](./Enable-AzBatchComputeNodeScheduling.md)


