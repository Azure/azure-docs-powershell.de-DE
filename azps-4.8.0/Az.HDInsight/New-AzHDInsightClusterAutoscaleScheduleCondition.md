---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 86276DF3-95E2-405F-BA46-F188B7AE3B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterautoscaleschedulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterAutoscaleScheduleCondition.md
ms.openlocfilehash: 4f046344942e244d6bd220034f7cbe85c48681ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009282"
---
# New-AzHDInsightClusterAutoscaleScheduleCondition

## Synopsis
Erstellt eine Plan basierte AutoScale-Bedingung.

## Syntax

```
New-AzHDInsightClusterAutoscaleScheduleCondition -Time <DateTime> -WorkerNodeCount <Int32>
 -Day <AzureHDInsightDaysOfWeek[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzHDInsightClusterAutoscaleScheduleCondition** erstellt eine zeitplanbasierte AutoScale-Bedingung.

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday
```

Mit diesem Befehl wird eine Bedingung erstellt, in der der Cluster automatisch auf 5 Worker-Knoten bei 09:00 pro Montag, Mittwoch, skaliert wird.

### Beispiel 2: Aktivieren Sie die zeitplanbasierte autoskala eines Clusters mit automatischem skalieren.
```powershell
# create a autoscale condition
PS C:\> $condition=New-AzHDInsightClusterAutoscaleScheduleCondition -Time 09:00 -WorkerNodeCount 5 -Day Monday,Wednesday

# Set the cluster autoscale configuration
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Set-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName -Schedule -TimeZone "Pacific Standard Time" -Condition $condition
```

Mit diesem Befehl wird eine Bedingung erstellt, in der der Cluster automatisch auf 5 Worker-Knoten bei 09:00 pro Montag, Mittwoch, skaliert wird.

## Parameter

### -Tag
Ruft die Tage der AutoScale-Terminplan Bedingung ab oder legt diese fest.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightDaysOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
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

### -Zeit
Ruft die Zeit der AutoScale-Terminplan Bedingung ab oder legt diese fest.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkerNodeCount
Ruft die Zeit Plan workernode Anzahl der AutoScale-Terminplan Bedingung ab oder legt diese fest.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscaleCondition

## Notizen

## Verwandte Links

[Neu – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Satz-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
