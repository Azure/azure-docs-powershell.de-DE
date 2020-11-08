---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006126"
---
# New-AzureHDInsightClusterConfig

## Synopsis
Erstellt eine nicht persistente HDInsight-Cluster Konfiguration.

## Syntax

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Das Cmdlet **New-AzureHDInsightClusterConfig** erstellt eine nicht persistente Azure HDInsight-Cluster Konfiguration.

## Beispiele

### Beispiel 1: Erstellen einer Cluster Konfiguration
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.

Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.

Der vierte, fünfte und sechste Befehl verwenden Sie das Cmdlet **Get-Credential** , um Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive abzurufen, und speichern Sie dann die Anmeldeinformationen in Variablen.

Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus: 

- **New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration.
- **Legen Sie AzureHDInsightDefaultStorage** , um das Standardspeicher Konto für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net zu legen.
- **Add-AzureHDInsightStorage** , um der Konfiguration ein zweites Speicherkonto mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net hinzuzufügen.
- **Add-AzureHDInsightMetastore** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen.
- **New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration.

## Parameter

### -ClusterSizeInNodes
Gibt die Anzahl der Datenknoten an, die für einen Cluster erstellt werden sollen.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Clustertyp
Gibt den Typ des zu erstellende Clusters an.

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataNodeVMSize
Gibt die Größe des virtuellen Computers für den Datenknoten an.

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

### -HeadNodeVMSize
Gibt die Größe des virtuellen Computers des Head-Knotens für den Cluster an.

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

### -SubnetName
Gibt den Namen eines Subnetzes an.

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

### -VirtualNetworkId
Gibt die ID des virtuellen Netzwerks an, in das der Cluster bereitgestellt werden soll.

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

### -ZookeeperNodeVMSize
Gibt die Größe des virtuellen Computers für den zoowärter-Knoten für einen HBAs oder Storm-Cluster an.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureHDInsightMetastore](./Add-AzureHDInsightMetastore.md)

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[Neu – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Satz-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)


