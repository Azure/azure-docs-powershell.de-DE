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
# <span data-ttu-id="cc5d4-101">AzureRM. ServiceFabric-Modul</span><span class="sxs-lookup"><span data-stu-id="cc5d4-101">AzureRM.ServiceFabric Module</span></span>
## <span data-ttu-id="cc5d4-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc5d4-102">Description</span></span>
<span data-ttu-id="cc5d4-103">Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="cc5d4-104">AzureRM. ServiceFabric-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cc5d4-104">AzureRM.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="cc5d4-105">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="cc5d4-105">Add-AzureRmServiceFabricApplicationCertificate</span></span>](Add-AzureRmServiceFabricApplicationCertificate.md)
<span data-ttu-id="cc5d4-106">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="cc5d4-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="cc5d4-107">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="cc5d4-108">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc5d4-108">Add-AzureRmServiceFabricClientCertificate</span></span>](Add-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="cc5d4-109">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="cc5d4-110">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cc5d4-110">Add-AzureRmServiceFabricClusterCertificate</span></span>](Add-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="cc5d4-111">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="cc5d4-112">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cc5d4-112">Add-AzureRmServiceFabricNode</span></span>](Add-AzureRmServiceFabricNode.md)
<span data-ttu-id="cc5d4-113">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="cc5d4-114">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="cc5d4-114">Add-AzureRmServiceFabricNodeType</span></span>](Add-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="cc5d4-115">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="cc5d4-116">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-116">Get-AzureRmServiceFabricCluster</span></span>](Get-AzureRmServiceFabricCluster.md)
<span data-ttu-id="cc5d4-117">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-117">Get the cluster resource details.</span></span>

### [<span data-ttu-id="cc5d4-118">Neu – AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-118">New-AzureRmServiceFabricCluster</span></span>](New-AzureRmServiceFabricCluster.md)
<span data-ttu-id="cc5d4-119">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-119">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="cc5d4-120">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-120">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="cc5d4-121">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-121">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="cc5d4-122">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cc5d4-122">Remove-AzureRmServiceFabricClientCertificate</span></span>](Remove-AzureRmServiceFabricClientCertificate.md)
<span data-ttu-id="cc5d4-123">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-123">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="cc5d4-124">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cc5d4-124">Remove-AzureRmServiceFabricClusterCertificate</span></span>](Remove-AzureRmServiceFabricClusterCertificate.md)
<span data-ttu-id="cc5d4-125">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-125">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="cc5d4-126">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cc5d4-126">Remove-AzureRmServiceFabricNode</span></span>](Remove-AzureRmServiceFabricNode.md)
<span data-ttu-id="cc5d4-127">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-127">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="cc5d4-128">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="cc5d4-128">Remove-AzureRmServiceFabricNodeType</span></span>](Remove-AzureRmServiceFabricNodeType.md)
<span data-ttu-id="cc5d4-129">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-129">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="cc5d4-130">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="cc5d4-130">Remove-AzureRmServiceFabricSetting</span></span>](Remove-AzureRmServiceFabricSetting.md)
<span data-ttu-id="cc5d4-131">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-131">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="cc5d4-132">Satz-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="cc5d4-132">Set-AzureRmServiceFabricSetting</span></span>](Set-AzureRmServiceFabricSetting.md)
<span data-ttu-id="cc5d4-133">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="cc5d4-133">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="cc5d4-134">Satz-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="cc5d4-134">Set-AzureRmServiceFabricUpgradeType</span></span>](Set-AzureRmServiceFabricUpgradeType.md)
<span data-ttu-id="cc5d4-135">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="cc5d4-135">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="cc5d4-136">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="cc5d4-136">Update-AzureRmServiceFabricDurability</span></span>](Update-AzureRmServiceFabricDurability.md)
<span data-ttu-id="cc5d4-137">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-137">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="cc5d4-138">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="cc5d4-138">Update-AzureRmServiceFabricReliability</span></span>](Update-AzureRmServiceFabricReliability.md)
<span data-ttu-id="cc5d4-139">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="cc5d4-139">Update the reliability tier of the primary node type in a cluster.</span></span>

