---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938291"
---
# Get-AzBatchSubtask

## SYNOPSIS
Ruft die Teilvorgängeinformationen der angegebenen Aufgabe ab.

## SYNTAX

### ODataFilter (Standard)
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Get-AzBatchSubtask** ruft die Teilvorgängeinformationen zur angegebenen Aufgabe ab.
Teilvorgänge bieten eine parallele Verarbeitung für einzelne Vorgänge und ermöglichen eine präzise Überwachung der Ausführung und des Fortschritts von Vorgängen.

## BEISPIELE

### Beispiel 1: Zurückgeben aller Teilvorgänge für einen angegebenen Vorgang
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

Diese Befehle geben alle Teilvorgänge für die Aufgabe mit der ID myTask zurück.
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Batchkonto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $context.
Der zweite Befehl verwendet dann diesen Objektverweis und das **Get-AzBatchSubtask-Cmdlet,** um alle Teilvorgänge für myTask zurückzukehren, eine Aufgabe, die im Rahmen von Job-01 ausgeführt wird.

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

### -JobId
Gibt die ID des Auftrags an, der die Aufgabe enthält, deren Teilvorgänge dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
Gibt die maximale Anzahl der zurückzukehrenden Teilvorgänge an.
Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.
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

### -Aufgabe
Gibt einen Objektbezug auf die Aufgabe an, die die Teilvorgänge enthalten, die dieses Cmdlet zurückgibt.
Dieser Objektverweis wird mithilfe des cmdlets Get-AzBatchTask erstellt und das zurückgegebene Objekt in einer Variablen gespeichert.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
Gibt die ID der Aufgabe an, deren Teilvorgänge dieses Cmdlet zurückgibt.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSSubtaskInformation

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchTask](./Get-AzBatchTask.md)


