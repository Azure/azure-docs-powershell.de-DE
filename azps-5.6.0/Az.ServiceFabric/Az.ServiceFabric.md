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
# <span data-ttu-id="5f7dc-101">Az.ServiceFabric-Modul</span><span class="sxs-lookup"><span data-stu-id="5f7dc-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="5f7dc-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f7dc-102">Description</span></span>
<span data-ttu-id="5f7dc-103">Azure Service Fabric-Modul, mit dem Sie die End-2-End-Vorgänge automatisieren können, z. B. das Erstellen eines sicheren Clusters, das Roll over-Clusterzertifikat, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. Die vollständige Liste aller Vorgänge ist unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="5f7dc-104">Az.ServiceFabric Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5f7dc-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="5f7dc-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="5f7dc-106">Fügen Sie dem Cluster zu Clientauthentifizierungszwecken allgemeinen Namen oder Fingerabdruck hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="5f7dc-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="5f7dc-108">Fügen Sie dem Cluster ein sekundäres Clusterzertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="5f7dc-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="5f7dc-110">Fügen Sie dem Cluster gemeinsamen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="5f7dc-111">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="5f7dc-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="5f7dc-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="5f7dc-113">Fügen Sie dem Knotentyp die Erweiterung vm hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="5f7dc-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="5f7dc-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="5f7dc-115">Fügen Sie dem Knotentyp den Zertifikatsgeheimnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="5f7dc-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5f7dc-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="5f7dc-117">Fügen Sie dem bestimmten Knotentyp im Cluster Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="5f7dc-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="5f7dc-119">Fügen Sie dem vorhandenen Cluster einen neuen Knotentyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="5f7dc-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5f7dc-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="5f7dc-121">Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="5f7dc-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="5f7dc-123">Details zum Service Fabric-Anwendungstyp.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="5f7dc-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5f7dc-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="5f7dc-125">Details zur Version des Service Fabric-Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="5f7dc-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="5f7dc-127">Hier erhalten Sie die Details zu den Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="5f7dc-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="5f7dc-129">Hier erhalten Sie die Ressourcendetails für verwaltete Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="5f7dc-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="5f7dc-131">Holen Sie sich die Ressourcendetails für den verwalteten Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="5f7dc-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5f7dc-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="5f7dc-133">Holen Sie sich Service Fabric-Dienstdetails unter der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="5f7dc-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5f7dc-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="5f7dc-135">Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="5f7dc-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="5f7dc-137">Erstellen Sie einen neuen Service Fabric-Anwendungstyp unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="5f7dc-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5f7dc-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="5f7dc-139">Erstellen Sie eine neue Anwendungstypversion unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="5f7dc-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="5f7dc-141">Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder systemgenerierte selbst signierte Zertifikate, um einen neuen Service Fabric-Cluster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="5f7dc-142">Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="5f7dc-143">Sie haben die Möglichkeit, einen Ordner anzugeben, in den die selbst signierten Zertifikate exportiert oder später aus dem Schlüsseltresor abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="5f7dc-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="5f7dc-145">Erstellen Sie einen neuen verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="5f7dc-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="5f7dc-147">Erstellen Sie eine neue Knotentypressource.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-147">Create new node type resource.</span></span>

### [<span data-ttu-id="5f7dc-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5f7dc-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="5f7dc-149">Erstellen Sie einen neuen Service Fabric-Dienst unter der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="5f7dc-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5f7dc-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="5f7dc-151">Entfernen Sie eine Anwendung aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-151">Remove an application from the cluster.</span></span> <span data-ttu-id="5f7dc-152">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="5f7dc-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="5f7dc-154">Entfernen Sie service fabric einen Anwendungstyp aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="5f7dc-155">Dadurch werden alle Typversionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="5f7dc-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5f7dc-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="5f7dc-157">Entfernen sie eine Anwendungstypversion aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="5f7dc-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="5f7dc-159">Entfernen Sie die Namen von Clientzertifikaten oder Zertifikatsubjekten aus der Verwendung für die Clientauthentifizierung im Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="5f7dc-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="5f7dc-161">Entfernen Sie ein Clusterzertifikat aus der Verwendung für die Clustersicherheit.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="5f7dc-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="5f7dc-163">Entfernen Sie die Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="5f7dc-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5f7dc-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="5f7dc-165">Remvoe client certificate by thumbprint or common name.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="5f7dc-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="5f7dc-167">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="5f7dc-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="5f7dc-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="5f7dc-169">Entfernen Sie die Vm-Erweiterung aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="5f7dc-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5f7dc-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="5f7dc-171">Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="5f7dc-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="5f7dc-173">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="5f7dc-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5f7dc-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="5f7dc-175">Entfernen eines Diensts aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="5f7dc-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5f7dc-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="5f7dc-177">Entfernen Sie eine oder mehrere Service Fabric-Einstellungen aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="5f7dc-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="5f7dc-179">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="5f7dc-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="5f7dc-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="5f7dc-181">Festlegen von Clusterressourceneigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f7dc-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="5f7dc-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="5f7dc-183">Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Ndes des Knotentyps mit dem Parameter -Reimage aus.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="5f7dc-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="5f7dc-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="5f7dc-185">Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="5f7dc-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="5f7dc-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="5f7dc-187">Ändern Sie den Service Fabric-Upgradetyp des Clusters.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="5f7dc-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5f7dc-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="5f7dc-189">Aktualisieren einer Service Fabric-Anwendung</span><span class="sxs-lookup"><span data-stu-id="5f7dc-189">Update a service fabric application.</span></span> <span data-ttu-id="5f7dc-190">Dadurch können die Anwendungsparameter aktualisiert und/oder die Anwendungstypversion aktualisiert werden, wodurch ein Anwendungsupgrade ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="5f7dc-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="5f7dc-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="5f7dc-192">Aktualisieren Sie die Lebensdauerebene oder vmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="5f7dc-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="5f7dc-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="5f7dc-194">Aktualisieren Sie die Zuverlässigkeitsebene des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="5f7dc-194">Update the reliability tier of the primary node type in a cluster.</span></span>

