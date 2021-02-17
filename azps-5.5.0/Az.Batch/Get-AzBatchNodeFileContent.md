---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171516"
---
# Get-AzBatchNodeFileContent

## SYNOPSIS
Ruft eine Batchknotendatei ab.

## SYNTAX

### Task_Id_Path
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzBatchNodeFileContent"** ruft eine Azure Batch-Knotendatei ab und speichert sie als Datei oder in einem Datenstrom.

## BEISPIELE

### Beispiel 1: Erhalten einer einer Aufgabe zugeordneten Batchknotendatei und Speichern der Datei
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knotendatei mit dem Namen "StdOut.txt" ab und speichert sie im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.
Die StdOut.txt Knotendatei ist einer Aufgabe zugeordnet, die die ID Task01 für den Auftrag mit der ID Job01 enthält.
Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der Variablen einen Kontext $Context zuzuordnen.

### Beispiel 2: Herunterladen einer Batchknotendatei und Speichern der Datei unter einem angegebenen Dateipfad mithilfe der Pipeline
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knotendatei mit dem Namen StdErr.txt mit dem cmdlet Get-AzBatchNodeFile ab.
Der Befehl übergibt diese Datei mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Das aktuelle Cmdlet speichert diese Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.
Die StdOut.txt Knotendatei ist der Aufgabe zugeordnet, die die ID Task02 für den Auftrag mit der ID Job02 enthält.

### Beispiel 3: Erhalten einer einer Aufgabe zugeordneten Batchknotendatei und Direktes an einen Datenstrom
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in $Stream Variable.
Der zweite Befehl ruft die Knotendatei mit dem Namen "StdOut.txt" aus der Aufgabe ab, die die ID "Task11" für den Auftrag mit der ID "Job03" enthält.
Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.

### Beispiel 4: Herunterladen einer Knotendatei von einem Computeknoten und Speichern der Knotendatei
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Dieser Befehl ruft die Knotendatei Startup\StdOut.txt von dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID Pool01 enthält.
Der Befehl speichert die Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.

### Beispiel 5: Herunterladen einer Knotendatei von einem Computeknoten und Speichern der Knotendatei mithilfe der Pipeline
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

Mit diesem Befehl wird die Knotendatei Startup\StdOut.txt mit Get-AzBatchNodeFile des Rechenknotens mit der ID ComputeNode01 ruft.
Der Rechenknoten befindet sich in dem Pool mit dem ID Pool01.
Der Befehl übergibt diese Knotendatei an das aktuelle Cmdlet.
Dieses Cmdlet speichert die Datei im E:\PowerShell\StdOut.txt dateipfad auf dem lokalen Computer.

### Beispiel 6: Herunterladen einer Knotendatei von einem Computeknoten und Direktes an einen Datenstrom
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Der erste Befehl erstellt einen Datenstrom mithilfe des New-Object-Cmdlets und speichert ihn dann in $Stream Variable.
Der zweite Befehl ruft die Knotendatei mit dem Namen StdOut.txt aus dem Computeknoten ab, der die ID ComputeNode01 im Pool mit dem ID Pool01 enthält.
Der Befehl leitet Dateiinhalte an den Datenstrom in $Stream.

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

### -ByteRangeEnd
Das Ende des byte-Bereichs, der heruntergeladen werden soll.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
Der Anfang des byte-Bereichs, der heruntergeladen werden soll.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Gibt die ID des Computeknotens an, der die Knotendatei enthält, die von diesem Cmdlet zurückgegeben wird.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DestinationPath
Gibt den Dateipfad an, unter dem dieses Cmdlet die Knotendatei speichert.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Gibt den Datenstrom an, in den dieses Cmdlet den Inhalt der Knotendatei schreibt.
Dieser Datenstrom wird mit diesem Cmdlet nicht geschlossen oder zurückspulen.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Gibt die Datei an, die dieses Cmdlet erhält, als **PSNodeFile-Objekt.**
Verwenden Sie zum Abrufen eines Knotendateiobjekts das Get-AzBatchNodeFile-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt die ID des Auftrags an, der die Zielaufgabe enthält.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Der Pfad der Knotendatei, die heruntergeladen werden soll.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Gibt die ID des Pools an, der den Rechenknoten mit der Knotendatei enthält, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TaskId
Gibt die ID des Vorgangs an.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### System.Void

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Azure-Batch-Cmdlets](/powershell/module/Az.Batch/)
