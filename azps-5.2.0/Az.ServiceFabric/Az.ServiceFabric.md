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
# <span data-ttu-id="c9ebb-101">Az.ServiceFabric Module</span><span class="sxs-lookup"><span data-stu-id="c9ebb-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="c9ebb-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9ebb-102">Description</span></span>
<span data-ttu-id="c9ebb-103">Azure Service Fabric Module, das Sie zum Automatisieren der End-2-End-Vorgänge verwenden können, z. B. erstellen eines sicheren Cluster, Rolling über Clusterzertifikate, Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. Die vollständige Liste aller Vorgänge ist unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="c9ebb-104">Az.ServiceFabric Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c9ebb-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="c9ebb-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="c9ebb-106">Fügen Sie dem Cluster zu Clientauthentifizierungszwecken allgemeinen Namen oder Fingerabdrück hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="c9ebb-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="c9ebb-108">Fügen Sie dem Cluster ein Zertifikat für einen sekundären Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="c9ebb-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="c9ebb-110">Fügen Sie dem Cluster einen allgemeinen Zertifikatnamen oder Einen Fingerabdruck hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="c9ebb-111">Dadurch wird das Zertifikat erneut für den Cluster für Clientauthentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="c9ebb-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="c9ebb-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="c9ebb-113">Fügen Sie dem Knotentyp die Erweiterung "vm" hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="c9ebb-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="c9ebb-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="c9ebb-115">Fügen Sie dem Knotentyp einen geheimen Zertifikattyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="c9ebb-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c9ebb-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="c9ebb-117">Fügen Sie dem jeweiligen Knotentyp im Cluster Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="c9ebb-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="c9ebb-119">Fügen Sie dem vorhandenen Cluster einen neuen Knotentyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="c9ebb-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9ebb-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="c9ebb-121">Erhalten Sie Service Fabric-Anwendungsdetails.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="c9ebb-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="c9ebb-123">Get Service Fabric application type details.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="c9ebb-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c9ebb-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="c9ebb-125">Get Service Fabric application type version details.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="c9ebb-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="c9ebb-127">Erhalten Sie die Details der Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="c9ebb-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="c9ebb-129">Erhalten Sie die Details der verwalteten Clusterressourcen.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="c9ebb-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="c9ebb-131">Ressourcendetails für verwaltete Knotentypen</span><span class="sxs-lookup"><span data-stu-id="c9ebb-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="c9ebb-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c9ebb-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="c9ebb-133">Service Fabric service details under the specified application and cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="c9ebb-134">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9ebb-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="c9ebb-135">Create new service fabric application under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="c9ebb-136">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="c9ebb-137">Create new service fabric application type under the specified resource group and cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="c9ebb-138">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c9ebb-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="c9ebb-139">Erstellen Sie eine neue Anwendungstypversion unter der angegebenen Ressourcengruppe und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="c9ebb-140">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="c9ebb-141">Dieser Befehl verwendet Zertifikate, die Sie bereitstellen, oder vom System generierte selbst signierte Zertifikate zum Einrichten eines neuen Service Fabric Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="c9ebb-142">Sie kann eine Standardvorlage oder eine benutzerdefinierte Vorlage verwenden, die Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="c9ebb-143">Sie können einen Ordner angeben, in den die selbst signierten Zertifikate exportiert werden sollen, oder sie später aus dem Schlüsseltresor abrufen.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="c9ebb-144">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="c9ebb-145">Erstellen Sie einen neuen verwalteten Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="c9ebb-146">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="c9ebb-147">Erstellen sie eine neue Knotentypressource.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-147">Create new node type resource.</span></span>

### [<span data-ttu-id="c9ebb-148">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c9ebb-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="c9ebb-149">Create new service fabric service under the specified application and cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="c9ebb-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9ebb-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="c9ebb-151">Entfernen Sie eine Anwendung aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-151">Remove an application from the cluster.</span></span> <span data-ttu-id="c9ebb-152">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="c9ebb-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="c9ebb-154">Remove Service fabric an application type from the cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="c9ebb-155">Dadurch werden alle Typversionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="c9ebb-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c9ebb-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="c9ebb-157">Remove Service fabric an application type version from the cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="c9ebb-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="c9ebb-159">Entfernen Sie die Namen von Clientzertifikaten oder Zertifikatsubjekten aus der Verwendung für die Clientauthentifizierung im Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="c9ebb-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="c9ebb-161">Entfernen Sie ein Clusterzertifikat aus der Verwendung für cluster-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="c9ebb-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="c9ebb-163">Entfernen Sie die Clusterressource.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="c9ebb-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c9ebb-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="c9ebb-165">Geben Sie das Clientzertifikat per Fingerabdruck oder allgemeinem Namen ab.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="c9ebb-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="c9ebb-167">Entfernen Sie den Knotentyp oder bestimmte Knoten innerhalb des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="c9ebb-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="c9ebb-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="c9ebb-169">Entfernen Sie die erweiterung "vm" aus dem Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="c9ebb-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c9ebb-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="c9ebb-171">Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="c9ebb-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="c9ebb-173">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="c9ebb-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c9ebb-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="c9ebb-175">Entfernen sie einen Dienst aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="c9ebb-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c9ebb-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="c9ebb-177">Remove one or multiple Service Fabric setting from the cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="c9ebb-178">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="c9ebb-179">Starten Sie bestimmte Knoten vom Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="c9ebb-180">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="c9ebb-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="c9ebb-181">Legen Sie Clusterressourceneigenschaften festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="c9ebb-182">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="c9ebb-183">Legt Ressourceneigenschaften des Knotentyps fest, oder führen Sie Reimageaktionen für bestimmte Typen des Knotentyps mit dem Parameter "-Reimage" aus.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="c9ebb-184">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c9ebb-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="c9ebb-185">Fügen Sie dem Cluster eine oder mehrere Service Fabric-Einstellungen hinzu, oder aktualisieren Sie sie.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="c9ebb-186">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="c9ebb-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="c9ebb-187">Ändern Sie den Service Fabric-Upgradetyp des Clusters.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="c9ebb-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9ebb-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="c9ebb-189">Aktualisieren Sie eine Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-189">Update a service fabric application.</span></span> <span data-ttu-id="c9ebb-190">Dadurch können die Anwendungsparameter aktualisiert und/oder die Anwendungstypversion aktualisiert werden, wodurch ein Anwendungsupgrade ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="c9ebb-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c9ebb-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="c9ebb-192">Aktualisieren Sie das kontingente Tier oder vmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="c9ebb-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="c9ebb-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="c9ebb-194">Aktualisieren Sie die Zuverlässigkeitsstufen des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="c9ebb-194">Update the reliability tier of the primary node type in a cluster.</span></span>

