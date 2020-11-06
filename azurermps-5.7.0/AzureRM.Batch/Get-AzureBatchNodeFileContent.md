---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeFileContent.md
ms.openlocfilehash: 7795182ff1594c098a2afd778c137c48dc74c955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499057"
---
# Get-AzureBatchNodeFileContent

## Synopsis
Ruft eine Batch-Knoten Datei ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Task_Id_Path
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzureBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzureBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzureBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureBatchNodeFileContent** " Ruft eine Azure-Batch-Knoten Datei ab und speichert Sie als Datei oder in einem Stream.

## Beispiele

### Beispiel 1: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Speichern der Datei
```
PS C:\>Get-AzureBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knoten Datei mit dem Namen StdOut.txt ab und speichert Sie im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.
Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task01 für den Auftrag mit der ID Job01 hat.
Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.

### Beispiel 2: Abrufen einer Batch-Knoten Datei und Speichern der Datei in einem angegebenen Dateipfad mithilfe der Pipeline
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knoten Datei mit dem Namen StdErr.txt mithilfe des Get-AzureBatchNodeFile-Cmdlets ab.
Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.
Die StdOut.txt-Knoten Datei ist mit der Aufgabe verknüpft, die die ID-Task02 für den Auftrag enthält, der die ID Job02 hat.

### Beispiel 3: Abrufen einer Batch-Knoten Datei, die einem Vorgang zugeordnet ist, und Weiterleiten an einen Datenstrom
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.

Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus der Aufgabe ab, die die ID-Task11 für den Auftrag mit der ID Job03 hat.
Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.

### Beispiel 4: Abrufen einer Knoten Datei von einem Compute-Knoten und speichern
```
PS C:\>Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.
Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.

### Beispiel 5: Abrufen einer Knoten Datei aus einem Compute-Knoten und speichern mithilfe der Pipeline
```
PS C:\>Get-AzureBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzureBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knoten Datei Startup\StdOut.txt mithilfe von Get-AzureBatchNodeFile aus dem Compute-Knoten ab, der die ID ComputeNode01.
Der Compute-Knoten befindet sich im Pool mit der ID Pool01.
Der Befehl übergibt diese Knoten Datei an das aktuelle Cmdlet.
Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt Dateipfad auf dem lokalen Computer.

### Beispiel 6: Abrufen einer Knoten Datei aus einem Compute-Knoten und Weiterleiten an einen Datenstrom
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in der $Stream-Variablen.

Der zweite Befehl ruft die Knoten Datei mit dem Namen StdOut.txt aus dem Compute-Knoten ab, der die ID-ComputeNode01 im Pool mit der ID Pool01 hat.
Der Befehl leitet Dateiinhalte in $Stream an den Datenstrom weiter.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet. Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen. Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet. Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
Das Ende des Bytebereichs, der heruntergeladen werden soll.
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
Der Anfang des Bytebereichs, der heruntergeladen werden soll.
```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Gibt die ID des Compute-Knotens an, der die vom Cmdlet zurückgegebene Knoten Datei enthält.

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
Gibt den Dateipfad an, in dem dieses Cmdlet die Knoten Datei speichert.

```yaml
Type: String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Gibt den Datenstrom an, in den das Cmdlet den Inhalt der Knoten Datei schreibt.
Mit diesem Cmdlet wird dieser Datenstrom nicht geschlossen oder zurückgespult.

```yaml
Type: Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Gibt die Datei an, die dieses Cmdlet erhält, als **PSNodeFile** -Objekt.
Verwenden Sie das Get-AzureBatchNodeFile-Cmdlet, um ein Knoten Dateiobjekt zu erhalten.

```yaml
Type: PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt die ID des Auftrags an, der die Ziel Aufgabe enthält.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Der Pfad der Knoten Datei, die heruntergeladen werden soll.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pool-Nr
Gibt die ID des Pools an, der den Compute-Knoten enthält, der die Knoten Datei enthält, die dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Task-Nr
Gibt die ID der Aufgabe an.

```yaml
Type: String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### BatchAccountContext
Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.

### PSNodeFile
Der Parameter "Inputobject" akzeptiert den Wert vom Typ "PSNodeFile" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Azure Batch-Cmdlets](./AzureRM.Batch.md)


