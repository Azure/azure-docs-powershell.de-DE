---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93662111"
---
# Enable-AzBatchJob

## Synopsis
Aktiviert eine Stapelverarbeitung.

## Syntax

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **enable-AzBatchJob** aktiviert eine Azure-Batch Verarbeitung.
Nachdem Sie einen Auftrag aktiviert haben, können neue Aufgaben ausgeführt werden.

## Beispiele

### Beispiel 1: Aktivieren eines stapelverarbeitungsauftrags
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

Mit diesem Befehl können Sie den Auftrag mit der ID Job-000001.
Verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um der $Context Variablen einen Kontext zuzuweisen.

## Parameter

### -Batchcontext
Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.
Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet. Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen. Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet. Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.

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
Gibt die ID des Auftrags an, den dieses Cmdlet aktiviert.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## Ausgaben

### System. void

## Notizen

## Verwandte Links

[Deaktivieren-AzBatchJob](./Disable-AzBatchJob.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Neu – AzBatchJob](./New-AzBatchJob.md)

[Remove-AzBatchJob](./Remove-AzBatchJob.md)

[Stopp-AzBatchJob](./Stop-AzBatchJob.md)

[Azure Batch-Cmdlets](/powershell/module/az.batch)


