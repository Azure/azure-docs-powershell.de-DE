---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005922"
---
# Add-AzureHDInsightStorage

## Synopsis
Fügt einen BLOB-Speicherkonto Eintrag zu einer HDInsight-Konfiguration hinzu.

## Syntax

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Mit dem Cmdlet **Add-AzureHDInsightStorage** wird eine Azure HDInsight-Konfiguration ein BLOB-Speicherkonto Eintrag hinzugefügt.

## Beispiele

### Beispiel 1: Hinzufügen eines speicherkontos
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

Dieser Befehl fügt dem in $config gespeicherten Konfigurationsobjekt ein Speicherkonto mit dem Namen mystorage hinzu und speichert dann die Konfiguration in der $StoreConfig Variablen.

### Beispiel 2: Konfigurieren mehrerer Speicherkonten
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

Der erste Befehl verwendet das Cmdlet " **Get-AzureSubscription** ", um die aktuelle Abonnement-ID abzurufen, und speichert Sie dann in der $SubId-Variablen.

Der zweite und der dritte Befehl verwenden das Cmdlet " **Get-AzureStorageKey** ", um die primären Speicherschlüssel für MyBlobStorage und MySecondBlobStorage abzurufen, und speichern Sie dann die Schlüssel in den Variablen $Key 1 und $Key 2.

Der vierte, fünfte und sechste Befehl erhält die Anmeldeinformationen für das aktuelle Abonnement sowie für Oozie und Hive und speichert die Anmeldeinformationen dann in Variablen.

Der endgültige Befehl führt eine Abfolge von Vorgängen mithilfe dieser Cmdlets aus:

- **New-AzureHDInsightClusterConfig** zum Erstellen einer HDInsight-Cluster Konfiguration
- **Festlegen von AzureHDInsightDefaultStorage** zum Festlegen des Standardspeicher Kontos für die Konfiguration auf MyBlobStorage.BLOB.Core.Windows.net
- **Add-AzureHDInsightStorage** zum Hinzufügen eines zweiten speicherkontos mit dem Namen MySecondBlobStorage.BLOB.Core.Windows.net zur Konfiguration
- **Add-AzureHDInsightStorage** , um der Konfiguration einen metastore für Oozie und einen metastore für Hive hinzuzufügen
- **New-AzureHDInsightCluster** zum Erstellen eines HDInsight-Clusters mit der neuen Konfiguration

## Parameter

### -Config
Gibt ein Configuration-Objekt an.
Dieses Cmdlet fügt dem Objekt, das dieser Parameter angibt, Speicherkonto Informationen hinzu.

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

### -StorageAccountKey
Gibt den speicherkontoschlüssel an, der für den Zugriff auf ein Speicherkonto verwendet wird.

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

### -StorageAccountName
Gibt den Namen des Azure-speicherkontos an, das hinzugefügt werden soll.

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

[Neu – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Neu – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Satz-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)


