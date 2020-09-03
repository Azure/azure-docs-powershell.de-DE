---
title: Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen
description: Hier erfahren Sie, wie Sie Azure PowerShell-Cmdlets mithilfe von „-AsJob“ und „Start-Job“ parallel oder als Hintergrundaufgaben ausführen.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243156"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a><span data-ttu-id="3f5d7-103">Ausführen von Azure PowerShell-Cmdlets in PowerShell-Aufträgen</span><span class="sxs-lookup"><span data-stu-id="3f5d7-103">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>

<span data-ttu-id="3f5d7-104">Da von Azure PowerShell eine Verbindung mit einer Azure-Cloud hergestellt und auf Antworten gewartet werden muss, wird Ihre PowerShell-Sitzung durch die meisten dieser Cmdlets blockiert, bis eine Antwort von der Cloud empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-104">Azure PowerShell depends on connecting to an Azure cloud and waiting for responses, so most of these cmdlets block your PowerShell session until they get a response from the cloud.</span></span>
<span data-ttu-id="3f5d7-105">Mithilfe von PowerShell-Aufträgen können Sie Cmdlets im Hintergrund ausführen oder gleichzeitig mehrere Azure-Aufgaben in einer einzelnen PowerShell-Sitzung erledigen.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-105">Powershell Jobs let you run cmdlets in the background or do multiple tasks on Azure at once, from inside a single PowerShell session.</span></span>

<span data-ttu-id="3f5d7-106">Dieser Artikel enthält eine kurze Übersicht über das Ausführen von Azure PowerShell-Cmdlets als PowerShell-Aufträge sowie über das Überprüfen des Abschlusses.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-106">This article is a brief overview of how to run Azure PowerShell cmdlets as PowerShell Jobs and check for completion.</span></span> <span data-ttu-id="3f5d7-107">Wenn Sie Befehle in Azure PowerShell ausführen möchten, müssen Sie Azure PowerShell-Kontexte verwenden. Diese werden unter [Azure-Kontexte und -Anmeldeinformationen](context-persistence.md) ausführlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-107">Running commands in Azure PowerShell requires the use of Azure PowerShell contexts, which are covered in detail in [Azure contexts and sign-in credentials](context-persistence.md).</span></span>
<span data-ttu-id="3f5d7-108">Weitere Informationen zu PowerShell-Aufträgen finden Sie unter [Informationen zu Aufträgen](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="3f5d7-108">To learn more about PowerShell Jobs, see [About PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="azure-contexts-with-powershell-jobs"></a><span data-ttu-id="3f5d7-109">Azure-Kontexte mit PowerShell-Aufträgen</span><span class="sxs-lookup"><span data-stu-id="3f5d7-109">Azure contexts with PowerShell jobs</span></span>

<span data-ttu-id="3f5d7-110">Da PowerShell-Aufträge als separate Prozesse ohne angefügte PowerShell-Sitzung ausgeführt werden, müssen Ihre Azure-Anmeldeinformationen an sie weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-110">PowerShell Jobs are run as separate processes without an attached PowerShell session, so your Azure credentials must be shared with them.</span></span> <span data-ttu-id="3f5d7-111">Anmeldeinformationen werden mithilfe einer der folgenden Methoden als Azure-Kontextobjekte übergeben:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-111">Credentials are passed as Azure context objects, using one of these methods:</span></span>

* <span data-ttu-id="3f5d7-112">Automatische Kontextpersistenz:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-112">Automatic context persistence.</span></span> <span data-ttu-id="3f5d7-113">Die Kontextpersistenz ist standardmäßig aktiviert und behält Ihre Anmeldeinformationen über mehrere Sitzungen hinweg bei.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-113">Context persistence is enabled by default and preserves your sign-in information across multiple sessions.</span></span> <span data-ttu-id="3f5d7-114">Bei aktivierter Kontextpersistenz wird der aktuelle Azure-Kontext an den neuen Prozess übergeben:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-114">With context persistence enabled, the current Azure context is passed to the new process:</span></span>

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* <span data-ttu-id="3f5d7-115">Verwendung des Parameters `-AzContext` mit beliebigen Azure PowerShell-Cmdlets, um ein Azure-Kontextobjekt bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-115">Use the `-AzContext` parameter with any Azure PowerShell cmdlets to provide an Azure context object:</span></span>

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  <span data-ttu-id="3f5d7-116">Bei deaktivierter Kontextpersistenz wird das Argument `-AzContext` benötigt.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-116">If context persistence is disabled, the `-AzContext` argument is required.</span></span>

* <span data-ttu-id="3f5d7-117">Verwendung des Schalters `-AsJob`, der von einigen Azure PowerShell-Cmdlets bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-117">Use the `-AsJob` switch provided by some Azure PowerShell cmdlets.</span></span> <span data-ttu-id="3f5d7-118">Dieser Schalter startet das Cmdlet automatisch als PowerShell-Auftrag und verwendet dabei den derzeit aktiven Azure-Kontext:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-118">This switch automatically starts the cmdlet as a PowerShell Job, using the currently active Azure context:</span></span>

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  <span data-ttu-id="3f5d7-119">Ob ein Cmdlet `-AsJob` unterstützt, erfahren Sie in der zugehörigen Referenzdokumentation.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-119">To see if a cmdlet supports `-AsJob`, check its reference documentation.</span></span> <span data-ttu-id="3f5d7-120">Für den Schalter `-AsJob` muss die automatische Kontextspeicherung nicht aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-120">The `-AsJob` switch doesn't require context autosave to be enabled.</span></span>

<span data-ttu-id="3f5d7-121">Der Status eines aktiven Auftrags kann mithilfe des Cmdlets [Get-Job](/powershell/module/microsoft.powershell.core/get-job) überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3f5d7-121">You can check the status of a running job with the [Get-Job](/powershell/module/microsoft.powershell.core/get-job) cmdlet.</span></span> <span data-ttu-id="3f5d7-122">Wenn Sie die bisherige Ausgabe eines Auftrags abrufen möchten, verwenden Sie das Cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).</span><span class="sxs-lookup"><span data-stu-id="3f5d7-122">To get the output from a job so far, use the [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job) cmdlet.</span></span>

<span data-ttu-id="3f5d7-123">Wenn Sie den Fortschritt eines Vorgangs remote in Azure überprüfen möchten, verwenden Sie die Cmdlets vom Typ `Get-` für die Art der Ressource, die durch den Auftrag geändert wird:</span><span class="sxs-lookup"><span data-stu-id="3f5d7-123">To check an operation's progress remotely on Azure, use the `Get-` cmdlets associated with the type of resource being modified by the job:</span></span>

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a><span data-ttu-id="3f5d7-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f5d7-124">See Also</span></span>

* [<span data-ttu-id="3f5d7-125">Azure PowerShell-Kontextobjekte</span><span class="sxs-lookup"><span data-stu-id="3f5d7-125">Azure PowerShell contexts</span></span>](context-persistence.md)
* [<span data-ttu-id="3f5d7-126">Informationen zu Aufträgen</span><span class="sxs-lookup"><span data-stu-id="3f5d7-126">About PowerShell Jobs</span></span>](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [<span data-ttu-id="3f5d7-127">Get-Job</span><span class="sxs-lookup"><span data-stu-id="3f5d7-127">Get-Job reference</span></span>](/powershell/module/microsoft.powershell.core/get-job)
* [<span data-ttu-id="3f5d7-128">Receive-Job</span><span class="sxs-lookup"><span data-stu-id="3f5d7-128">Receive-Job reference</span></span>](/powershell/module/microsoft.powershell.core/receive-job)
