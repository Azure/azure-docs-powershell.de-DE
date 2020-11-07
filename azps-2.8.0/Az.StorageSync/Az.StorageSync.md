---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2019
ms.locfileid: "93650260"
---
# <span data-ttu-id="8355e-101">AZ. StorageSync-Modul</span><span class="sxs-lookup"><span data-stu-id="8355e-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="8355e-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8355e-102">Description</span></span>
<span data-ttu-id="8355e-103">Mit den Cmdlets im Speicher Synchronisierungsmodul können Sie Vorgänge in Bezug auf die Azure-Dateisynchronisierung in PowerShell verwalten.</span><span class="sxs-lookup"><span data-stu-id="8355e-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="8355e-104">AZ. StorageSync-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8355e-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="8355e-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="8355e-106">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="8355e-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="8355e-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8355e-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="8355e-108">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="8355e-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="8355e-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="8355e-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="8355e-110">Dieser Befehl listet alle Server auf, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="8355e-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="8355e-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="8355e-112">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="8355e-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="8355e-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8355e-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="8355e-114">Dieser Befehl listet alle Speicher Synchronisierungsdienste in einem bestimmten Bereich des Abonnements/der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="8355e-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="8355e-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="8355e-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="8355e-116">Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="8355e-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="8355e-117">Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="8355e-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="8355e-118">Es können maximal 10.000 Änderungen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="8355e-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="8355e-119">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb einer 10.000-Änderungs Grenze abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8355e-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="8355e-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="8355e-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="8355e-121">Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="8355e-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="8355e-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="8355e-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="8355e-123">Dieser Befehl ruft alle Tiered-Dateien wieder auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="8355e-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="8355e-124">Neu – AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="8355e-125">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="8355e-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="8355e-126">Neu – AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8355e-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="8355e-127">Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="8355e-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="8355e-128">Neu – AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="8355e-129">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="8355e-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="8355e-130">Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.</span><span class="sxs-lookup"><span data-stu-id="8355e-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="8355e-131">Neu – AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8355e-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="8355e-132">Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="8355e-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="8355e-133">Registrieren-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="8355e-133">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="8355e-134">Mit diesem Befehl wird ein Server für einen Speicher Synchronisierungsdienst registriert, der eine Vertrauensstellung herstellt.</span><span class="sxs-lookup"><span data-stu-id="8355e-134">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="8355e-135">PowerShell oder das Azure-Portal kann dann verwendet werden, um die Synchronisierung auf diesem Server zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8355e-135">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="8355e-136">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-136">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="8355e-137">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8355e-137">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="8355e-138">Ohne mindestens einen Cloud-Endpunkt können keine anderen Server Endpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8355e-138">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="8355e-139">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8355e-139">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="8355e-140">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8355e-140">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="8355e-141">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-141">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="8355e-142">Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8355e-142">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="8355e-143">Die Synchronisierung mit diesem Speicherort wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="8355e-143">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="8355e-144">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8355e-144">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="8355e-145">Mit diesem Befehl wird der angegebene Speicher Synchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8355e-145">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="8355e-146">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="8355e-146">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="8355e-147">Nur zur Problembehandlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8355e-147">Use for troubleshooting only.</span></span> <span data-ttu-id="8355e-148">Mit diesem Befehl wird das Storage-Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8355e-148">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="8355e-149">Satz-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8355e-149">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="8355e-150">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="8355e-150">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="8355e-151">Registrierung aufheben-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="8355e-151">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="8355e-152">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8355e-152">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="8355e-153">Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="8355e-153">This command will unregister a server from it's storage sync service.</span></span>

