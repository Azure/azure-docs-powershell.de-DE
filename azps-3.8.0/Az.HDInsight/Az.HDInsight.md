---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: 1a4413056e7658b81501067d3c0148951c05c235
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847583"
---
# AZ. HDInsight-Modul
## Beschreibung
In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets für Microsoft Azure HDInsight im Azure Resource Manager (Arm)-Framework dokumentiert. Diese Cmdlets werden zum Verwalten von HDInsight-Clustern und den darauf ausgeführten Aufträgen verwendet. Die Cmdlets sind im Microsoft. Azure. Commands. HDInsight-Namespace vorhanden.

## AZ. HDInsight-Cmdlets
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Fügt einem Cluster Konfigurationsobjekt eine Clusteridentität hinzu.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Fügt eine Version für einen in einem Cluster ausgeführten Dienst zu einem Cluster Konfigurationsobjekt hinzu.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Fügt einem Cluster Konfigurationsobjekt eine Anpassung der Hadoop-Konfigurationswerte und/oder eine freigegebene Hive-Bibliothek hinzu.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Fügt eine SQL-Datenbank hinzu, die als Hive-oder Oozie-metastore für ein Cluster Konfigurationsobjekt fungieren soll.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Fügt einem Cluster Konfigurationsobjekt eine Skript Aktion hinzu.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Fügt einem Cluster Konfigurationsobjekt ein Sicherheitsprofil hinzu.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Fügt einen Azure-Speicherschlüssel zu einem Cluster-Konfigurationsobjekt hinzu.

### [Deaktivieren-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Deaktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden nicht mehr in den während der Aktivierung angegebenen Überwachungs Arbeitsbereich überfließen.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Aktiviert die Überwachung in einem HDInsight-Cluster, und relevante Protokolle werden an den während der Aktivierung angegebenen Überwachungs Arbeitsbereich gesendet.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Ruft alle Azure HDInsight-Cluster ab, die dem aktuellen Abonnement oder einer angegebenen Ressourcengruppe zugeordnet sind, oder Ruft einen bestimmten Cluster ab.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder Ruft einen bestimmten Auftrag ab.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Ruft den Status der überwachungsinstallation auf dem Cluster ab.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Ruft die beibehaltenen Skriptaktionen für einen Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Ruft Eigenschaften des HDInsight-Diensts ab, beispielsweise Verfügbare Speicherorte und Kapazität.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Ruft den Skript Aktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Sendet eine Hive-Abfrage an einen HDInsight-Cluster und ruft Abfrageergebnisse in einem Vorgang ab.

### [Neu – AzHDInsightCluster](New-AzHDInsightCluster.md)
Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.

### [Neu – AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.

### [Neu – AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Erstellt ein Hive-Auftragsobjekt.

### [Neu – AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Erstellt ein MapReduce-Auftragsobjekt.

### [Neu – AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Erstellt ein Pig-Auftragsobjekt.

### [Neu – AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Erstellt ein Sqoop-Auftragsobjekt.

### [Neu – AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Erstellt ein Streaming-MapReduce-Auftragsobjekt.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Entfernt den angegebenen HDInsight-Cluster aus dem aktuellen Abonnement.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Entfernt eine beibehaltene Skript Aktion aus einem HDInsight-Cluster.

### [Satz-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Legt die Anzahl der Arbeitskraft Knoten in einem angegebenen Cluster fest.

### [Satz-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Legt die Standardeinstellung für das Speicherkonto in einem Cluster Konfigurationsobjekt fest.

### [Satz-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Legt die Gateway-http-Anmeldeinformationen eines Azure HDInsight-Clusters fest.

### [Satz-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.

### [Anfang-AzHDInsightJob](Start-AzHDInsightJob.md)
Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.

### [Stopp-AzHDInsightJob](Stop-AzHDInsightJob.md)
Beendet einen angegebenen ausgeführten Auftrag in einem Cluster.

### [Submit-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.

### [Verwenden von-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Wählt einen Cluster aus, der mit dem Invoke-RmAzureHDInsightHiveJob-Cmdlet verwendet werden soll.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.

