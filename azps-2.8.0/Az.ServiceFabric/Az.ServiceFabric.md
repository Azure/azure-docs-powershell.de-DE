---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: d94e7001df730b22fb900b284c6fac47b5d81b8b
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93650306"
---
# <span data-ttu-id="ab59b-101">AZ. ServiceFabric-Modul</span><span class="sxs-lookup"><span data-stu-id="ab59b-101">Az.ServiceFabric Module</span></span>
## <span data-ttu-id="ab59b-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab59b-102">Description</span></span>
<span data-ttu-id="ab59b-103">Azure Service Fabric-Modul, das Sie verwenden können, um die End-2-End-Vorgänge wie das Erstellen eines sicheren Clusters, das Rollen über Cluster Zertifikate, das Hinzufügen oder Entfernen von Knoten aus dem Cluster usw. zu automatisieren. Nachfolgend finden Sie die vollständige Liste aller Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="ab59b-103">Azure Service Fabric Module that you can use to automate the end-2-end operations like creating a secure cluster, rolling over cluster certificates, adding or removed nodes from the cluster, etc. The complete list of all operations are listed below.</span></span>

## <span data-ttu-id="ab59b-104">AZ. ServiceFabric-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ab59b-104">Az.ServiceFabric Cmdlets</span></span>
### [<span data-ttu-id="ab59b-105">Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab59b-105">Add-AzServiceFabricApplicationCertificate</span></span>](Add-AzServiceFabricApplicationCertificate.md)
<span data-ttu-id="ab59b-106">Hinzufügen eines neuen Zertifikats zu den Skalierungs Sätzen des virtuellen Computers, aus denen sich der Cluster besteht</span><span class="sxs-lookup"><span data-stu-id="ab59b-106">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="ab59b-107">Das Zertifikat soll als Anwendungszertifikat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab59b-107">The certificate is intended to be used as an application certificate.</span></span>

### [<span data-ttu-id="ab59b-108">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab59b-108">Add-AzServiceFabricClientCertificate</span></span>](Add-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ab59b-109">Fügen Sie dem Cluster einen allgemeinen Namen oder Fingerabdruck hinzu, um Client Authentifizierungszwecke zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab59b-109">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

### [<span data-ttu-id="ab59b-110">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ab59b-110">Add-AzServiceFabricClusterCertificate</span></span>](Add-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ab59b-111">Hinzufügen eines sekundären Cluster Zertifikats zum Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-111">Add a secondary cluster certificate to the cluster.</span></span>

### [<span data-ttu-id="ab59b-112">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab59b-112">Add-AzServiceFabricNode</span></span>](Add-AzServiceFabricNode.md)
<span data-ttu-id="ab59b-113">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab59b-113">Add nodes to the specific node type in the cluster.</span></span>

### [<span data-ttu-id="ab59b-114">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ab59b-114">Add-AzServiceFabricNodeType</span></span>](Add-AzServiceFabricNodeType.md)
<span data-ttu-id="ab59b-115">Hinzufügen eines neuen Knotentyps zum vorhandenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-115">Add a new node type to the existing cluster.</span></span>

### [<span data-ttu-id="ab59b-116">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab59b-116">Get-AzServiceFabricApplication</span></span>](Get-AzServiceFabricApplication.md)
<span data-ttu-id="ab59b-117">Abrufen von Details zur Service Fabric-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ab59b-117">Get Service Fabric application details.</span></span>

### [<span data-ttu-id="ab59b-118">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab59b-118">Get-AzServiceFabricApplicationType</span></span>](Get-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab59b-119">Informationen zu den Details des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="ab59b-119">Get Service Fabric application type details.</span></span>

### [<span data-ttu-id="ab59b-120">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab59b-120">Get-AzServiceFabricApplicationTypeVersion</span></span>](Get-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab59b-121">Abrufen von Details zur Version des Service Fabric-Anwendungstyps</span><span class="sxs-lookup"><span data-stu-id="ab59b-121">Get Service Fabric application type version details.</span></span>

