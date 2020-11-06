---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: d25e9aeb75c58bcce560043d87f5ce9eef065b97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500277"
---
# Get-AzureBatchRemoteLoginSettings

## Synopsis
Ruft die Remote Anmeldeeinstellungen für einen Compute-Knoten ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ID (Standard)
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureBatchRemoteLoginSettings** " ruft Remote Anmeldeeinstellungen für einen Compute-Knoten in einem auf Infrastruktur basierenden virtuellen Computerpool ab.

## Beispiele

### Beispiel 1: Abrufen von Remote Anmeldeeinstellungen für alle Knoten in einem Pool
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, indem **Sie Get-AzureRmBatchAccountKeys** verwenden.
Der Befehl speichert den Kontext in der $Context Variablen, die im nächsten Befehl verwendet werden soll.
Der zweite Befehl ruft jeden Compute-Knoten im Pool ab, der die ID-ContosoPool mithilfe von **Get-AzureBatchComputeNode**.
Der Befehl übergibt die einzelnen Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl ruft die Remote Anmeldeeinstellungen für jeden Compute-Knoten ab.

### Beispiel 2: Abrufen der Remote Anmeldeeinstellungen für einen Knoten
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Der erste Befehl ruft einen Batch Konto Kontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in der $Context-Variablen.
Der zweite Befehl ruft die Remote Anmeldeeinstellungen für den Compute-Knoten ab, auf dem sich die angegebene ID im Pool mit der ID ContosoPool befindet.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um eine **BatchAccountContext** zu erhalten, die Zugriffstasten für Ihr Abonnement enthält.

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
Gibt einen Compute-Knoten als **PSComputeNode** -Objekt an, für das dieses Cmdlet Remote Anmeldeeinstellungen erhält.
Verwenden Sie das Get-AzureBatchComputeNode-Cmdlet, um ein Compute-Node-Objekt zu erhalten.

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

### -ComputeNodeId
Gibt die ID des Compute-Knotens an, für den die Remote Anmeldeeinstellungen abgerufen werden sollen.
für die dieses Cmdlet Remote Anmeldeeinstellungen erhält.

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

### -Pool-Nr
Gibt die ID des Pools an, der den virtuellen Computer enthält.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft.Azure.Commands.Batch. Models. PSComputeNode
Parameter: ComputeNode (ByValue)

### Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter: batchcontext (ByValue)

## Ausgaben

### Microsoft.Azure.Commands.Batch. Models. PSRemoteLoginSettings

## Notizen

## Verwandte Links

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Get-AzureBatchRemoteDesktopProtocolFile](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[Azure Batch-Cmdlets](./AzureRM.Batch.md)


