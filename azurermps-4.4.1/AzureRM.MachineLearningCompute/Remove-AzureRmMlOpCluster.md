---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663313"
---
# Remove-AzureRmMlOpCluster

## Synopsis
Entfernt einen Operations Cluster.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Entfernen eines Vorgangs Clusters aus Cmdlet-Eingabeparametern
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### Entfernen eines Vorgangs Clusters aus einer OperationalizationCluster-Instanzen Definition
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### Entfernen eines Vorgangs Clusters aus einer Azure Resouce-ID
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## Beschreibung
Entfernt einen Operations Cluster. Einige Ressourcen, die dem Cluster zugeordnet sind, werden möglicherweise nicht alle entfernt. Beispielsweise wird der Azure-Containerdienst entfernt, die zugehörigen VMS jedoch nicht. Das Speicherkonto, die Container Registrierung und die Anwendungs Einsichten werden für Diagnoseinformationen nicht entfernt.

## Beispiele

### Beispiel 1
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### Beispiel 2
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## Parameter

### -Inputobject
Das Clusterobjekt für die Operation

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des Clusters für die Cluster Operation.

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe für den Zuordnungs Cluster.

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Azure-Ressourcen-ID für den Zuordnungs Cluster.

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
### System. String


## Ausgaben

### System. void


## Notizen

## Verwandte Links