### [<span data-ttu-id="ab59b-122">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-122">Get-AzServiceFabricCluster</span></span>](Get-AzServiceFabricCluster.md)
<span data-ttu-id="ab59b-123">Rufen Sie die Clusterressourcen Details ab.</span><span class="sxs-lookup"><span data-stu-id="ab59b-123">Get the cluster resource details.</span></span>

### [<span data-ttu-id="ab59b-124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab59b-124">Get-AzServiceFabricService</span></span>](Get-AzServiceFabricService.md)
<span data-ttu-id="ab59b-125">Informationen zum Service Fabric-Dienst finden Sie unter der angegebenen Anwendung und dem angegebenen Cluster.</span><span class="sxs-lookup"><span data-stu-id="ab59b-125">Get Service Fabric service details under the specified application and cluster.</span></span>

### [<span data-ttu-id="ab59b-126">Neu – AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab59b-126">New-AzServiceFabricApplication</span></span>](New-AzServiceFabricApplication.md)
<span data-ttu-id="ab59b-127">Erstellen Sie eine neue Service Fabric-Anwendung unter der angegebenen Ressourcengruppe und dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="ab59b-127">Create new service fabric application under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab59b-128">Neu – AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab59b-128">New-AzServiceFabricApplicationType</span></span>](New-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab59b-129">Erstellen eines neuen Service Fabric-Anwendungstyps unter der angegebenen Ressourcengruppe und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-129">Create new service fabric application type under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab59b-130">Neu – AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab59b-130">New-AzServiceFabricApplicationTypeVersion</span></span>](New-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab59b-131">Erstellen Sie unter der angegebenen Ressourcengruppe und dem Cluster eine neue Version des Anwendungstyps.</span><span class="sxs-lookup"><span data-stu-id="ab59b-131">Create new application type version under the specified resource group and cluster.</span></span>

### [<span data-ttu-id="ab59b-132">Neu – AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-132">New-AzServiceFabricCluster</span></span>](New-AzServiceFabricCluster.md)
<span data-ttu-id="ab59b-133">Dieser Befehl verwendet von Ihnen bereitgestellte Zertifikate oder vom System generierte selbstsignierte Zertifikate, um einen neuen Service Fabric-Cluster einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ab59b-133">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="ab59b-134">Sie kann eine Standardvorlage oder eine von Ihnen bereitgestellte benutzerdefinierte Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab59b-134">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="ab59b-135">Sie haben die Möglichkeit, einen Ordner anzugeben, um die selbstsignierten Zertifikate zu exportieren oder später aus dem schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ab59b-135">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

### [<span data-ttu-id="ab59b-136">Neu – AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab59b-136">New-AzServiceFabricService</span></span>](New-AzServiceFabricService.md)
<span data-ttu-id="ab59b-137">Erstellen eines neuen Service Fabric-Diensts unter der angegebenen Anwendung und dem angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-137">Create new service fabric service under the specified application and cluster.</span></span>

### [<span data-ttu-id="ab59b-138">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab59b-138">Remove-AzServiceFabricApplication</span></span>](Remove-AzServiceFabricApplication.md)
<span data-ttu-id="ab59b-139">Entfernen einer Anwendung aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-139">Remove an application from the cluster.</span></span> <span data-ttu-id="ab59b-140">Dadurch werden alle Dienste unter der Anwendung entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab59b-140">This will remove all the services under the application.</span></span>

### [<span data-ttu-id="ab59b-141">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab59b-141">Remove-AzServiceFabricApplicationType</span></span>](Remove-AzServiceFabricApplicationType.md)
<span data-ttu-id="ab59b-142">Entfernen Sie den Dienst Fabric, und geben Sie einen Anwendungstyp aus dem Cluster ein.</span><span class="sxs-lookup"><span data-stu-id="ab59b-142">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ab59b-143">Dadurch werden alle Typen Versionen unter dieser Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="ab59b-143">This will remove all type versions under this resource.</span></span>

### [<span data-ttu-id="ab59b-144">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab59b-144">Remove-AzServiceFabricApplicationTypeVersion</span></span>](Remove-AzServiceFabricApplicationTypeVersion.md)
<span data-ttu-id="ab59b-145">Entfernen Sie Service Fabric, eine Anwendungstypen Version aus dem Cluster.</span><span class="sxs-lookup"><span data-stu-id="ab59b-145">Remove Service fabric an application type version from the cluster.</span></span>

### [<span data-ttu-id="ab59b-146">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ab59b-146">Remove-AzServiceFabricClientCertificate</span></span>](Remove-AzServiceFabricClientCertificate.md)
<span data-ttu-id="ab59b-147">Entfernen Sie ein Clientzertifikat (e) oder den Namen des Zertifikats betreffs, der für die Clientauthentifizierung für den Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab59b-147">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

### [<span data-ttu-id="ab59b-148">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="ab59b-148">Remove-AzServiceFabricClusterCertificate</span></span>](Remove-AzServiceFabricClusterCertificate.md)
<span data-ttu-id="ab59b-149">Entfernen Sie ein Cluster Zertifikat, das für die Cluster Sicherheit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab59b-149">Remove a cluster certificate from being used for cluster security.</span></span>

### [<span data-ttu-id="ab59b-150">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab59b-150">Remove-AzServiceFabricNode</span></span>](Remove-AzServiceFabricNode.md)
<span data-ttu-id="ab59b-151">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-151">Remove nodes from the specific node type from a cluster.</span></span>

### [<span data-ttu-id="ab59b-152">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="ab59b-152">Remove-AzServiceFabricNodeType</span></span>](Remove-AzServiceFabricNodeType.md)
<span data-ttu-id="ab59b-153">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-153">Remove a complete node type from a cluster.</span></span>

### [<span data-ttu-id="ab59b-154">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab59b-154">Remove-AzServiceFabricService</span></span>](Remove-AzServiceFabricService.md)
<span data-ttu-id="ab59b-155">Entfernen eines Diensts aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-155">Remove a service from the cluster.</span></span>

### [<span data-ttu-id="ab59b-156">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ab59b-156">Remove-AzServiceFabricSetting</span></span>](Remove-AzServiceFabricSetting.md)
<span data-ttu-id="ab59b-157">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-157">Remove one or multiple Service Fabric setting from the cluster.</span></span>

### [<span data-ttu-id="ab59b-158">Satz-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ab59b-158">Set-AzServiceFabricSetting</span></span>](Set-AzServiceFabricSetting.md)
<span data-ttu-id="ab59b-159">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="ab59b-159">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

### [<span data-ttu-id="ab59b-160">Satz-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="ab59b-160">Set-AzServiceFabricUpgradeType</span></span>](Set-AzServiceFabricUpgradeType.md)
<span data-ttu-id="ab59b-161">Ändern des Service Fabric-Upgrade-Typs des Clusters</span><span class="sxs-lookup"><span data-stu-id="ab59b-161">Change the Service Fabric upgrade type of the cluster.</span></span>

### [<span data-ttu-id="ab59b-162">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab59b-162">Update-AzServiceFabricApplication</span></span>](Update-AzServiceFabricApplication.md)
<span data-ttu-id="ab59b-163">Aktualisieren einer Service Fabric-Anwendung</span><span class="sxs-lookup"><span data-stu-id="ab59b-163">Update a service fabric application.</span></span> <span data-ttu-id="ab59b-164">Auf diese Weise können Sie die Anwendungsparameter aktualisieren und/oder die Version des Anwendungstyps aktualisieren, die ein Anwendungs Upgrade auslösen wird.</span><span class="sxs-lookup"><span data-stu-id="ab59b-164">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

### [<span data-ttu-id="ab59b-165">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ab59b-165">Update-AzServiceFabricDurability</span></span>](Update-AzServiceFabricDurability.md)
<span data-ttu-id="ab59b-166">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="ab59b-166">Update the durability tier or VmSku of a node type in the cluster.</span></span>

### [<span data-ttu-id="ab59b-167">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ab59b-167">Update-AzServiceFabricReliability</span></span>](Update-AzServiceFabricReliability.md)
<span data-ttu-id="ab59b-168">Aktualisieren Sie die Zuverlässigkeitsstufe des primären Knotentyps in einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="ab59b-168">Update the reliability tier of the primary node type in a cluster.</span></span>

