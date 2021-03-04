---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 9cb2207381e7f874884bc53b5b85572fdffbd1a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919035"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
Ruft Remoteanmeldungseinstellungen für einen Computeknoten ab.

## SYNTAX

### ID (Standard)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzBatchRemoteLoginSetting-Cmdlet** ruft Remoteanmeldungseinstellungen für einen Computeknoten in einem infrastrukturbasierten Pool für virtuelle Computer ab.

## BEISPIELE

### Beispiel 1: Remoteanmeldungseinstellungen für alle Knoten in einem Pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Der erste Befehl ruft mithilfe von **Get-AzBatchAccountKey einen Batchkontokontext** ab, der Zugriffstasten für Ihr Abonnement enthält.
Der Befehl speichert den Kontext in der $Context, die im nächsten Befehl verwendet werden soll.
Der zweite Befehl ruft jeden Computeknoten im Pool ab, der über die ID ContosoPool verfügt, indem **Get-AzBatchComputeNode verwendet wird.**
Der Befehl übergibt jeden Computerknoten mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Der Befehl ruft die Remoteanmeldungseinstellungen für jeden Computeknoten ab.

### Beispiel 2: Remoteanmeldungseinstellungen für einen Knoten erhalten
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Der erste Befehl ruft einen Batchkontokontext ab, der Zugriffstasten für Ihr Abonnement enthält, und speichert ihn dann in der $Context Variablen.
Der zweite Befehl ruft die Remoteanmeldungseinstellungen für den Computeknoten ab, der die angegebene ID im Pool mit der ID ContosoPool hat.

## PARAMETER

### -BatchContext
Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.
Um einen **BatchAccountContext zu erhalten,** der Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzBatchAccountKey Cmdlet.

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
Gibt einen Computeknoten als **PSComputeNode-Objekt** an, für den dieses Cmdlet Remoteanmeldungseinstellungen erhält.
Verwenden Sie zum Abrufen eines Computeknotenobjekts das Get-AzBatchComputeNode Cmdlet.

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
Gibt die ID des Computeknotens an, für den die Einstellungen für die Remoteanmeldung angezeigt werden.
für die dieses Cmdlet Remoteanmeldungseinstellungen erhält.

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

### -PoolId
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings

## NOTIZEN

## VERWANDTE LINKS

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
