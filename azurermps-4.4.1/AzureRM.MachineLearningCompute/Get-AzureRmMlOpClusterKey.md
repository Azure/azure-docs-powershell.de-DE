---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501777"
---
# Get-AzureRmMlOpClusterKey

## Synopsis
Ruft die Zugriffstasten ab, die einem Operations Cluster zugeordnet sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Besorgen Sie sich die Schlüssel des Operations Clusters aus Cmdlet-Eingabeparametern.
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### Besorgen Sie sich die Schlüssel des Operations Clusters aus einer OperationalizationCluster-Instanzen Definition.
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### Besorgen Sie sich die Schlüssel des Operational Clusters aus einer Azure-Ressourcen-ID.
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## Beschreibung
Die Schlüssel für das Speicherkonto, die Container Registrierung und andere Dienste, die dem Zuordnungs Cluster zugeordnet sind, werden beim Abrufen der Clustereigenschaften nicht zurückgegeben. Ein bestimmter Aufruf zum Abrufen der Schlüssel muss vorgenommen werden, da es sich um vertrauliche Informationen handelt.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

Gibt die geheimen Schlüssel für die Dienste zurück, die dem Cluster für die Operation zugeordnet sind.

## Parameter

### -Inputobject
Das Clusterobjekt für die Operation

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
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
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
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
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## Eingaben

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster
System. String


## Ausgaben

### Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationClusterCredentials


## Notizen

## Verwandte Links

