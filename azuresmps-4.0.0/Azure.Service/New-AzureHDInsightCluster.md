---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006129"
---
# New-AzureHDInsightCluster

## Synopsis
Erstellt einen HDInsight-Cluster.

## Syntax

### Cluster nach config (mit bestimmten Anmeldeinformationen für Abonnements) (Standard)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Cluster nach Name (mit bestimmten Anmeldeinformationen für Abonnements)
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Mit dem Cmdlet **New-AzureHDInsightCluster** wird ein Azure HDInsight-Cluster mithilfe der angegebenen Parameter oder mithilfe eines Konfigurationsobjekts erstellt, das mit dem Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.

## Beispiele

### Beispiel 1: Erstellen eines HDInsight-Clusters
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

In diesem Beispiel wird ein HDInsight-Cluster für das aktuelle Abonnement erstellt.

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

### -Zertifikat
Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClusterSizeInNodes
Gibt die Anzahl der Datenknoten an, die für einen Cluster erstellt werden sollen.

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
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
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Gibt ein Configuration-Objekt an, das mit dem Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt die Benutzeranmeldeinformationen an, die HDInsight für das Standardkonto verwenden soll, das für den Remotezugriff auf einen Hadoop-Cluster verwendet wird.
Diese Anmeldeinformationen unterscheiden sich von den Abonnement Anmeldeinformationen des Benutzers.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataNodeVMSize
Gibt die Größe des virtuellen Computers für den Datenknoten an.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountKey
Gibt den Kontoschlüssel für das Standardspeicher Konto an, das vom HDInsight-Cluster verwendet wird.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageContainerName
Gibt den Namen des Standardcontainers im standardmäßigen Azure Storage-Konto an, das ein HDInsight-Cluster verwendet.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunkt
Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeadNodeVMSize
Gibt die Größe des virtuellen Computers für den Head-Knoten an.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Gibt den Namespace eines HDInsight-Diensts an.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardnamespace.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Gibt den Bereich an, in dem ein HDInsight-Cluster erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Azure HDInsight-Clusters an, den Sie erstellen möchten.

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Gibt das Betriebssystem für einen Cluster an.

```yaml
Type: OSType
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

### -RdpAccessExpiry
Gibt den Ablauf als **DateTime** -Objekt für den Zugriff auf einen Cluster mit Remote Desktop Protokoll (RDP) an.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RdpCredential
Gibt die Anmeldeinformationen für den RDP-Zugriff auf einen Cluster an.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshCredential
Gibt den Benutzernamen und das Kennwort für Secure Shell (SSH) für den HDInsight-Cluster an.
Dieser Parameter ist nur für Linux-Cluster gültig.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SshPublicKey
Gibt den öffentlichen SSH-Schlüssel für einen HDInsight-Cluster an.
Dieser Parameter ist nur für Linux-Cluster gültig.

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

### -SubnetName
Gibt den Namen eines Subnetzes an.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement
Gibt das Azure-Abonnement an, in dem ein HDInsight-Cluster erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Gibt die HDInsight-Clusterversion an, die erstellt werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

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
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZookeeperNodeVMSize
Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.
Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
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

[Get-AzureHDInsightCluster](./Get-AzureHDInsightCluster.md)

[Neu – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Remove-AzureHDInsightCluster](./Remove-AzureHDInsightCluster.md)

[Satz-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)

[Verwenden von-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


