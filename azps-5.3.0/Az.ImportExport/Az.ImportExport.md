---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472528"
---
# <span data-ttu-id="4ecfe-101">Az.ImportExport-Modul</span><span class="sxs-lookup"><span data-stu-id="4ecfe-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="4ecfe-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ecfe-102">Description</span></span>
<span data-ttu-id="4ecfe-103">Microsoft Azure PowerShell: ImportExport-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4ecfe-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="4ecfe-104">Az.ImportExport-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4ecfe-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="4ecfe-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4ecfe-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="4ecfe-106">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="4ecfe-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="4ecfe-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="4ecfe-108">Gibt die BitLocker-Schlüssel für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="4ecfe-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="4ecfe-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="4ecfe-110">Gibt die Details zu einem Speicherort zurück, an den Sie die einem Import- oder Exportauftrag zugeordneten Datenträger versenden können.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="4ecfe-111">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="4ecfe-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4ecfe-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="4ecfe-113">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="4ecfe-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="4ecfe-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="4ecfe-115">Erstellen Sie ein "DriverList"-Objekt für "ImportExport".</span><span class="sxs-lookup"><span data-stu-id="4ecfe-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="4ecfe-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4ecfe-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="4ecfe-117">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-117">Deletes an existing job.</span></span>
<span data-ttu-id="4ecfe-118">Nur Aufträge in den Zu Zustände "Erstellen" oder "Abgeschlossen" können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="4ecfe-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4ecfe-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="4ecfe-120">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="4ecfe-121">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, auf denen der Import- oder Exportauftrag ausgeführt wurde, an das Microsoft-Rechenzentrum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="4ecfe-122">Sie kann auch zum Abbrechen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ecfe-122">It can also be used to cancel an existing job.</span></span>

