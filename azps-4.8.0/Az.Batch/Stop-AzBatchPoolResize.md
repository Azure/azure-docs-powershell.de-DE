---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165321"
---
# Stop-AzBatchPoolResize

## Synopsis
Beendet die Größe eines Pool-Vorgangs.

## Syntax

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Stop-AzBatchPoolResize** beendet eine Azure Batch-Größenänderung in einem Pool.

## Beispiele

### Beispiel 1: Beenden der Größenänderung eines Pools
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

Dieser Befehl beendet einen Größen Änderungsvorgang für den Pool mit der ID ContosoPool06.
Verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.

### Beispiel 2: Beenden der Größenänderung eines Pools mithilfe der Pipeline
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

Mit diesem Befehl wird die Größe eines Pools mithilfe des Pipelineoperators beendet.
Der Befehl ruft den Pool mit der ID-ContosoPool06 mithilfe des Get-AzBatchPool-Cmdlets ab.
Der Befehl übergibt das Pool-Objekt an das aktuelle Cmdlet.
Der Befehl beendet den Größen Änderungsvorgang für diesen Pool.

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
Gibt die ID des Pools an, für den das Cmdlet einen Größen Änderungsvorgang beendet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchPool](./Get-AzBatchPool.md)

[Anfang-AzBatchPoolResize](./Start-AzBatchPoolResize.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
