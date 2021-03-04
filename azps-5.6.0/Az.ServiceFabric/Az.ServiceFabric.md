---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924427"
---
# Az.ServiceFabric-Modul
## Beschreibung
Azure Service Fabric-Modul, mit dem Sie die End-2-End-Vorgänge automatisieren können, z. B. das Erstellen eines sicheren Clusters, das Roll over-Clusterzertifikat, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. Die vollständige Liste aller Vorgänge ist unten aufgeführt.

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Fügen Sie dem Cluster zu Clientauthentifizierungszwecken allgemeinen Namen oder Fingerabdruck hinzu.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Fügen Sie dem Cluster ein sekundäres Clusterzertifikat hinzu.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Fügen Sie dem Cluster gemeinsamen Namen oder Fingerabdruck des Zertifikats hinzu. Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Fügen Sie dem Knotentyp die Erweiterung vm hinzu.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Fügen Sie dem Knotentyp den Zertifikatsgeheimnis hinzu.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Fügen Sie dem bestimmten Knotentyp im Cluster Knoten hinzu.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Fügen Sie dem vorhandenen Cluster einen neuen Knotentyp hinzu.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Details zur Service Fabric-Anwendung.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Details zum Service Fabric-Anwendungstyp.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Details zur Version des Service Fabric-Anwendungstyps.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Hier erhalten Sie die Details zu den Clusterressourcen.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Hier erhalten Sie die Ressourcendetails für verwaltete Cluster.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Holen Sie sich die Ressourcendetails für den verwalteten Knotentyp.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Holen Sie sich Service Fabric-Dienstdetails unter der angegebenen Anwendung und dem angegebenen Cluster.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Erstellen Sie einen neuen Service Fabric-Anwendungstyp unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Erstellen Sie eine neue Anwendungstypversion unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder systemgenerierte selbst signierte Zertifikate, um einen neuen Service Fabric-Cluster zu erstellen. Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen. Sie haben die Möglichkeit, einen Ordner anzugeben, in den die selbst signierten Zertifikate exportiert oder später aus dem Schlüsseltresor abgerufen werden sollen.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Erstellen Sie einen neuen verwalteten Cluster.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Erstellen Sie eine neue Knotentypressource.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Erstellen Sie einen neuen Service Fabric-Dienst unter der angegebenen Anwendung und dem angegebenen Cluster.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Entfernen Sie eine Anwendung aus dem Cluster. Dadurch werden alle Dienste unter der Anwendung entfernt.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Entfernen Sie service fabric einen Anwendungstyp aus dem Cluster. Dadurch werden alle Typversionen unter dieser Ressource entfernt.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Entfernen sie eine Anwendungstypversion aus dem Cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Entfernen Sie die Namen von Clientzertifikaten oder Zertifikatsubjekten aus der Verwendung für die Clientauthentifizierung im Cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Entfernen Sie ein Clusterzertifikat aus der Verwendung für die Clustersicherheit.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Entfernen Sie die Clusterressource.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe client certificate by thumbprint or common name.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Entfernen Sie die Vm-Erweiterung aus dem Knotentyp.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Entfernen eines vollständigen Knotentyps aus einem Cluster

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Entfernen eines Diensts aus dem Cluster

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Entfernen Sie eine oder mehrere Service Fabric-Einstellungen aus dem Cluster.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Starten Sie bestimmte Knoten vom Knotentyp neu.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Festlegen von Clusterressourceneigenschaften

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Ndes des Knotentyps mit dem Parameter -Reimage aus.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändern Sie den Service Fabric-Upgradetyp des Clusters.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aktualisieren einer Service Fabric-Anwendung Dadurch können die Anwendungsparameter aktualisiert und/oder die Anwendungstypversion aktualisiert werden, wodurch ein Anwendungsupgrade ausgelöst wird.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualisieren Sie die Lebensdauerebene oder vmSku eines Knotentyps im Cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualisieren Sie die Zuverlässigkeitsebene des primären Knotentyps in einem Cluster.

