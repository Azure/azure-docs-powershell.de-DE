---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 36EB9CE6-EAC9-471C-97D6-14E882E0F710
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchcomputenodescheduling
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchComputeNodeScheduling.md
ms.openlocfilehash: 9969388d51abb337030a8a732805ee1a15368ea7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356472"
---
# Enable-AzBatchComputeNodeScheduling

## SYNOPSIS
Aktiviert die Aufgabenplanung für den angegebenen Rechenknoten.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet "Enable-AzBatchComputeNodeScheduling"** ermöglicht die Aufgabenplanung für den angegebenen Rechenknoten.
Ein Rechenknoten ist ein virtueller Azure-Computer, der einer bestimmten Anwendungsarbeitsauslastung gewidmet ist.

## BEISPIELE

### Beispiel 1: Aktivieren der Aufgabenplanung für einen Rechenknoten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Enable-AzBatchComputeNodeScheduling  -PoolId "myPool" -Id "tvm-1783593343_34-20151117t222514z" -BatchContext $Context
```

Diese Befehle ermöglichen die Aufgabenplanung auf dem berechneten Knoten "tvm-1783593343_34-20151117t222514z".
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto "contosobatchaccount" enthält.
Dieser Objektverweis wird in einer Variablen namens "$context.
Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Enable-AzBatchComputeNodeScheduling",** um eine Verbindung mit dem Pool "myPool" herzustellen und die Aufgabenplanung auf tvm-1783593343_34-20151117t222514z zu aktivieren.

### Beispiel 2: Aktivieren der Aufgabenplanung für Rechenknoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchComputeNode -PoolId "Pool06"  -BatchContext $Context | Enable-AzBatchComputeNodeScheduling  -BatchContext $Context
```

Diese Befehle ermöglichen die Aufgabenplanung für alle Im Pool06 gefundenen Rechenknoten.
Zum Ausführen dieser Aufgabe erstellt der erste Befehl im Beispiel einen Objektverweis, der die Kontoschlüssel für das Batchkonto "contosobatchaccount" enthält.
Dieser Objektverweis wird in einer Variablen namens "$context.
Der zweite Befehl im Beispiel verwendet dann diesen Objektverweis und **"Get-AzBatchComputeNode",** um eine Sammlung aller In Pool06 gefundenen Berechnungsknoten zurückzukehren.
Diese Sammlung wird dann an das **Cmdlet "Enable-AzBatchComputeNodeScheduling"** weiterverteilt, das die Aufgabenplanung für jeden Berechnungsknoten in der Sammlung ermöglicht.

## PARAMETERS

### -BatchContext
Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.
Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet. Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten. Bei verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet. Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.

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
Gibt einen Objektverweis auf den Rechenknoten an, für den die Aufgabenplanung aktiviert ist.
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

### -ID
Gibt die ID des Rechenknotens an, für den die Aufgabenplanung aktiviert ist.

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
Gibt die ID des Batchpools an, der den Rechenknoten enthält, für den die Aufgabenplanung aktiviert ist.

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

[Disable-AzBatchComputeNodeScheduling](./Disable-AzBatchComputeNodeScheduling.md)


