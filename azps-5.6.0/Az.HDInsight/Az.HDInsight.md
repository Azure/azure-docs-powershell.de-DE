---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: ec924f7424d2b522e6bbd9ce1db51e8c920ec663
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938091"
---
# Az.HDInsight-Modul
## Beschreibung
Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets für Microsoft Azure HDInsight im Azure Resource Manager (ARM)-Framework. Diese Cmdlets werden verwendet, um HDInsight-Cluster und die Aufträge zu verwalten, die auf diesen Clustern ausgeführt werden. Die Cmdlets sind im Microsoft.Azure.Commands.HDInsight-Namespace vorhanden.

## Az.HDInsight-Cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Fügt einem Clusterkonfigurationsobjekt eine Clusteridentität hinzu.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Fügt einem Clusterkonfigurationsobjekt eine Version für einen Dienst hinzu, der in einem Cluster ausgeführt wird.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Fügt einem Clusterkonfigurationsobjekt eine Anpassung des Hadoop-Konfigurationswerts und/oder eine Hive-Bibliotheksanpassung hinzu.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Fügt eine SQL-Datenbank hinzu, die einem Clusterkonfigurationsobjekt als Hive- oder Oozie-Metastore dienen soll.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Fügt einem Clusterkonfigurationsobjekt eine Skriptaktion hinzu.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Fügt einem Clusterkonfigurationsobjekt ein Sicherheitsprofil hinzu.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Fügt einem Clusterkonfigurationsobjekt einen Azure Storage-Schlüssel hinzu.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich, der während der Aktivierung angegeben wurde.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Aktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden an den Überwachungsarbeitsbereich gesendet, der während der Aktivierung angegeben wurde.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Ruft alle Azure HDInsight-Cluster ab und auf, die dem aktuellen Abonnement oder einer angegebenen Ressourcengruppe zugeordnet sind, oder ruft einen bestimmten Cluster ab.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Ruft die Konfiguration der automatischen Skalierung des HDInsight-Clusters ab.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Listet die Hosts des HDInsight-Clusters auf.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder ruft einen bestimmten Auftrag ab.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Ruft den Status der Überwachung der Installation im Cluster ab.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Ruft die beibehaltenen Skriptaktionen für einen Cluster ab und listet sie in chronologischer Reihenfolge auf, oder ruft Details für eine angegebene Aktion für persistierte Skripts ab.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Ruft Eigenschaften zum HDInsight-Dienst ab, z. B. verfügbare Speicherorte und Kapazität.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Ruft den Skriptaktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf, oder ruft Details einer zuvor ausgeführten Skriptaktion ab.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Sendet eine Hive-Abfrage an einen HDInsight-Cluster und ruft Abfrageergebnisse in einem Einzigen Vorgang ab.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Erstellt ein nicht persistiertes Objekt, das die Konfiguration der automatischen Skalierung eines Azure HDInsight-Clusters beschreibt.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Erstellt eine terminplanbasierte Bedingung für die automatische Skalierung.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Erstellt ein nicht persistiertes Clusterkonfigurationsobjekt, das eine Azure HDInsight-Clusterkonfiguration beschreibt.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Erstellt ein Hive-Auftragsobjekt.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Erstellt ein MapReduce-Auftragsobjekt.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Erstellt ein Schweinauftragsobjekt.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Erstellt ein Sqoop-Auftragsobjekt.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Erstellt ein Streaming MapReduce-Auftragsobjekt.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Entfernt den angegebenen HDInsight-Cluster aus dem aktuellen Abonnement.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Entfernt die Konfiguration der automatischen Skalierung des HDInsight-Clusters.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Entfernt eine persistierte Skriptaktion aus einem HDInsight-Cluster.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Startet die spezifischen Hosts des HDInsight-Clusters neu.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Legt die Konfiguration der automatischen Skalierung eines Azure HDInsight-Clusters fest.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Dreht den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Clusters.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Legt die Anzahl der Workerknoten in einem angegebenen Cluster fest.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Legt die Standardeinstellung für das Speicherkonto in einem Clusterkonfigurationsobjekt fest.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Legt die GATEWAY-HTTP-Anmeldeinformationen eines Azure HDInsight-Clusters fest.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Legt eine zuvor ausgeführte Skriptaktion so fest, dass sie eine aktion für ein beibehaltenes Skript ist.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Beendet einen angegebenen ausgeführten Auftrag in einem Cluster.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Sendet eine neue Skriptaktion an einen Azure HDInsight-Cluster.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Wählt einen Cluster aus, der mit dem cmdlet Invoke-RmAzureHDInsightHiveJob werden soll.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.

