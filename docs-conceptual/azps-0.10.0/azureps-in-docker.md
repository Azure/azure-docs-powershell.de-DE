---
title: Verwenden von Azure PowerShell in Docker
description: Hier finden Sie Informationen zur Verwendung einer in einem Docker-Image vorinstallierten Azure PowerShell-Instanz.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2b487abeecbffa6cd8b7b64276ab301619348385
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242017"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="e44c3-103">Verwenden von Azure PowerShell in Docker</span><span class="sxs-lookup"><span data-stu-id="e44c3-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="e44c3-104">Wir veröffentlichen Docker-Images, für die Azure PowerShell vorinstalliert ist.</span><span class="sxs-lookup"><span data-stu-id="e44c3-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="e44c3-105">Dieser Artikel veranschaulicht die ersten Schritte mit Azure PowerShell im Docker-Container.</span><span class="sxs-lookup"><span data-stu-id="e44c3-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="e44c3-106">Ermitteln verfügbarer Images</span><span class="sxs-lookup"><span data-stu-id="e44c3-106">Finding available images</span></span>

<span data-ttu-id="e44c3-107">Für die veröffentlichten Images ist mindestens Docker 17.05 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e44c3-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="e44c3-108">Es wird auch erwartet, dass Sie Docker ohne `sudo` oder lokale Administratorrechte ausführen können.</span><span class="sxs-lookup"><span data-stu-id="e44c3-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="e44c3-109">Befolgen Sie die offiziellen [Anweisungen][install] von Docker zur ordnungsgemäßen Installation von `docker`.</span><span class="sxs-lookup"><span data-stu-id="e44c3-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="e44c3-110">Das neueste Containerimage enthält die aktuelle PowerShell-Version sowie die aktuellen Azure PowerShell-Module, die für das Az-Modul unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e44c3-110">The latest container image contains the latest version of PowerShell and the latest Azure PowerShell modules supported with the Az module.</span></span>

<span data-ttu-id="e44c3-111">Für jede neue Version des Az-Moduls veröffentlichen wir ein Image für die folgenden Betriebssysteme:</span><span class="sxs-lookup"><span data-stu-id="e44c3-111">For each new release of the Az module we are releasing an image for the following operating systems:</span></span>

- <span data-ttu-id="e44c3-112">Ubuntu 18.04 (Standard)</span><span class="sxs-lookup"><span data-stu-id="e44c3-112">Ubuntu 18.04 (default)</span></span>
- <span data-ttu-id="e44c3-113">Debian 9</span><span class="sxs-lookup"><span data-stu-id="e44c3-113">Debian 9</span></span>
- <span data-ttu-id="e44c3-114">CentOS 7</span><span class="sxs-lookup"><span data-stu-id="e44c3-114">CentOs 7</span></span>

<span data-ttu-id="e44c3-115">Eine vollständige Liste der verfügbaren Images finden Sie auf unserer Seite mit den [Docker-Images][az image].</span><span class="sxs-lookup"><span data-stu-id="e44c3-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="e44c3-116">Verwenden von Azure PowerShell in einem Container</span><span class="sxs-lookup"><span data-stu-id="e44c3-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="e44c3-117">Die folgenden Schritte zeigen die Docker-Befehle, die zum Herunterladen des Images und zum Starten einer interaktiven PowerShell-Sitzung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e44c3-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="e44c3-118">Laden Sie das aktuelle Azure PowerShell-Image herunter.</span><span class="sxs-lookup"><span data-stu-id="e44c3-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="e44c3-119">Führen Sie den Azure PowerShell-Container im interaktiven Modus aus:</span><span class="sxs-lookup"><span data-stu-id="e44c3-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

<span data-ttu-id="e44c3-120">Bei Windows Docker-Hosts müssen Sie die Docker-Dateifreigabe aktivieren, um zuzulassen, dass lokale Laufwerke unter Windows für Linux-Container freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e44c3-120">For Windows Docker hosts, you must enable Docker File Sharing to allow local drives on Windows to be shared with Linux containers.</span></span> <span data-ttu-id="e44c3-121">Weitere Informationen finden Sie unter [Erste Schritte mit Docker für Windows][file-sharing].</span><span class="sxs-lookup"><span data-stu-id="e44c3-121">For more information see [Get started with Docker for Windows][file-sharing].</span></span>

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="e44c3-122">Interaktives Ausführen des Azure PowerShell-Containers mithilfe der Hostauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="e44c3-122">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="e44c3-123">Wenn Sie Azure PowerShell bereits auf dem System installiert haben, auf dem auch Docker gehostet wird, haben Sie unter Umständen Azure-Anmeldeinformationen zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="e44c3-123">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="e44c3-124">Diese Anmeldeinformationen können in der PowerShell-Sitzung verwendet werden, die im Docker-Container ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e44c3-124">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="e44c3-125">Standardmäßig befinden sich die zwischengespeicherten Anmeldeinformationen im Verzeichnis `$HOME/.Azure` auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="e44c3-125">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="e44c3-126">Der Docker-Dienst muss Zugriff auf diesen Speicherort haben, um auf die Anmeldeinformationen zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="e44c3-126">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="e44c3-127">Der folgende Befehl startet den Container mit dem eingebundenen Anmeldeinformationscache sowie eine interaktive PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e44c3-127">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="e44c3-128">Entfernen des Images, sobald es nicht mehr benötigt wird</span><span class="sxs-lookup"><span data-stu-id="e44c3-128">Remove the image when no longer needed</span></span>

<span data-ttu-id="e44c3-129">Der folgende Befehl dient zum Löschen des Docker-Containers, wenn Sie ihn nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="e44c3-129">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="e44c3-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e44c3-130">Next steps</span></span>

<span data-ttu-id="e44c3-131">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="e44c3-131">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
