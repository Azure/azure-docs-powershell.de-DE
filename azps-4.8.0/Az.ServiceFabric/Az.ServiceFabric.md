---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010490"
---
# <span data-ttu-id="41804-101">AZ. ServiceFabric-Modul</span><span class="sxs-lookup"><span data-stu-id="41804-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="41804-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41804-102">Description</span></span>
<span data-ttu-id="41804-103">Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="41804-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="41804-104">AZ. ServiceFabric-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="41804-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="41804-105">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-105">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="41804-106">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="41804-106">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="41804-107">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-107">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="41804-108">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-108">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="41804-109">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-109">Add-AzServiceFabricManagedClusterClientCertificate</span></span>](Add-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="41804-110">Fügen Sie dem Cluster den allgemeinen Namen oder Fingerabdruck des Zertifikats hinzu.</span><span class="sxs-lookup"><span data-stu-id="41804-110">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="41804-111">Dadurch wird das Zertifikat beim erneuten Registrieren des Clusters für Client Authentifizierungszwecke registriert.</span><span class="sxs-lookup"><span data-stu-id="41804-111">This will register the certificate agains the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="41804-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="41804-112">Add-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="41804-113">Fügen Sie dem Knotentyp eine VM-Erweiterung hinzu.</span><span class="sxs-lookup"><span data-stu-id="41804-113">Add vm extension to the node type.</span></span>

### [<span data-ttu-id="41804-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="41804-114">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
<span data-ttu-id="41804-115">Fügen Sie dem Knotentyp Zertifikatschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="41804-115">Add certificate secret to the node type.</span></span>

### [<span data-ttu-id="41804-116">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="41804-116">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="41804-117">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="41804-117">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="41804-118">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-118">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="41804-119">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-119">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="41804-120">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41804-120">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="41804-121">Abrufen von Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="41804-121">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="41804-122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41804-122">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="41804-123">Informationen zu den Details des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="41804-123">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="41804-124">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41804-124">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="41804-125">Abrufen von Details zur Version des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="41804-125">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="41804-126">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="41804-126">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="41804-127">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="41804-127">Get the cluster resource details.</span></span>

### [<span data-ttu-id="41804-128">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="41804-128">Get-AzServiceFabricManagedCluster</span></span>](Get-AzServiceFabricManagedCluster.md)
<span data-ttu-id="41804-129">Rufen Sie die Details der verwalteten Clusterressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="41804-129">Get the managed cluster resource details.</span></span>

### [<span data-ttu-id="41804-130">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-130">Get-AzServiceFabricManagedNodeType</span></span>](Get-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="41804-131">Abrufen der Ressourcendetails des verwalteten Knotentyps</span><span class="sxs-lookup"><span data-stu-id="41804-131">Get the managed node type resource details.</span></span>

### [<span data-ttu-id="41804-132">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="41804-132">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="41804-133">Informationen zum Service Fabric-Dienst finden Sie unter der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="41804-133">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="41804-134">Neu – AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41804-134">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="41804-135">Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="41804-135">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="41804-136">Neu – AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41804-136">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="41804-137">Erstellen eines neuen Service Fabric-Anwendungstyps unter der angegebenen Ressourcengruppe und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-137">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="41804-138">Neu – AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41804-138">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="41804-139">Erstellen Sie unter der angegebenen Ressourcengruppe und dem Cluster eine neue Version des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="41804-139">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="41804-140">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="41804-140">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="41804-141">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="41804-141">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="41804-142">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="41804-142">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="41804-143">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41804-143">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

### [<span data-ttu-id="41804-144">Neu – AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="41804-144">New-AzServiceFabricManagedCluster</span></span>](New-AzServiceFabricManagedCluster.md)
<span data-ttu-id="41804-145">Erstellen eines neuen verwalteten Clusters</span><span class="sxs-lookup"><span data-stu-id="41804-145">Create new managed cluster.</span></span>

### [<span data-ttu-id="41804-146">Neu – AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-146">New-AzServiceFabricManagedNodeType</span></span>](New-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="41804-147">Erstellen Sie eine neue Knotentyp Ressource.</span><span class="sxs-lookup"><span data-stu-id="41804-147">Create new node type resource.</span></span>

### [<span data-ttu-id="41804-148">Neu – AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="41804-148">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="41804-149">Erstellen eines neuen Service Fabric-Diensts unter der angegebenen Anwendung und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-149">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="41804-150">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41804-150">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="41804-151">Entfernen einer Anwendung aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-151">Remove an application from the cluster.</span></span> <span data-ttu-id="41804-152">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="41804-152">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="41804-153">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41804-153">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="41804-154">Entfernen Sie den Dienst Fabric, und geben Sie einen Anwendungstyp aus dem Cluster ein.</span><span class="sxs-lookup"><span data-stu-id="41804-154">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="41804-155">Dadurch werden alle Typen Versionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="41804-155">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="41804-156">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41804-156">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="41804-157">Entfernen Sie Service Fabric, eine Anwendungstypen Version aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="41804-157">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="41804-158">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-158">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="41804-159">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41804-159">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="41804-160">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-160">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="41804-161">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41804-161">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="41804-162">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="41804-162">Remove-AzServiceFabricManagedCluster</span></span>](Remove-AzServiceFabricManagedCluster.md)
<span data-ttu-id="41804-163">Clusterressource entfernen.</span><span class="sxs-lookup"><span data-stu-id="41804-163">Remove cluster resource.</span></span>

### [<span data-ttu-id="41804-164">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41804-164">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>](Remove-AzServiceFabricManagedClusterClientCertificate.md)
<span data-ttu-id="41804-165">Remvoe-Clientzertifikat nach Fingerabdruck oder allgemeinem Namen.</span><span class="sxs-lookup"><span data-stu-id="41804-165">Remvoe client certificate by thumbprint or common name.</span></span>

### [<span data-ttu-id="41804-166">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-166">Remove-AzServiceFabricManagedNodeType</span></span>](Remove-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="41804-167">Entfernen des Knotentyps oder bestimmter Knoten innerhalb des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="41804-167">Remove the node type or specific nodes within the node type.</span></span>

### [<span data-ttu-id="41804-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="41804-168">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
<span data-ttu-id="41804-169">Entfernen Sie die VM-Erweiterung vom Knotentyp.</span><span class="sxs-lookup"><span data-stu-id="41804-169">Remove vm extension from the node type.</span></span>

### [<span data-ttu-id="41804-170">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="41804-170">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="41804-171">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-171">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="41804-172">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-172">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="41804-173">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-173">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="41804-174">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="41804-174">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="41804-175">Entfernen eines Diensts aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-175">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="41804-176">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="41804-176">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="41804-177">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-177">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="41804-178">Neustart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-178">Restart-AzServiceFabricManagedNodeType</span></span>](Restart-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="41804-179">Starten Sie bestimmte Knoten aus dem Knotentyp neu.</span><span class="sxs-lookup"><span data-stu-id="41804-179">Restart specific nodes from the node type.</span></span>

### [<span data-ttu-id="41804-180">Satz-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="41804-180">Set-AzServiceFabricManagedCluster</span></span>](Set-AzServiceFabricManagedCluster.md)
<span data-ttu-id="41804-181">Clusterressourcen Eigenschaften einrichten</span><span class="sxs-lookup"><span data-stu-id="41804-181">Set cluster resource properties.</span></span>

### [<span data-ttu-id="41804-182">Satz-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="41804-182">Set-AzServiceFabricManagedNodeType</span></span>](Set-AzServiceFabricManagedNodeType.md)
<span data-ttu-id="41804-183">Legt Knotentyp-Ressourceneigenschaften fest oder führt reimage-Aktionen für bestimmte NDES des Knotentyps mit dem Parameter-reimage aus.</span><span class="sxs-lookup"><span data-stu-id="41804-183">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

### [<span data-ttu-id="41804-184">Satz-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="41804-184">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="41804-185">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="41804-185">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="41804-186">Satz-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="41804-186">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="41804-187">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="41804-187">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="41804-188">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41804-188">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="41804-189">Aktualisieren einer Service Fabric-Anwendung</span><span class="sxs-lookup"><span data-stu-id="41804-189">Update a service fabric application.</span></span> <span data-ttu-id="41804-190">Auf diese Weise können Sie die Anwendungsparameter aktualisieren und/oder die Version des Anwendungstyps aktualisieren, die ein Anwendungs Upgrade auslösen wird.</span><span class="sxs-lookup"><span data-stu-id="41804-190">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="41804-191">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="41804-191">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="41804-192">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="41804-192">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="41804-193">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="41804-193">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="41804-194">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="41804-194">Update the reliability tier of the primary node type in a cluster.</span></span>

