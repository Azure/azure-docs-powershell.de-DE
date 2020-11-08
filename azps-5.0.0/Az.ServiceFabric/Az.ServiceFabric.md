---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177228"
---
# AZ. ServiceFabric-Modul
## Beschreibung
Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.

## AZ. ServiceFabric-Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Hinzufügen eines sekundären Cluster Zertifikats zum Cluster

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Fügen Sie dem Cluster den allgemeinen Namen oder Fingerabdruck des Zertifikats hinzu. Dadurch wird das Zertifikat beim erneuten Registrieren des Clusters für Client Authentifizierungszwecke registriert.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Fügen Sie dem Knotentyp eine VM-Erweiterung hinzu.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Fügen Sie dem Knotentyp Zertifikatschlüssel hinzu.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Abrufen von Details zur Service Fabric-Anwendung.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Informationen zu den Details des Service Fabric-Anwendungstyps

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Abrufen von Details zur Version des Service Fabric-Anwendungstyps

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Rufen Sie die Clusterressourcen Details ab.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Rufen Sie die Details der verwalteten Clusterressourcen ab.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Abrufen der Ressourcendetails des verwalteten Knotentyps

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Informationen zum Service Fabric-Dienst finden Sie unter der angegebenen Anwendung und dem angegebenen Cluster.

### [Neu – AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem Cluster.

### [Neu – AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Erstellen eines neuen Service Fabric-Anwendungstyps unter der angegebenen Ressourcengruppe und dem angegebenen Cluster

### [Neu – AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Erstellen Sie unter der angegebenen Ressourcengruppe und dem Cluster eine neue Version des Anwendungstyps.

### [Neu – AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten. Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden. Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.

### [Neu – AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Erstellen eines neuen verwalteten Clusters

### [Neu – AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Erstellen Sie eine neue Knotentyp Ressource.

### [Neu – AzServiceFabricService](New-AzServiceFabricService.md)
Erstellen eines neuen Service Fabric-Diensts unter der angegebenen Anwendung und dem angegebenen Cluster

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Entfernen einer Anwendung aus dem Cluster Dadurch werden alle Dienste unter der Anwendung entfernt.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Entfernen Sie den Dienst Fabric, und geben Sie einen Anwendungstyp aus dem Cluster ein. Dadurch werden alle Typen Versionen unter dieser Ressource entfernt.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Entfernen Sie Service Fabric, eine Anwendungstypen Version aus dem Cluster.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Clusterressource entfernen.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe-Clientzertifikat nach Fingerabdruck oder allgemeinem Namen.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Entfernen des Knotentyps oder bestimmter Knoten innerhalb des Knotentyps

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Entfernen Sie die VM-Erweiterung vom Knotentyp.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Entfernen eines vollständigen Knotentyps aus einem Cluster

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Entfernen eines Diensts aus dem Cluster

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster

### [Neustart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Starten Sie bestimmte Knoten aus dem Knotentyp neu.

### [Satz-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Clusterressourcen Eigenschaften einrichten

### [Satz-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Legt Knotentyp-Ressourceneigenschaften fest oder führt reimage-Aktionen für bestimmte NDES des Knotentyps mit dem Parameter-reimage aus.

### [Satz-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster

### [Satz-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändern des Service Fabric-Upgrade-Typs des Clusters

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Aktualisieren einer Service Fabric-Anwendung Auf diese Weise können Sie die Anwendungsparameter aktualisieren und/oder die Version des Anwendungstyps aktualisieren, die ein Anwendungs Upgrade auslösen wird.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.

