---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 51bfee17e33afcb93b90c36198e9352c3fca5fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662428"
---
# Add-AzureRmHDInsightScriptAction

## Synopsis
Fügt einem Cluster Konfigurationsobjekt eine Skript Aktion hinzu.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das **Add-AzureRmHDInsightScriptAction-** Cmdlet fügt dem vom New-AzureRmHDInsightClusterConfig-Cmdlet erstellten HDInsight-Konfigurationsobjekt Skriptaktionen hinzu.

Skriptaktionen stellen Funktionen bereit, die zum Installieren zusätzlicher Software oder zum Ändern der Konfiguration von Anwendungen, die auf einem Hadoop-Cluster ausgeführt werden, mithilfe von Windows PowerShell-oder Bash-Skripts (für Windows-oder Linux-Cluster) verwendet werden.

Eine Skript Aktion wird auf den Clusterknoten ausgeführt, wenn HDInsight-Cluster bereitgestellt werden, und Sie werden ausgeführt, nachdem die Knoten im Cluster die HDInsight-Konfiguration abgeschlossen haben.
Die Skript Aktion wird unter Systemadministratorkonto Privilegien ausgeführt und bietet vollständige Zugriffsrechte für die Clusterknoten.
Sie können jedem Cluster eine Liste von Skriptaktionen zur Verfügung stellen, die in einer bestimmten Reihenfolge ausgeführt werden sollen.

## Beispiele

### Beispiel 1: Hinzufügen einer Skript Aktion zum Cluster-Konfigurationsobjekt
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

Dieser Befehl fügt eine Skript Aktion für die Head-und worker-Knoten des Clusters your-Hadoop-001 hinzu, die am Ende der Clustererstellung ausgeführt werden.

## Parameter

### -Config
Gibt das HDInsight-Cluster Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.
Dieses Objekt wird vom Cmdlet **New-AzureRmHDInsightClusterConfig** erstellt.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Skript Aktion an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeType
Gibt den Knotentyp an, für den die Skript Aktion ausgeführt werden soll.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- HeadNode
- WorkerNode
- ZookeeperNode

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
Gibt die Parameter für die Skript Aktion an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Gibt den öffentlichen URI für die Skript Aktion an (ein PowerShell-oder bash-Skript).

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### AzureHDInsightConfig
Der Parameter "config" akzeptiert den Wert vom Typ "AzureHDInsightConfig" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig

## Notizen

## Verwandte Links

[Neu – AzureRmHDInsightClusterConfig](./New-AzureRmHDInsightClusterConfig.md)


