---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009388"
---
# Remove-AzBatchPool

## Synopsis
Löscht den angegebenen Batch Pool.

## Syntax

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzBatchPool** löscht den angegebenen Azure Batch-Pool.
Sie werden zur Bestätigung aufgefordert, es sei denn, Sie verwenden den Parameter *Force* .

## Beispiele

### Beispiel 1: Löschen eines Batch Pools nach Pool-ID
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

Dieser Befehl löscht den Pool mit der ID MyPool.
Der Benutzer wird zur Bestätigung aufgefordert, bevor der Löschvorgang durchgeführt wird.

### Beispiel 2: Löschen aller Batch Pools mit Gewalt
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

Dieser Befehl löscht alle Batch-Pools.
Da der Parameter *Force* vorhanden ist, wird die Bestätigungsaufforderung unterdrückt.

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

### -ID
Gibt die ID des zu löschenden Pools an.
Sie können keine Platzhalterzeichen angeben.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

[Neu – AzBatchPool](./New-AzBatchPool.md)

[Azure Batch-Cmdlets](/powershell/module/Az.Batch/)
