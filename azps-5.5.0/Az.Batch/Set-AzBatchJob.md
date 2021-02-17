---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 75483BC7-440A-437B-9EDE-D270D87CF3C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJob.md
ms.openlocfilehash: 1104eed4d60405226cdc6dad351ae418b84142e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176100"
---
# Set-AzBatchJob

## SYNOPSIS
Aktualisiert einen Batchauftrag.

## SYNTAX

```
Set-AzBatchJob [-Job] <PSCloudJob> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzBatchJob"** aktualisiert einen Azure Batch-Auftrag.
Verwenden Sie das Get-AzBatchJob-Cmdlet, um ein **"PSCloudJob"-Objekt zu** erhalten.
Ändern Sie die Eigenschaften dieses Objekts, und verwenden Sie dann das aktuelle Cmdlet, um Ihre Änderungen an den Batchdienst zu commiten.

## BEISPIELE

### Beispiel 1: Aktualisieren eines Auftrags
```
PS C:\>$Job = Get-AzBatchJob -Id "Job17" -BatchContext $Context
PS C:\> $Job.Priority = 1
PS C:\> Set-AzBatchJob -Job $Job -BatchContext $Context
```

Der erste Befehl ruft einen Auftrag mithilfe von **"Get-AzBatchJob"** ab und speichert ihn dann in der $Job Variable.
Mit dem zweiten Befehl wird die Prioritätsspezifikation für das $Job geändert.
Der letzte Befehl aktualisiert den Batchdienst so, dass er dem lokalen Objekt in der $Job.

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

### -Job
Gibt einen **PSCloudJob an,** an den dieses Cmdlet den Batchdienst aktualisiert.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Batch. Models.PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## AUSGABEN

### System.Void

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Disable-AzBatchJob](./Disable-AzBatchJob.md)

[Enable-AzBatchJob](./Enable-AzBatchJob.md)

[Get-AzBatchJob](./Get-AzBatchJob.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[New-AzBatchJob](./New-AzBatchJob.md)

[Remove-AzBatchJob](./Remove-AzBatchJob.md)

[Stop-AzBatchJob](./Stop-AzBatchJob.md)

[Azure-Batch-Cmdlets](/powershell/module/Az.Batch/)
