---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93650068"
---
# <span data-ttu-id="3c9c8-101">AZ. StorageSync-Modul</span><span class="sxs-lookup"><span data-stu-id="3c9c8-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="3c9c8-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c9c8-102">Description</span></span>
<span data-ttu-id="3c9c8-103">Mit den Cmdlets im Speicher Synchronisierungsmodul können Sie Vorgänge in Bezug auf die Azure-Dateisynchronisierung in PowerShell verwalten.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="3c9c8-104">AZ. StorageSync-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3c9c8-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="3c9c8-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3c9c8-106">Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="3c9c8-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3c9c8-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="3c9c8-108">Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="3c9c8-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3c9c8-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="3c9c8-110">Dieser Befehl listet alle Server auf, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="3c9c8-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3c9c8-112">Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="3c9c8-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3c9c8-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="3c9c8-114">Dieser Befehl listet alle Speicher Synchronisierungsdienste in einem bestimmten Bereich des Abonnements/der Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="3c9c8-115">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="3c9c8-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="3c9c8-116">Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="3c9c8-117">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="3c9c8-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="3c9c8-118">Dieser Befehl ruft alle Tiered-Dateien wieder auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="3c9c8-119">Neu – AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3c9c8-120">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="3c9c8-121">Neu – AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3c9c8-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="3c9c8-122">Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="3c9c8-123">Neu – AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3c9c8-124">Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="3c9c8-125">Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="3c9c8-126">Neu – AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3c9c8-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="3c9c8-127">Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="3c9c8-128">Registrieren-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3c9c8-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="3c9c8-129">Mit diesem Befehl wird ein Server für einen Speicher Synchronisierungsdienst registriert, der eine Vertrauensstellung herstellt.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="3c9c8-130">PowerShell oder das Azure-Portal kann dann verwendet werden, um die Synchronisierung auf diesem Server zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="3c9c8-131">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="3c9c8-132">Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="3c9c8-133">Ohne mindestens einen Cloud-Endpunkt können keine anderen Server Endpunkte in dieser Synchronisierungsgruppe synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="3c9c8-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="3c9c8-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="3c9c8-135">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="3c9c8-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3c9c8-137">Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="3c9c8-138">Die Synchronisierung mit diesem Speicherort wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="3c9c8-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="3c9c8-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="3c9c8-140">Mit diesem Befehl wird der angegebene Speicher Synchronisierungsdienst gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="3c9c8-141">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="3c9c8-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="3c9c8-142">Nur zur Problembehandlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-142">Use for troubleshooting only.</span></span> <span data-ttu-id="3c9c8-143">Mit diesem Befehl wird das Storage-Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="3c9c8-144">Satz-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c9c8-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="3c9c8-145">Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="3c9c8-146">Registrierung aufheben-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="3c9c8-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="3c9c8-147">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="3c9c8-148">Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="3c9c8-148">This command will unregister a server from it's storage sync service.</span></span>