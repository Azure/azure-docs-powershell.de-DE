---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005926"
---
# Add-AzureHDInsightScriptAction

## Synopsis
Fügt eine HDInsight-Skript Aktion hinzu.

## Syntax

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Das Cmdlet **Add-AzureHDInsightScriptAction** bietet Azure-HDInsight-Funktionen, die zum Installieren zusätzlicher Software oder zum Ändern der Konfiguration von Anwendungen verwendet werden, die in einem Hadoop-Cluster mithilfe von Windows PowerShell-Skripts ausgeführt werden.

Eine Skript Aktion wird auf den Clusterknoten ausgeführt, wenn HDInsight-Cluster bereitgestellt werden, und Sie werden ausgeführt, nachdem die Knoten im Cluster die HDInsight-Konfiguration abgeschlossen haben.
Die Skript Aktion wird unter Systemadministratorkonto Privilegien ausgeführt und bietet vollständige Zugriffsrechte für die Clusterknoten.
Sie können jedem Cluster eine Liste von Skriptaktionen zur Verfügung stellen, die in einer bestimmten Reihenfolge ausgeführt werden sollen.

## Beispiele

### Beispiel 1: Hinzufügen einer Skript Aktion zu einem Cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Der erste Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.

Der zweite Befehl verwendet das Cmdlet **Add-AzureHDInsightScriptAction** , um die Skript Aktion mit dem Namen TestScriptAction zu $config hinzuzufügen.

Der endgültige Befehl verwendet das Cmdlet **New-AzureHDInsightCluster** zum Erstellen eines neuen HDInsight-Clusters, der die in $config gespeicherte Skript Aktion ausführt.

### Beispiel 2: Hinzufügen mehrerer Skriptaktionen zu einem Cluster
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Der erste Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.

Der zweite Befehl verwendet das Cmdlet **Add-AzureHDInsightScriptAction** , um die angegebene Skript Aktion zu $config hinzuzufügen, und verwendet dann den Pipelineoperator, um $config an **Add-AzureHDInsightScriptAction** ein zweites Mal zu übergeben, um $config eine zweite Skript Aktion hinzuzufügen.

Der endgültige Befehl verwendet das Cmdlet **New-AzureHDInsightCluster** zum Erstellen eines Clusters, in dem die Skriptaktionen in $config ausgeführt werden.

## Parameter

### -ClusterRoleCollection
Gibt die Knoten an, für die ein Skript ausgeführt werden soll.
Die zulässigen Werte für diesen Parameter sind: HeadNode oder datanode.

Sie können einen oder beide Werte angeben.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Gibt ein Configuration-Objekt an.
Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, Skript Aktionsinformationen hinzu.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Gibt den Namen einer Skript Aktion an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
Gibt die Parameter an, die für eine Skript Aktion erforderlich sind.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
Gibt den URI-Speicherort eines Skripts an, das ausgeführt werden soll.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Neu – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


