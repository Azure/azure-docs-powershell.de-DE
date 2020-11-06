---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: bbbb418a8e101fa1b806bc910132f44e40158190
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474093"
---
# AzureRM. HDInsight-Modul
## Beschreibung
In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets für Microsoft Azure HDInsight im Azure Resource Manager (Arm)-Framework dokumentiert. Diese Cmdlets werden zum Verwalten von HDInsight-Clustern und den darauf ausgeführten Aufträgen verwendet. Die Cmdlets sind im Microsoft. Azure. Commands. HDInsight-Namespace vorhanden.

## AzureRM. HDInsight-Cmdlets
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Fügt einem Cluster Konfigurationsobjekt eine Clusteridentität hinzu.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Fügt eine Version für einen in einem Cluster ausgeführten Dienst zu einem Cluster Konfigurationsobjekt hinzu.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Fügt einem Cluster Konfigurationsobjekt eine Anpassung der Hadoop-Konfigurationswerte und/oder eine freigegebene Hive-Bibliothek hinzu.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Fügt eine SQL-Datenbank hinzu, die als Hive-oder Oozie-metastore für ein Cluster Konfigurationsobjekt fungieren soll.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Fügt einem Cluster Konfigurationsobjekt eine Skript Aktion hinzu.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Fügt ein Security profileo-Cluster-Konfigurationsobjekt hinzu.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Fügt einen Azure-Speicherschlüssel zu einem Cluster-Konfigurationsobjekt hinzu.

### [Deaktivieren-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Deaktiviert die Operations Management Suite (OMS) in einem HDInsight-Cluster, und relevante Protokolle werden nicht mehr in den OMS-Arbeitsbereich fließen, der während der Aktivierung angegeben wird.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Aktiviert die Operations Management Suite (OMS) in einem HDInsight-Cluster, und relevante Protokolle werden an den OMS-Arbeitsbereich gesendet, der während der Aktivierung angegeben wird.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Ruft alle Azure HDInsight-Cluster ab, die dem aktuellen Abonnement oder einer angegebenen Ressourcengruppe zugeordnet sind, oder Ruft einen bestimmten Cluster ab.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Ruft die Liste der Aufträge aus einem Cluster ab und listet sie in umgekehrter chronologischer Reihenfolge auf oder Ruft einen bestimmten Auftrag ab.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Ruft die Protokollausgabe für einen Auftrag aus dem Speicherkonto ab, das einem angegebenen Cluster zugeordnet ist.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Ruft den Status der Operation Management Suite (OMS)-Installation auf dem Cluster ab.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Ruft die beibehaltenen Skriptaktionen für einen Cluster ab und listet sie in chronologischer Reihenfolge auf oder ruft Details für eine angegebene permanente Skript Aktion ab.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
Ruft Eigenschaften des HDInsight-Diensts ab, beispielsweise Verfügbare Speicherorte und Kapazität.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Ruft den Skript Aktionsverlauf für einen Cluster ab und listet ihn in umgekehrter chronologischer Reihenfolge auf oder ruft Details einer zuvor ausgeführten Skript Aktion ab.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Gewährt dem Cluster HTTP-Zugriff.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Gewährt RDP-Zugriff auf den Windows-Cluster.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Sendet eine Hive-Abfrage an einen HDInsight-Cluster und ruft Abfrageergebnisse in einem Vorgang ab.

### [Neu – AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Erstellt einen Azure HDInsight-Cluster in der angegebenen Ressourcengruppe für das aktuelle Abonnement.

### [Neu – AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.

### [Neu – AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Erstellt ein Hive-Auftragsobjekt.

### [Neu – AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
Erstellt ein MapReduce-Auftragsobjekt.

### [Neu – AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Erstellt ein Pig-Auftragsobjekt.

### [Neu – AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Erstellt ein Sqoop-Auftragsobjekt.

### [Neu – AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Erstellt ein Streaming-MapReduce-Auftragsobjekt.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Entfernt den angegebenen HDInsight-Cluster aus dem aktuellen Abonnement.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Entfernt eine beibehaltene Skript Aktion aus einem HDInsight-Cluster.

### [REVOKE-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Deaktiviert den HTTP-Zugriff auf den Cluster.

### [REVOKE-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Deaktiviert den RDP-Zugriff auf einen Windows-Cluster.

### [Satz-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Legt die Anzahl der Arbeitskraft Knoten in einem angegebenen Cluster fest.

### [Satz-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Legt die Standardeinstellung für das Speicherkonto in einem Cluster Konfigurationsobjekt fest.

### [Satz-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Legt eine zuvor ausgeführte Skript Aktion als permanente Skript Aktion fest.

### [Anfang-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Startet einen definierten Azure HDInsight-Auftrag in einem angegebenen Cluster.

### [Stopp-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Beendet einen angegebenen ausgeführten Auftrag in einem Cluster.

### [Submit-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Sendet eine neue Skript Aktion an einen Azure HDInsight-Cluster.

### [Verwenden von-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Wählt einen Cluster aus, der mit dem Invoke-RmAzureHDInsightHiveJob-Cmdlet verwendet werden soll.

### [Wait-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Wartet auf den Abschluss oder Fehler eines angegebenen Auftrags.

