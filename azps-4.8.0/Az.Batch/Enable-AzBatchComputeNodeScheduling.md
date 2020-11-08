---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008704"
---
# Enable-AzBatchComputeNodeScheduling

## Synopsis
Aktiviert die Aufgabenplanung auf dem angegebenen Compute-Knoten.

## Syntax

### ID (Standard)
```
Enable-AzBatchComputeNodeScheduling [-PoolId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchComputeNodeScheduling [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **enable-AzBatchComputeNodeScheduling** ermöglicht die Aufgabenplanung auf dem angegebenen Compute-Knoten.
Ein Compute-Knoten ist ein Azure Virtual Machine, der einer bestimmten Anwendungsauslastung gewidmet ist.

## Beispiele

### Beispiel 1: Aktivieren der Vorgangsplanung auf einem Compute-Knoten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Diese Befehle ermöglichen die Aufgabenplanung auf dem Compute-Knoten TVM-1783593343_34-20151117t222514z.
Dazu wird mit dem ersten Befehl im Beispiel ein Objektverweis erstellt, der die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.
Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet **enable-AzBatchComputeNodeScheduling** , um eine Verbindung mit dem Pool MyPool herzustellen und die Aufgabenplanung auf TVM-1783593343_34-20151117t222514z zu ermöglichen.

### Beispiel 2: Aktivieren der Vorgangsplanung für Compute-Knoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Mit diesen Befehlen können Sie die Aufgabenplanung für alle Compute-Knoten in der Pool-Pool06.
Zum Ausführen dieser Aufgabe wird mit dem ersten Befehl im Beispiel ein Objektverweis erstellt, der die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.
Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **Get-AzBatchComputeNode** , um eine Auflistung aller in Pool06 gefundenen Compute-Knoten zurückzugeben.
Diese Sammlung wird dann an das Cmdlet **enable-AzBatchComputeNodeScheduling** weitergeleitet, das die Aufgabenplanung für jeden Compute-Knoten in der Sammlung ermöglicht.

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
Gibt einen Objektverweis auf den Compute-Knoten an, in dem die Aufgabenplanung aktiviert ist.
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

### -ID
Gibt die ID des Compute-Knotens an, in dem die Vorgangsplanung aktiviert ist.

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
Gibt die ID des Batch Pools an, der den Compute-Knoten enthält, in dem die Vorgangsplanung aktiviert ist.

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

[Deaktivieren-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


