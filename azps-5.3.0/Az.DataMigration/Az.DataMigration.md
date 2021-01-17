---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458027"
---
# <span data-ttu-id="0bef3-101">Az.DataMigration Module</span><span class="sxs-lookup"><span data-stu-id="0bef3-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="0bef3-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bef3-102">Description</span></span>
<span data-ttu-id="0bef3-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="0bef3-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="0bef3-104">Az.DataMigration-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0bef3-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="0bef3-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="0bef3-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="0bef3-106">Ruft die Eigenschaften eines Azure-Datenbankmigrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="0bef3-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="0bef3-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bef3-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="0bef3-108">Ruft die Eigenschaften ab, die einer Instanz des Azure Database Migration Service zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0bef3-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="0bef3-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0bef3-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="0bef3-110">Ruft das psProjectTask-Objekt ab, das einer Migrationsaufgabe des Azure Database Migration Service zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0bef3-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="0bef3-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="0bef3-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="0bef3-112">Erstellt einen neuen Befehl, der für eine vorhandene Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bef3-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="0bef3-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="0bef3-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="0bef3-114">Erstellt ein neues Verbindungsinformationsobjekt, das den Servertyp und den Namen für die Verbindung an gibt.</span><span class="sxs-lookup"><span data-stu-id="0bef3-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="0bef3-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="0bef3-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="0bef3-116">Erstellt das DatabaseInfo-Objekt für den Azure-Datenbankmigrationsdienst, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="0bef3-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="0bef3-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="0bef3-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="0bef3-118">Erstellt das Objekt "FileShare" für den Azure-Datenbankmigrationsdienst, der die lokale Netzwerkfreigabe angibt, an die die Quelldatenbanksicherungen durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0bef3-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="0bef3-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="0bef3-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="0bef3-120">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="0bef3-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="0bef3-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="0bef3-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="0bef3-122">Erstellt ein Datenbankeingabeobjekt, das Informationen zu Quell- und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="0bef3-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="0bef3-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bef3-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="0bef3-124">Erstellt eine neue Instanz des Azure-Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="0bef3-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="0bef3-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="0bef3-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="0bef3-126">Erstellt ein Datenbankinformationsobjekt speziell für das Synchronisierungsszenario, das für eine Migrationsaufgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0bef3-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="0bef3-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0bef3-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="0bef3-128">Erstellt und startet eine Datenmigrationsaufgabe im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="0bef3-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="0bef3-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="0bef3-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="0bef3-130">Entfernt ein Azure Database Migration Service-Projekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0bef3-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="0bef3-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bef3-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="0bef3-132">Entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0bef3-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="0bef3-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0bef3-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="0bef3-134">Entfernt eine Aufgabe des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="0bef3-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="0bef3-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bef3-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="0bef3-136">Startet eine Instanz des Azure-Datenbankmigrationsdiensts in einem angehaltenen Zustand.</span><span class="sxs-lookup"><span data-stu-id="0bef3-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="0bef3-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0bef3-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="0bef3-138">Beendet eine Instanz des Azure-Datenbankmigrationsdiensts, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="0bef3-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="0bef3-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="0bef3-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="0bef3-140">Beendet eine Aufgabe des Azure Database Migration Service, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="0bef3-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

