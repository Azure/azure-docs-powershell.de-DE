---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 8b74dd57a85a39403f56840dd0fc54b3f25184f1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006972"
---
# <span data-ttu-id="b0b93-101">AZS. Compute. Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="b0b93-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="b0b93-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b93-102">Description</span></span>
<span data-ttu-id="b0b93-103">Preview-Version des AzureStack Compute-Administrator-Moduls, das Funktionen zum Verwalten von Compute-Kontingenten, Platt Form Abbildern und Virtual Machine-Erweiterungen sowie für die Migration von verwalteten Datenträgern zum wieder angleichen des Speichers bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b0b93-103">Preview release of the AzureStack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="b0b93-104">AZS. Compute. admin-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b0b93-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="b0b93-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b0b93-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="b0b93-106">Fügen Sie ein Bild einer virtuellen Computerplattform aus einer bestimmten Bild Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0b93-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="b0b93-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b0b93-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="b0b93-108">Erstellen Sie ein neues Abbild der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="b0b93-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="b0b93-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b0b93-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="b0b93-110">Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.</span><span class="sxs-lookup"><span data-stu-id="b0b93-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="b0b93-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="b0b93-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="b0b93-112">Gibt die Liste der verwalteten Datenträger zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="b0b93-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="b0b93-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b0b93-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="b0b93-114">Gibt die Liste der verwalteten Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="b0b93-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="b0b93-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b0b93-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="b0b93-116">Gibt Bilder virtueller Computer zurück, die in das Platform-Image-Repository geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="b0b93-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="b0b93-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b0b93-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="b0b93-118">Gibt die aktuell verfügbaren Virtual Machine-Bild Erweiterungen zurück.</span><span class="sxs-lookup"><span data-stu-id="b0b93-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="b0b93-119">Neu – AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b0b93-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="b0b93-120">Erstellen Sie ein neues Compute-Kontingent, das zum Begrenzen von Compute-Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0b93-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="b0b93-121">Neu – AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b0b93-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="b0b93-122">Startet einen Auftrag für die verwaltete Datenträger Migration, um verwaltete Datenträger zur angegebenen Zielfreigabe zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="b0b93-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="b0b93-123">Neu-datadiskobject</span><span class="sxs-lookup"><span data-stu-id="b0b93-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="b0b93-124">Erstellt einen Daten Datenträger, der zum Erstellen eines neuen Platt Form Bilds für eine virtuelle Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0b93-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="b0b93-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b0b93-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="b0b93-126">Löscht das angegebene Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="b0b93-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="b0b93-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b0b93-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="b0b93-128">Löschen Sie ein Bild eines virtuellen Computers aus dem Platform-Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="b0b93-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="b0b93-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="b0b93-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="b0b93-130">Löscht ein Abbild einer virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="b0b93-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="b0b93-131">Satz-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="b0b93-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="b0b93-132">Aktualisieren eines vorhandenen Compute-Kontingents mit den bereitgestellten Parametern</span><span class="sxs-lookup"><span data-stu-id="b0b93-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="b0b93-133">Stopp-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b0b93-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="b0b93-134">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="b0b93-134">Cancel a managed disk migration job.</span></span>

