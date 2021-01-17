---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469699"
---
# Az.HDInsight Module
## Beschreibung
Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets für Microsoft Azure HDInsight im Azure Resource Manager (ARM)-Framework. Diese Cmdlets werden zum Verwalten von HDInsight-Clustern und der Aufträge verwendet, die auf ihnen ausgeführt werden. Die Cmdlets sind im Namespace "Microsoft.Azure.Commands.HDInsight" vorhanden.

## Az.HDInsight-Cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Fügt einem Clusterkonfigurationsobjekt eine Clusteridentität hinzu.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Fügt einem Clusterkonfigurationsobjekt eine Version für einen Dienst hinzu, der in einem Cluster ausgeführt wird.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Fügt einem Clusterkonfigurationsobjekt eine Anpassung des Werts für die Konfiguration von Hadoop und/oder eine Anpassung der freigegebenen Strukturbibliothek hinzu.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Fügt eine SQL Datenbank hinzu, die als Struktur- oder Oozie-Metastore zu einem Clusterkonfigurationsobjekt dienen soll.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Fügt einem Clusterkonfigurationsobjekt eine Skriptaktion hinzu.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Fügt einem Clusterkonfigurationsobjekt ein Sicherheitsprofil hinzu.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Fügt einem Clusterkonfigurationsobjekt einen Azure Storage Key hinzu.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle fließen nicht mehr zum Überwachungsarbeitsbereich, der während der Aktivierung angegeben wurde.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Aktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden an den Überwachungsarbeitsbereich gesendet, der während der Aktivierung angegeben wurde.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Ruft alle Azure -HDInsight-Cluster ab, die dem aktuellen Abonnement oder einer bestimmten Ressourcengruppe zugeordnet sind, und listet sie auf, oder ruft einen bestimmten Cluster ab.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Ruft die Autoskalenkonfiguration des Cluster "HDInsight" ab.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Listet die Hosts des Cluster "HDInsight" auf.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder ruft einen bestimmten Auftrag ab.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Ruft den Status der Überwachung der Installation für den Cluster ab.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Ruft die Aktionen für beibehaltene Skripts für einen Cluster ab und listet sie in chronologischer Reihenfolge auf, oder ruft Details zu einer angegebenen Aktion für beibehaltene Skripts ab.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Ruft Eigenschaften zum Dienst HDInsight ab, z. B. verfügbare Standorte und Kapazität.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Ruft den Skriptaktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf, oder ruft Details einer zuvor ausgeführten Skriptaktion ab.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Übermittelt eine Strukturabfrage an einen HDInsight-Cluster und ruft die Abfrageergebnisse in einem Vorgang ab.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Erstellt einen Azure -HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Erstellt ein nicht beibehaltenes Objekt, das die Konfiguration der automatischen Skalierung eines Azure -HDInsight-Cluster beschreibt.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Erstellt eine terminplanbasierte Autoskalen-Bedingung.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Erstellt ein nicht beibehaltenes Clusterkonfigurationsobjekt, das eine Konfiguration des Azure -HDInsight-Cluster beschreibt.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Erstellt ein Objekt für einen Strukturauftrag.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Erstellt ein Auftragsobjekt von MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Erstellt ein Objekt für einen Schweinauftrag.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Erstellt ein Sqoop-Auftragsobjekt.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Erstellt ein Streaming-MapReduce-Auftragsobjekt.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Entfernt den angegebenen Cluster "HDInsight" aus dem aktuellen Abonnement.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Entfernt die Konfiguration der Automatischskala des HDInsight-Cluster.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Entfernt eine Aktion für beibehaltene Skripts aus einem HDInsight-Cluster.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Startet die spezifischen Hosts des HDInsight-Cluster neu.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Legt die Konfiguration der automatischen Skalierung eines Azure -HDInsight-Cluster fest.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Dreht den Datenträgerverschlüsselungsschlüssel des angegebenen HDInsight-Cluster.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Legt die Anzahl der Workerknoten in einem angegebenen Cluster fest.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Legt die Standardeinstellung für das Speicherkonto in einem Clusterkonfigurationsobjekt fest.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Legt die Gateway-HTTP-Anmeldeinformationen eines Azure -HDInsight-Cluster fest.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Legt eine zuvor ausgeführte Skriptaktion als aktion für beibehaltene Skripts fest.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Startet einen definierten Azure -HDInsight-Auftrag für einen angegebenen Cluster.

### [Stop-AzHDInsightJob](Stop-AzHDInsightJob.md)
Beendet einen angegebenen ausgeführten Auftrag für einen Cluster.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Übermittelt eine neue Skriptaktion an einen Azure HDInsight-Cluster.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Wählt einen Cluster aus, der mit dem cmdlet Invoke-RmAzureHDInsightHiveJob werden soll.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.

