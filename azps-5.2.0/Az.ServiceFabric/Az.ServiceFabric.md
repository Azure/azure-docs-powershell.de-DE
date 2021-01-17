---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303024"
---
# Az.ServiceFabric Module
## Beschreibung
Azure Service Fabric Module, das Sie zum Automatisieren der End-2-End-Vorgänge verwenden können, z. B. erstellen eines sicheren Cluster, Rolling über Clusterzertifikate, Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. Die vollständige Liste aller Vorgänge ist unten aufgeführt.

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Fügen Sie dem Cluster zu Clientauthentifizierungszwecken allgemeinen Namen oder Fingerabdrück hinzu.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Fügen Sie dem Cluster ein Zertifikat für einen sekundären Cluster hinzu.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Fügen Sie dem Cluster einen allgemeinen Zertifikatnamen oder Einen Fingerabdruck hinzu. Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Fügen Sie dem Knotentyp die Erweiterung "vm" hinzu.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Fügen Sie dem Knotentyp einen geheimen Zertifikattyp hinzu.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Fügen Sie dem jeweiligen Knotentyp im Cluster Knoten hinzu.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Fügen Sie dem vorhandenen Cluster einen neuen Knotentyp hinzu.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Erhalten Sie Service Fabric-Anwendungsdetails.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Get Service Fabric application type details.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Get Service Fabric application type version details.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Erhalten Sie die Details der Clusterressourcen.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Erhalten Sie die Details der verwalteten Clusterressourcen.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Ressourcendetails für verwaltete Knotentypen

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Service Fabric service details under the specified application and cluster.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Create new service fabric application under the specified resource group and cluster.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Create new service fabric application type under the specified resource group and cluster.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Erstellen Sie eine neue Anwendungstypversion unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder vom System generierte selbst signierte Zertifikate zum Einrichten eines neuen Service Fabric Cluster. Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen. Sie können einen Ordner angeben, in den die selbst signierten Zertifikate exportiert werden sollen, oder sie später aus dem Schlüsseltresor abrufen.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Erstellen Sie einen neuen verwalteten Cluster.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Erstellen sie eine neue Knotentypressource.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Create new service fabric service under the specified application and cluster.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Entfernen Sie eine Anwendung aus dem Cluster. Dadurch werden alle Dienste unter der Anwendung entfernt.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Remove Service fabric an application type from the cluster. Dadurch werden alle Typversionen unter dieser Ressource entfernt.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Remove Service fabric an application type version from the cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Entfernen Sie die Namen von Clientzertifikaten oder Zertifikatsubjekten aus der Verwendung für die Clientauthentifizierung im Cluster.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Entfernen Sie ein Clusterzertifikat aus der Verwendung für cluster-Sicherheit.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Entfernen Sie die Clusterressource.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen ab.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Entfernen Sie die erweiterung "vm" aus dem Knotentyp.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Entfernen eines vollständigen Knotentyps aus einem Cluster

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Entfernen sie einen Dienst aus dem Cluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Remove one or multiple Service Fabric setting from the cluster.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Starten Sie bestimmte Knoten vom Knotentyp neu.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Legen Sie Clusterressourceneigenschaften festgelegt.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Typen des Knotentyps mit dem Parameter "-Reimage" aus.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändern Sie den Service Fabric-Upgradetyp des Clusters.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aktualisieren Sie eine Service Fabric-Anwendung. Dadurch können die Anwendungsparameter aktualisiert und/oder die Anwendungstypversion aktualisiert werden, wodurch ein Anwendungsupgrade ausgelöst wird.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualisieren Sie das kontingente Tier oder vmSku eines Knotentyps im Cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualisieren Sie die Zuverlässigkeitsstufen des primären Knotentyps in einem Cluster.

