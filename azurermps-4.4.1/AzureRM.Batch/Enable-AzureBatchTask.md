---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665109"
---
# Enable-AzureBatchTask

## Synopsis
Reaktiviert eine Aufgabe.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ID
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **enable-AzureBatchTask** wird eine Aufgabe erneut aktiviert.
Wenn ein Vorgang seine Wiederholungsanzahl erschöpft hat, ermöglicht dieses Cmdlet dennoch die Ausführung.

## Beispiele

### Beispiel 1: Reaktivieren einer Aufgabe
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

Mit diesem Befehl wird die Aufgabe task2 in Job Job7 erneut aktiviert.

### Beispiel 2: Reaktivieren einer Aufgabe mithilfe der Pipeline
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

Dieser Befehl ruft die Batch Aufgabe mit der ID Task3 in dem Auftrag ab, der die ID-Job8 mit dem Get-AzureBatchTask-Cmdlet aufweist.
Der Befehl übergibt diesen Vorgang mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl aktiviert diese Aufgabe erneut.

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
Verwenden Sie das Get-AzureBatchTask-Cmdlet, um ein **PSCloudTask** -Objekt zu erhalten.

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

### PSCloudTask
Der Parameter "Aufgabe" akzeptiert den Wert vom Typ "PSCloudTask" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchTask](./Get-AzureBatchTask.md)

[Neu – AzureBatchTask](./New-AzureBatchTask.md)

[Remove-AzureBatchTask](./Remove-AzureBatchTask.md)

[Satz-AzureBatchTask](./Set-AzureBatchTask.md)

[Stopp-AzureBatchTask](./Stop-AzureBatchTask.md)


