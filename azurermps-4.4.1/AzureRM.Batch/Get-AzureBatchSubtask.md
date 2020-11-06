---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505650"
---
# Get-AzureBatchSubtask

## Synopsis
Ruft die Untervorgangs Informationen der angegebenen Aufgabe ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ODataFilter (Standard)
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Get-AzureBatchSubtask werden** die Teilvorgangsinformationen zur angegebenen Aufgabe abgerufen.
Teilvorgänge bieten parallele Verarbeitung für einzelne Aufgaben und ermöglichen eine präzise Überwachung der Aufgabenausführung und des Fortschritts.

## Beispiele

### Beispiel 1: Zurückgeben aller Teilvorgänge für eine angegebene Aufgabe
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

Mit diesen Befehlen werden alle Teilvorgänge für die Aufgabe mit der ID MyTask zurückgegeben.
Dazu erstellt der erste Befehl im Beispiel einen Objektverweis auf die Kontoschlüssel für das Stapelverarbeitungs Konto contosobatchaccount.
Dieser Objektverweis wird in einer Variablen mit dem Namen $Context gespeichert.

Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzureBatchSubtask** ", um alle Teilvorgänge für MyTask zurückzugeben, eine Aufgabe, die als Teil von Job Job-01 ausgeführt wird.

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
Gibt die maximale Anzahl von Teilvorgängen an, die zurückgegeben werden sollen.
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

### – Aufgabe
Gibt einen Objektverweis auf die Aufgabe an, die die Teilvorgänge enthält, die dieses Cmdlet zurückgibt.
Dieser Objektverweis wird mithilfe des Get-AzureBatchTask-Cmdlets erstellt und speichert das zurückgegebene Objekt in einer Variablen.

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

### -Task-Nr
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

###  
Dieses Cmdlet gibt Instanzen des **PSSubtaskInformation** -Objekts zurück.

## Notizen

## Verwandte Links

[Get-AzureBatchTask](./Get-AzureBatchTask.md)


