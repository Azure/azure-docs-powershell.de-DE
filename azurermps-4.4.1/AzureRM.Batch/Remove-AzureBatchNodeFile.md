---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DBA02017-8372-4A91-A4F1-985777DEDAB9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchNodeFile.md
ms.openlocfilehash: 5b8797cf2f6068098d1ca407f0f97283dd171af5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497890"
---
# Remove-AzureBatchNodeFile

## Synopsis
Löscht eine Knoten Datei für einen Vorgang oder einen Compute-Knoten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Aufgabe
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComputeNode
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObject
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureBatchNodeFile** löscht eine Azure-Batch-Knoten Datei für einen Task-oder Compute-Knoten.

## Beispiele

### Beispiel 1: Löschen einer Datei Extent mit einer Aufgabe
```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

Dieser Befehl löscht die Knoten Datei mit dem Namen wd\testFile.txt.
Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.

### Beispiel 2: Löschen einer Datei aus einem Compute-Knoten
```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

Dieser Befehl löscht die Knoten Datei mit dem Namen startup\testFile.txt aus dem angegebenen Compute-Knoten im Pool mit der ID Pool07.

### Beispiel 3: Entfernen einer Datei mithilfe der Pipeline
```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

Dieser Befehl ruft die Knoten Datei mithilfe von **Get-AzureBatchNodeFile** ab.
Diese Datei ist mit der Aufgabe verknüpft, die die ID Task26 unter dem Job Job-000001.
Der Befehl übergibt diese Datei mithilfe der Pipeline an das aktuelle Cmdlet.
Das aktuelle Cmdlet entfernt die Knoten Datei.
Der Befehl gibt den Parameter *Force* an.
Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.

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

### -ComputeNodeId
Gibt die ID des Compute-Knotens an, der die vom Cmdlet gelöschte Batch-Knoten Datei enthält.

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Gibt das **PSNodeFile** -Objekt an, das die vom Cmdlet gelöschte Knoten Datei darstellt.
Verwenden Sie zum Abrufen eines **PSNodeFile** das Get-AzureBatchNodeFile-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Gibt die ID des Auftrags an, der die Aufgabe enthält.

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der vom Cmdlet gelöschten Knoten Datei an.

```yaml
Type: System.String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pool-Nr
Gibt die ID des Pools an, der die Compute-Knoten enthält, für die dieses Cmdlet eine Datei entfernt.

```yaml
Type: System.String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekursiv
Gibt an, dass dieses Cmdlet den Ordner und alle Unterordner und Dateien unterhalb des angegebenen Pfads löscht.
Dieses Cmdlet ist nur relevant, wenn es sich bei dem Pfad um einen Ordner handelt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Task-Nr
Gibt die ID der Aufgabe an.

```yaml
Type: System.String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### PSNodeFile
Der Parameter "Inputobject" akzeptiert den Wert vom Typ "PSNodeFile" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchNodeFile](./Get-AzureBatchNodeFile.md)

[Get-AzureBatchNodeFileContent](./Get-AzureBatchNodeFileContent.md)


