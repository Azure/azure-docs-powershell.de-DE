---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: c73e82285a848c9ff6abf197eb3352cf708a2f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921992"
---
# <span data-ttu-id="10f6a-101">Az.DataMigration Module</span><span class="sxs-lookup"><span data-stu-id="10f6a-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="10f6a-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10f6a-102">Description</span></span>
<span data-ttu-id="10f6a-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="10f6a-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="10f6a-104">Az.DataMigration-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="10f6a-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="10f6a-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="10f6a-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="10f6a-106">Ruft die Eigenschaften eines Azure-Datenbankmigrationsprojekts ab.</span><span class="sxs-lookup"><span data-stu-id="10f6a-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="10f6a-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="10f6a-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="10f6a-108">Ruft die Eigenschaften ab, die einer Instanz des Azure-Datenbankmigrationsdiensts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="10f6a-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="10f6a-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="10f6a-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="10f6a-110">Ruft das PSProjectTask-Objekt ab, das einer Azure Database Migration Service-Migrationsaufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="10f6a-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="10f6a-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="10f6a-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="10f6a-112">Erstellt einen neuen Befehl, der für eine vorhandene DMS-Aufgabe ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10f6a-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="10f6a-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="10f6a-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="10f6a-114">Erstellt ein neues Verbindungsinfoobjekt, das den Servertyp und den Namen für die Verbindung an gibt.</span><span class="sxs-lookup"><span data-stu-id="10f6a-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="10f6a-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="10f6a-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="10f6a-116">Erstellt das DatabaseInfo-Objekt für den Azure Database Migration Service, der die Datenbankquelle für die Migration angibt.</span><span class="sxs-lookup"><span data-stu-id="10f6a-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="10f6a-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="10f6a-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="10f6a-118">Erstellt das FileShare-Objekt für den Azure Database Migration Service, der die lokale Netzwerkfreigabe angibt, in die die Quelldatenbanksicherungen ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10f6a-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="10f6a-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="10f6a-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="10f6a-120">Erstellt ein neues Azure Database Migration Service-Projekt.</span><span class="sxs-lookup"><span data-stu-id="10f6a-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="10f6a-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="10f6a-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="10f6a-122">Erstellt ein Datenbankeingabeobjekt, das Informationen zu Quell- und Zieldatenbanken für die Migration enthält.</span><span class="sxs-lookup"><span data-stu-id="10f6a-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="10f6a-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="10f6a-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="10f6a-124">Erstellt eine neue Instanz des Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="10f6a-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="10f6a-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="10f6a-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="10f6a-126">Erstellt ein Datenbankinformationsobjekt speziell für das Synchronisierungsszenario, das für eine Migrationsaufgabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10f6a-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="10f6a-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="10f6a-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="10f6a-128">Erstellt und startet eine Datenmigrationsaufgabe im Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="10f6a-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="10f6a-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="10f6a-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="10f6a-130">Entfernt ein Azure-Datenbankmigrationsdienstprojekt aus Azure.</span><span class="sxs-lookup"><span data-stu-id="10f6a-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="10f6a-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="10f6a-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="10f6a-132">Entfernt eine Instanz des Azure-Datenbankmigrationsdiensts aus Azure.</span><span class="sxs-lookup"><span data-stu-id="10f6a-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="10f6a-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="10f6a-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="10f6a-134">Entfernt eine Azure-Datenbankmigrationsdienstaufgabe aus Azure.</span><span class="sxs-lookup"><span data-stu-id="10f6a-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="10f6a-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="10f6a-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="10f6a-136">Startet eine Instanz des Azure-Datenbankmigrationsdiensts in einem beendeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="10f6a-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="10f6a-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="10f6a-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="10f6a-138">Beendet eine Instanz des Azure-Datenbankmigrationsdiensts, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="10f6a-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="10f6a-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="10f6a-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="10f6a-140">Beendet eine Azure-Datenbankmigrationsdienstaufgabe, die sich in einem ausgeführten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="10f6a-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

