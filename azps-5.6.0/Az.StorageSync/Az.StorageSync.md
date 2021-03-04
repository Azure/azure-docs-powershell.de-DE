---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929203"
---
# <span data-ttu-id="9bcb2-101">Az.StorageSync-Modul</span><span class="sxs-lookup"><span data-stu-id="9bcb2-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="9bcb2-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bcb2-102">Description</span></span>
<span data-ttu-id="9bcb2-103">Die Cmdlets im Speichersynchronisierungsmodul ermöglichen ihnen das Verwalten von Vorgängen im Zusammenhang mit Azure File Sync in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="9bcb2-104">Az.StorageSync-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9bcb2-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="9bcb2-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9bcb2-106">Mit diesem Befehl werden alle Cloudendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="9bcb2-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9bcb2-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="9bcb2-108">Mit diesem Befehl werden alle Synchronisierungsgruppen innerhalb eines bestimmten Speichersynchronisierungsdiensts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="9bcb2-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9bcb2-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="9bcb2-110">Mit diesem Befehl werden alle Server aufgeführt, die bei einem bestimmten Speichersynchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="9bcb2-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9bcb2-112">Mit diesem Befehl werden alle Serverendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="9bcb2-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9bcb2-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="9bcb2-114">Mit diesem Befehl werden alle Speichersynchronisierungsdienste in einem bestimmten Bereich der Abonnement-/Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="9bcb2-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="9bcb2-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="9bcb2-116">Dieser Befehl kann verwendet werden, um die Erkennung von Namespaceänderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="9bcb2-117">Sie kann auf die gesamte Freigabe, den Unterordner oder die gesamte Gruppe von Dateien ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="9bcb2-118">Es können maximal 10.000 Änderungen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="9bcb2-119">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb eines Grenzwerts von 10.000 Änderungen abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="9bcb2-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="9bcb2-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="9bcb2-121">Sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="9bcb2-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="9bcb2-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="9bcb2-123">Dieser Befehl ruft alle mehrstufigen Dateien wieder auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="9bcb2-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9bcb2-125">Mit diesem Befehl wird ein Azure File Sync-Cloudendpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="9bcb2-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9bcb2-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="9bcb2-127">Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="9bcb2-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9bcb2-129">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="9bcb2-130">Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="9bcb2-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9bcb2-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="9bcb2-132">Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="9bcb2-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9bcb2-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="9bcb2-134">Mit diesem Befehl wird ein Speichersynchronisierungsdienst in einer Ressourcengruppe definiert.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="9bcb2-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9bcb2-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="9bcb2-136">Mit diesem Befehl wird ein Server bei einem Speichersynchronisierungsdienst registriert, der eine Vertrauensstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="9bcb2-137">PowerShell oder das Azure-Portal können dann zum Konfigurieren der Synchronisierung auf diesem Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="9bcb2-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="9bcb2-139">Mit diesem Befehl wird der angegebene Cloudendpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9bcb2-140">Ohne mindestens einen Cloudendpunkt können keine anderen Serverendpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="9bcb2-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9bcb2-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="9bcb2-142">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="9bcb2-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9bcb2-144">Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="9bcb2-145">Die Synchronisierung mit diesem Speicherort wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="9bcb2-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9bcb2-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="9bcb2-147">Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="9bcb2-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="9bcb2-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="9bcb2-149">Wird nur zur Problembehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-149">Use for troubleshooting only.</span></span> <span data-ttu-id="9bcb2-150">Mit diesem Befehl wird das Speichersynchronisierungsserverzertifikat rollt, das zum Beschreiben der Serveridentität für den Speichersynchronisierungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="9bcb2-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9bcb2-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="9bcb2-152">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="9bcb2-153">Aufheben der Registrierung-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9bcb2-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="9bcb2-154">Warnung: Das Aufheben der Registrierung eines Servers führt dazu, dass alle Serverendpunkte auf diesem Server kaskadiert werden.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="9bcb2-155">Mit diesem Befehl wird die Registrierung eines Servers vom Speichersynchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="9bcb2-155">This command will unregister a server from it's storage sync service.</span></span>

