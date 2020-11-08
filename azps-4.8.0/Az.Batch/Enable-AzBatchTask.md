---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165326"
---
# Enable-AzBatchTask

## Synopsis
Reaktiviert eine Aufgabe.

## Syntax

### ID
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **enable-AzBatchTask** wird eine Aufgabe erneut aktiviert.
Wenn ein Vorgang seine Wiederholungsanzahl erschöpft hat, ermöglicht dieses Cmdlet dennoch die Ausführung.

## Beispiele

### Beispiel 1: Reaktivieren einer Aufgabe
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

Mit diesem Befehl wird die Aufgabe task2 in Job Job7 erneut aktiviert.

### Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

Dieser Befehl ruft die Batch Aufgabe mit der ID Task3 in dem Auftrag ab, der die ID-Job8 mit dem Get-AzBatchTask-Cmdlet aufweist.
Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl aktiviert diese Aufgabe erneut.

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
Gibt die ID der Aufgabe an, die erneut aktiviert werden soll.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Gibt die ID des Auftrags an, der die Aufgabe enthält.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Aufgabe
Gibt die Aufgabe an, die dieses Cmdlet reaktiviert.
Verwenden Sie das Get-AzBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft.Azure.Commands.Batch. Models. PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchTask](./Get-AzBatchTask.md)

[Neu – AzBatchTask](./New-AzBatchTask.md)

[Remove-AzBatchTask](./Remove-AzBatchTask.md)

[Satz-AzBatchTask](./Set-AzBatchTask.md)

[Stopp-AzBatchTask](./Stop-AzBatchTask.md)


