---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93473941"
---
# AzureRM. ServiceFabric-Modul
## Beschreibung
Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.

## AzureRM. ServiceFabric-Cmdlets
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht Das Zertifikat soll als Anwendungszertifikat verwendet werden.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Hinzufügen eines sekundären Cluster Zertifikats zum Cluster

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Rufen Sie die Clusterressourcen Details ab.

### [Neu – AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten. Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden. Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Entfernen eines vollständigen Knotentyps aus einem Cluster

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster

### [Satz-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster

### [Satz-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Ändern des Service Fabric-Upgrade-Typs des Clusters

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.

