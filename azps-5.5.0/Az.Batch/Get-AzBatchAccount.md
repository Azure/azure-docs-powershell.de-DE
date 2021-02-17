---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171576"
---
# Get-AzBatchAccount

## SYNOPSIS
Ruft ein Batchkonto im aktuellen Abonnement ab.

## SYNTAX

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzBatchAccount-Cmdlet** ruft ein Azure -Batchkonto im aktuellen Abonnement ab. Sie können den Parameter *"AccountName"* verwenden, um ein einzelnes Konto zu erhalten, oder Sie können den Parameter *"ResourceGroupName"* verwenden, um Konten unter dieser Ressourcengruppe zu erhalten.

## BEISPIELE

### Beispiel 1: Erhalten eines Batchkontos nach Name
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

Dieser Befehl ruft das Batchkonto namens "pfuller" ab.

### Beispiel 2: Erhalten der einer Ressourcengruppe zugeordneten Batchkonten
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

Dieser Befehl ruft die Batchkonten ab, die der Ressourcengruppe "CmdletExampleRG" zugeordnet sind.

## PARAMETERS

### -AccountName
Gibt den Namen eines Kontos an.
Wenn Sie einen Kontonamen angeben, gibt dieses Cmdlet nur dieses Konto zurück.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
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

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an.
Wenn Sie eine Ressourcengruppe angeben, ruft dieses Cmdlet die Konten unter der angegebenen Ressourcengruppe ab.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"} Dieses Cmdlet ruft Konten ab, die die von diesem Parameter angegebenen Tags enthalten.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzBatchAccount](./New-AzBatchAccount.md)

[Remove-AzBatchAccount](./Remove-AzBatchAccount.md)

[Set-AzBatchAccount](./Set-AzBatchAccount.md)

[Azure-Batch-Cmdlets](/powershell/module/Az.Batch/)
