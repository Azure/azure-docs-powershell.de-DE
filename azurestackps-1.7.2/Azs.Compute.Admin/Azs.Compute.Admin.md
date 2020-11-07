---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 4194899ad20356c8cde68110553495558d3816d5
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "93650134"
---
# <span data-ttu-id="31cdc-101">AZS. Compute. Admin-Modul</span><span class="sxs-lookup"><span data-stu-id="31cdc-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="31cdc-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31cdc-102">Description</span></span>
<span data-ttu-id="31cdc-103">Preview-Version des AzureStack-Compute-Operator-Moduls, das Funktionen zum Verwalten von Compute-Kontingenten, Platt Form Abbildern und Virtual Machine-Erweiterungen sowie zu den Migrations Aufträgen für verwaltete Datenträger bereitstellt, um den Speicher zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="31cdc-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="31cdc-104">AZS. Compute. admin-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31cdc-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="31cdc-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="31cdc-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="31cdc-106">Fügen Sie ein Bild einer virtuellen Computerplattform aus einer bestimmten Bild Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="31cdc-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="31cdc-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="31cdc-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="31cdc-108">Erstellen Sie ein neues Abbild der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="31cdc-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="31cdc-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="31cdc-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="31cdc-110">Gibt Kontingente zurück, die die Kontingentgrenzen für Compute-Objekte angeben.</span><span class="sxs-lookup"><span data-stu-id="31cdc-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="31cdc-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="31cdc-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="31cdc-112">Gibt die Liste der verwalteten Datenträger zurück, die in der angegebenen Freigabe migriert werden können.</span><span class="sxs-lookup"><span data-stu-id="31cdc-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="31cdc-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="31cdc-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="31cdc-114">Gibt die Liste der verwalteten Datenträger Migrationsaufträge zurück.</span><span class="sxs-lookup"><span data-stu-id="31cdc-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="31cdc-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="31cdc-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="31cdc-116">Gibt Bilder virtueller Computer zurück, die in das Platform-Image-Repository geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="31cdc-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="31cdc-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="31cdc-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="31cdc-118">Gibt die aktuell verfügbaren Virtual Machine-Bild Erweiterungen zurück.</span><span class="sxs-lookup"><span data-stu-id="31cdc-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="31cdc-119">Neu – AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="31cdc-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="31cdc-120">Erstellen Sie ein neues Compute-Kontingent, das zum Begrenzen von Compute-Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31cdc-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="31cdc-121">Neu – AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="31cdc-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="31cdc-122">Startet einen Auftrag für die verwaltete Datenträger Migration, um verwaltete Datenträger zur angegebenen Zielfreigabe zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="31cdc-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="31cdc-123">Neu – AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="31cdc-123">New-AzsDataDiskObject</span></span>](New-AzsDataDiskObject.md)
<span data-ttu-id="31cdc-124">Erstellt einen Daten Datenträger, der zum Erstellen eines neuen Platt Form Bilds für eine virtuelle Maschine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31cdc-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="31cdc-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="31cdc-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="31cdc-126">Löscht das angegebene Compute-Kontingent.</span><span class="sxs-lookup"><span data-stu-id="31cdc-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="31cdc-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="31cdc-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="31cdc-128">Löschen Sie ein Bild eines virtuellen Computers aus dem Platform-Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="31cdc-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="31cdc-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="31cdc-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="31cdc-130">Löscht ein Abbild einer virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="31cdc-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="31cdc-131">Satz-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="31cdc-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="31cdc-132">Aktualisieren eines vorhandenen Compute-Kontingents mit den bereitgestellten Parametern</span><span class="sxs-lookup"><span data-stu-id="31cdc-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="31cdc-133">Stopp-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="31cdc-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="31cdc-134">Abbrechen eines verwalteten Datenträger Migrationsauftrags</span><span class="sxs-lookup"><span data-stu-id="31cdc-134">Cancel a managed disk migration job.</span></span>

