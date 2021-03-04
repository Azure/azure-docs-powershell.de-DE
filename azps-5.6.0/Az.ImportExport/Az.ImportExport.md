---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930507"
---
# <span data-ttu-id="94e16-101">Az.ImportExport Module</span><span class="sxs-lookup"><span data-stu-id="94e16-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="94e16-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94e16-102">Description</span></span>
<span data-ttu-id="94e16-103">Microsoft Azure PowerShell: ImportExport cmdlets</span><span class="sxs-lookup"><span data-stu-id="94e16-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="94e16-104">Az.ImportExport Cmdlets</span><span class="sxs-lookup"><span data-stu-id="94e16-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="94e16-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="94e16-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="94e16-106">Ruft Informationen zu einem vorhandenen Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="94e16-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="94e16-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="94e16-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="94e16-108">Gibt die BitLockertasten für alle Laufwerke im angegebenen Auftrag zurück.</span><span class="sxs-lookup"><span data-stu-id="94e16-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="94e16-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="94e16-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="94e16-110">Gibt die Details zu einem Speicherort zurück, an den Sie die Datenträger versenden können, die einem Import- oder Exportauftrag zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="94e16-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="94e16-111">Ein Speicherort ist eine Azure-Region.</span><span class="sxs-lookup"><span data-stu-id="94e16-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="94e16-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="94e16-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="94e16-113">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94e16-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="94e16-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="94e16-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="94e16-115">Erstellen Sie ein DriverList-Objekt für ImportExport.</span><span class="sxs-lookup"><span data-stu-id="94e16-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="94e16-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="94e16-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="94e16-117">Löscht einen vorhandenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="94e16-117">Deletes an existing job.</span></span>
<span data-ttu-id="94e16-118">Nur Aufträge im Zustände Erstellen oder Abgeschlossen können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="94e16-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="94e16-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="94e16-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="94e16-120">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="94e16-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="94e16-121">Sie können diesen Vorgang aufrufen, um den Import-/Exportdienst darüber zu informieren, dass die Festplatten, die den Import- oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="94e16-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="94e16-122">Sie kann auch zum Kündigen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94e16-122">It can also be used to cancel an existing job.</span></span>

