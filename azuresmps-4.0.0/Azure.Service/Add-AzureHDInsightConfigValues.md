---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005934"
---
# Add-AzureHDInsightConfigValues

## Synopsis
Fügt einer HDInsight-Cluster Konfiguration eine Anpassung des Hadoop-Konfigurationswerts oder eine freigegebene Hive-Bibliothek hinzu.

## Syntax

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).

Das **Add-AzureHDInsightConfigValues-** Cmdlet fügt eine Anpassung des Hadoop-Konfigurationswerts wie Core-site.xml oder Hive-site.xml oder eine freigegebene Bibliothek für eine Hive-Konfiguration zu einer Azure HDInsight-Cluster Konfiguration hinzu.

Das Cmdlet fügt einem angegebenen Konfigurationsobjekt benutzerdefinierte Konfigurationswerte hinzu.
Die benutzerdefinierten Einstellungen werden den Konfigurationsdateien der relevanten Hadoop-Dienste hinzugefügt, wenn der Cluster bereitgestellt wird.

## Beispiele

### Beispiel 1: Konfigurieren eines Clusters
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

Der erste Befehl erstellt ein neues **AzureHDInsightHiveConfiguration** -Objekt und speichert es dann in der $HiveConfigValues-Variablen.

Die nächsten fünf Befehle erstellen Konfigurationswerte für Hive und speichern diese Werte als Mitglieder von $HiveConfigValues.

Der siebte Befehl erstellt ein **AzureHDInsightOozieConfiguration** -Objekt und speichert es dann in der $OozieConfigValues-Variablen.
Der achte Befehl erstellt einen Konfigurationswert für Oozie und speichert diese Werte dann als Mitglied von $OozieConfigValues.

Der neunte Befehl erstellt ein **AzureHDInsightMapReduceConfiguration** -Objekt und speichert es dann in der $MapredConfigValues-Variablen.
Die nächsten beiden Befehle erstellen Konfigurationswerte für MapReduce und speichern diese Werte als Mitglieder von $MapredConfigValues.

Der zwölfte Befehl verwendet das Cmdlet **New-AzureHDInsightClusterConfig** , um eine HDInsight-Cluster Konfiguration zu erstellen, und speichert Sie dann in der $config-Variablen.
Der Befehl übergibt $config an das Cmdlet " **AzureHDInsightDefaultStorage** ", um die Standardspeichereinstellung und das Cmdlet " **Add-AzureHDInsightConfigValues** " zu aktualisieren, um die neuen Konfigurationswerte zur Cluster Konfiguration hinzuzufügen.

Der endgültige Befehl verwendet den Pipelineoperator, um $config an das Cmdlet **New-AzureHDInsightCluster** zu übergeben, um einen neuen HDInsight-Cluster mit den angepassten Einstellungen zu erstellen.

## Parameter

### -Config
Gibt das Configuration-Objekt an, dem eine Hadoop-Konfiguration hinzugefügt werden soll.

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

### -Core
Gibt einen Satz von Hadoop-Konfigurationswerten für Core-site.xml an.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HBAs
Gibt einen Satz von HBAs-Konfigurationswerten für Hbase-site.xml an.

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HDFS
Gibt einen Satz von Hadoop-Konfigurationswerten für Hdfs-site.xml an.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hive
Gibt ein Anpassungs Objekt für den Hadoop-hivedienst an, einschließlich einer Reihe von Hadoop-Konfigurationswerten für Hive-site.xml-und Hive-freigegebene Bibliotheken.

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapReduce
Gibt ein Anpassungs Objekt für MapReduce und den Kapazitätsplaner an.

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Oozie
Gibt ein Anpassungs Objekt für den Hadoop-Oozie-Dienst an, einschließlich einer Reihe von Hadoop-Konfigurationswerten für Oozie-site.xml.

```yaml
Type: AzureHDInsightOozieConfiguration
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

### -Funken
Gibt ein Anpassungs Objekt für Apache Spark an.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Storm
Gibt ein Anpassungs Objekt für Apache Storm an.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Garn
Gibt ein Anpassungs Objekt für Hadoop-Garn an und gibt einen Satz angepasster Garn Konfigurationswerte für Yarn-site.xml an.

```yaml
Type: Hashtable
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

[Neu – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Neu – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)

[Satz-AzureHDInsightDefaultStorage](./Set-AzureHDInsightDefaultStorage.md)
