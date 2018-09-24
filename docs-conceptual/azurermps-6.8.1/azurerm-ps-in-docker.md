---
title: Ausführen von Azure PowerShell in einem Docker-Container
description: Es wird beschrieben, wie Sie Azure PowerShell in einem Docker-Container ausführen.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304011"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="60946-103">Ausführen von Azure PowerShell in einem Docker-Container</span><span class="sxs-lookup"><span data-stu-id="60946-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="60946-104">Microsoft veröffentlicht Docker-Images, für die Azure PowerShell vorinstalliert ist.</span><span class="sxs-lookup"><span data-stu-id="60946-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="60946-105">Diese Images können für das Experimentieren mit Azure PowerShell oder das Ausführen in einer isolierten Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60946-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="60946-106">Es sind auch Images mit PowerShell Core und PowerShell 5 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="60946-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="60946-107">Environment</span><span class="sxs-lookup"><span data-stu-id="60946-107">Environment</span></span> | <span data-ttu-id="60946-108">Docker-Image</span><span class="sxs-lookup"><span data-stu-id="60946-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="60946-109">PowerShell unter Windows</span><span class="sxs-lookup"><span data-stu-id="60946-109">PowerShell on Windows</span></span> | [<span data-ttu-id="60946-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="60946-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="60946-111">PowerShell Core unter Windows</span><span class="sxs-lookup"><span data-stu-id="60946-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="60946-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="60946-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="60946-113">PowerShell Core unter Linux</span><span class="sxs-lookup"><span data-stu-id="60946-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="60946-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="60946-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="60946-115">Verwenden Sie `docker run -it $ImageName`, um ein interaktives Terminal zu erhalten, wenn Sie einen dieser Container ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="60946-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="60946-116">Beispiel für die Ausführung eines Linux-Containers mit PowerShell Core:</span><span class="sxs-lookup"><span data-stu-id="60946-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="60946-117">Wenn Sie einen Windows-Container in Docker ausführen möchten, muss Windows als Hostbetriebssystem verwendet werden, und Docker muss für die Ausführung von Windows-Containern konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="60946-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="60946-118">Informationen zum Wechseln zwischen Windows- und Linux-Umgebungen in Docker finden Sie in der Docker-Dokumentation unter [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Wechseln zwischen Windows und Linux-Containern).</span><span class="sxs-lookup"><span data-stu-id="60946-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="60946-119">Verwenden eines PowerShell Core-Containers</span><span class="sxs-lookup"><span data-stu-id="60946-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="60946-120">Die PowerShell Core-Container werden mit PowerShell Core v6 bereitgestellt, und das Modul `AzureRM.NetCore` ist vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="60946-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="60946-121">Führen Sie das [Import-Module](/powershell/module/microsoft.powershell.core/import-module)-Cmdlet aus, und melden Sie sich dann mit Ihrem Azure-Konto an:</span><span class="sxs-lookup"><span data-stu-id="60946-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="60946-122">Verwenden des Windows-Containers mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="60946-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="60946-123">Für den Windows-Container ist das Modul `AzureRM` vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="60946-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="60946-124">Führen Sie das [Import-Module](/powershell/module/microsoft.powershell.core/import-module)-Cmdlet aus, und melden Sie sich dann mit Ihrem Azure-Konto an:</span><span class="sxs-lookup"><span data-stu-id="60946-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```