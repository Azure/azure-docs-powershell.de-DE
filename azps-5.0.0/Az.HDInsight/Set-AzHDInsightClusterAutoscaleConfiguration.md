---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 1C3B7A57-D645-498C-98F4-DAE9B782123E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: bb22bda0f22ae128942e6e1d5a7aed9b0b646875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296337"
---
# Set-AzHDInsightClusterAutoscaleConfiguration

## Synopsis
Legt die AutoScale-Konfiguration eines Azure HDInsight-Clusters fest.

## Syntax

### LoadAutoscaleByNameParameterSet (Standard)
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScheduleAutoscaleByNameParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AutoscaleConfigurationByNameParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LoadAutoscaleByResourceIdParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-MinWorkerNodeCount <Int32>]
 [-MaxWorkerNodeCount <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ScheduleAutoscaleByResourceIdParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AutoscaleConfigurationByResourceIdParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LoadAutoscaleByInputObjectParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-MinWorkerNodeCount <Int32>] [-MaxWorkerNodeCount <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScheduleAutoscaleByInputObjectParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-TimeZone <String>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]>]
 [-Schedule] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AutoscaleConfigurationByInputObjectParameterSet
```
Set-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 -AutoscaleConfiguration <AzureHDInsightAutoscale> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Mit diesem Cmdlet **Set-AzHDInsightClusterAutoscaleConfiguration** wird die AutoScale-Konfiguration eines Azure HDInsight-Clusters festgelegt.

## Beispiele

### Beispiel 1: Einrichten der Last basierten Konfiguration des HDInsight-Clusters
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup `
            -ClusterName $clusterName -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5
```

Mit diesem Befehl wird die Last basierte AutoScale-Konfiguration eines Azure HDInsight-Clusters festgelegt.

### Beispiel 2: Festlegen der zeitplanbasierten autoskala des HDInsight-Clusters
```powershell
# Create autoscale conditions
PS C:\> $condition1=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
PS C:\> $condition2=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 4 -Day Friday

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition1,$condition2
```

Mit diesem Befehl wird die Plan basierte AutoScale-Konfiguration des HDInsight-Clusters festgelegt.

### Beispiel 3: Einrichten der AutoScale-Konfiguration des HDInsight-Clusters basierend auf einem anderen Cluster, der die Konfiguration der AutoScale-Konfiguration eingestellt hat
```powershell
# Get the autoscale configuration of another cluster.
PS C:\> $clusterResourceGroup="group"
PS C:\> $anotherClusterName="anotherClusterName"
PS C:\> $autoscaleConfig=Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $anotherClusterName

# Set autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName `
            -Autoscale $autoscaleConfig
```

Mit diesem Befehl wird die AutoScale-Konfiguration des HDInsight-Clusters basierend auf einem anderen Cluster festgelegt.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -AutoscaleConfiguration
Ruft die Konfiguration des AutoScale ab oder legt diese fest

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: AutoscaleConfigurationByNameParameterSet, AutoscaleConfigurationByResourceIdParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Clustername
Ruft den Namen des Clusters ab oder legt ihn fest.

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bedingung
Ruft die Bedingung des zeitplanbasierten AutoScale ab oder legt diese fest.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscaleCondition]
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Inputobject
Ruft das Eingabeobjekt ab oder legt dieses fest.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: LoadAutoscaleByInputObjectParameterSet, ScheduleAutoscaleByInputObjectParameterSet, AutoscaleConfigurationByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxWorkerNodeCount
Ruft die maximale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinWorkerNodeCount
Ruft die minimale workernode-Anzahl der Last basierten autoskala ab oder legt diese fest.

```yaml
Type: System.Int32
Parameter Sets: LoadAutoscaleByNameParameterSet, LoadAutoscaleByResourceIdParameterSet, LoadAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByNameParameterSet, ScheduleAutoscaleByNameParameterSet, AutoscaleConfigurationByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ruft die Ressourcen-ID ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: LoadAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByResourceIdParameterSet, AutoscaleConfigurationByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Terminplan
Festlegen von zeitplanbasierten Parametern

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone
Ruft die Zeitzone der zeitplanbasierten autoskala ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: ScheduleAutoscaleByNameParameterSet, ScheduleAutoscaleByResourceIdParameterSet, ScheduleAutoscaleByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale

## Notizen

## Verwandte Links

[Neu – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)
