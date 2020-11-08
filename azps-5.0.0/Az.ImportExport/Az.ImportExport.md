---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177575"
---
# <span data-ttu-id="8b53c-101">AZ. DataObjects-Modul</span><span class="sxs-lookup"><span data-stu-id="8b53c-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="8b53c-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b53c-102">Description</span></span>
<span data-ttu-id="8b53c-103">Microsoft Azure PowerShell: DataObjects-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b53c-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="8b53c-104">AZ. DataObjects-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8b53c-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="8b53c-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8b53c-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="8b53c-106">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="8b53c-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="8b53c-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="8b53c-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="8b53c-108">Gibt die BitLocker-Schlüssel für alle Laufwerke des angegebenen Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="8b53c-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="8b53c-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="8b53c-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="8b53c-110">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger senden können, die einem Import-oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8b53c-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="8b53c-111">Eine Position ist ein Azure-Bereich.</span><span class="sxs-lookup"><span data-stu-id="8b53c-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="8b53c-112">Neu – AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8b53c-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="8b53c-113">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b53c-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="8b53c-114">Neu – AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="8b53c-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="8b53c-115">Erstellen Sie ein driverlist-Objekt für DataObjects.</span><span class="sxs-lookup"><span data-stu-id="8b53c-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="8b53c-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8b53c-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="8b53c-117">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8b53c-117">Deletes an existing job.</span></span>
<span data-ttu-id="8b53c-118">Nur Aufträge im Status "erstellen" oder "abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8b53c-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="8b53c-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="8b53c-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="8b53c-120">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="8b53c-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="8b53c-121">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, die den Import-oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="8b53c-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="8b53c-122">Sie kann auch verwendet werden, um einen vorhandenen Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="8b53c-122">It can also be used to cancel an existing job.</span></span>

