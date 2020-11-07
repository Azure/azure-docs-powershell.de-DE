---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93650115"
---
# <span data-ttu-id="12f56-101">AZ. ServiceFabric-Modul</span><span class="sxs-lookup"><span data-stu-id="12f56-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="12f56-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12f56-102">Description</span></span>
<span data-ttu-id="12f56-103">Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="12f56-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="12f56-104">AZ. ServiceFabric-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="12f56-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="12f56-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="12f56-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="12f56-106">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="12f56-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="12f56-107">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12f56-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="12f56-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12f56-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="12f56-109">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12f56-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="12f56-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="12f56-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="12f56-111">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="12f56-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="12f56-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="12f56-113">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="12f56-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="12f56-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="12f56-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="12f56-115">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="12f56-116">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="12f56-116">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="12f56-117">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="12f56-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="12f56-118">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="12f56-118">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="12f56-119">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="12f56-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="12f56-120">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="12f56-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="12f56-121">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12f56-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="12f56-122">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12f56-122">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="12f56-123">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12f56-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="12f56-124">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="12f56-124">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="12f56-125">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="12f56-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="12f56-126">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="12f56-126">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="12f56-127">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="12f56-128">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="12f56-128">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="12f56-129">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="12f56-130">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="12f56-130">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="12f56-131">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="12f56-132">Satz-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="12f56-132">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="12f56-133">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="12f56-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="12f56-134">Satz-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="12f56-134">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="12f56-135">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="12f56-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="12f56-136">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="12f56-136">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="12f56-137">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="12f56-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="12f56-138">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="12f56-138">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="12f56-139">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="12f56-139">Update the reliability tier of the primary node type in a cluster.</span></span>

