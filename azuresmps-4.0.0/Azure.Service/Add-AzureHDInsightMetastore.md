---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005929"
---
# Add-AzureHDInsightMetastore

## Synopsis
Fügt ein SQL Server-Daten Bank Konto zu einer HDInsight-Cluster Konfiguration hinzu.

## Syntax

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Das Cmdlet **Add-AzureHDInsightMetastore** fügt eine Microsoft SQL Server-Datenbank zu einer Azure HDInsight-Konfiguration hinzu, die vom Cmdlet **New-AzureHDInsightClusterConfig** erstellt wird.
Die Datenbank wird zum Speichern von Metadaten für Hive-oder Oozie oder beides verwendet.

## Beispiele

### Beispiel 1: Hinzufügen eines metastores
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

Dieser Befehl fügt eine SQL Server-Datenbank mit dem Namen ContosoSQLServer hinzu, die als Hive-metastore für einen HDInsight-Cluster fungieren soll.

### Beispiel 2: Konfigurieren des Speichers und Hinzufügen von metastores
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
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

### -Config
Gibt ein Configuration-Objekt an.
Dieses Cmdlet fügt dem Configuration-Objekt metastore-Informationen hinzu, die dieser Parameter angibt.

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

### – Anmeldeinformationen
Gibt die Anmeldeinformationen an, die für den Zugriff auf eine SQL Server-Datenbank verwendet werden.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Gibt den Namen der Datenbank an, in der die Hive-oder Oozie-Metadaten gespeichert werden.

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

### -Metastoretype
Gibt den metastore-Typ an.
Die zulässigen Werte für diesen Parameter sind: HiveMetaStore oder OozieMetaStore.

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
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

### -SqlAzureServerName
Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des SQL Server an, der die Datenbank zum Speichern von Metadaten enthält.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Add-AzureHDInsightStorage](./Add-AzureHDInsightStorage.md)

[Neu – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Neu – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Satz-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
