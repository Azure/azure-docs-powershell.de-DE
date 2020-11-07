---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663566"
---
# Test-AzureRmMlOpClusterSystemServicesUpdateAvailability

## Synopsis
Überprüft, ob Updates für die Systemdienste verfügbar sind, die mit einem Operations Cluster verbunden sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Testen Sie die Verfügbarkeit von Updates über Cmdlet-Eingabeparameter.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### Testen Sie die Verfügbarkeit von Updates anhand einer OperationalizationCluster-Instanzen Definition.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### Testen Sie die Verfügbarkeit von Updates über eine Azure Resouce-ID.
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## Beschreibung
System Dienste erhalten Updates unabhängig vom Operations Cluster. Wenn Sie dieses Cmdlet verwenden, kann der Benutzer wissen, ob Invoke-AzureRmMlOpClusterSystemServicesUpdate.

## Beispiele

### Beispiel 1
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### Beispiel 2
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### Beispiel 3
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## Parameter

### -Inputobject
Das Clusterobjekt für die Operation

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Der Name des Clusters für die Cluster Operation.

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
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
Parameter Sets: Test for update availability from cmdlet input parameters.
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
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
### System. String


## Ausgaben

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSCheckSystemServicesUpdatesAvailableResponse


## Notizen

## Verwandte Links

