---
title: Verwenden von Azure PowerShell in Docker
description: Hier finden Sie Informationen zur Verwendung einer in einem Docker-Image vorinstallierten Azure PowerShell-Instanz.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: a5746b71cfc41f7c6283b0e95b0940ca4b594ec7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402679"
---
# <a name="using-azure-powershell-in-docker"></a><span data-ttu-id="b83c8-103">Verwenden von Azure PowerShell in Docker</span><span class="sxs-lookup"><span data-stu-id="b83c8-103">Using Azure PowerShell in Docker</span></span>

<span data-ttu-id="b83c8-104">Wir veröffentlichen Docker-Images, für die Azure PowerShell vorinstalliert ist.</span><span class="sxs-lookup"><span data-stu-id="b83c8-104">We are publishing Docker images with Azure PowerShell preinstalled.</span></span> <span data-ttu-id="b83c8-105">Dieser Artikel veranschaulicht die ersten Schritte mit Azure PowerShell im Docker-Container.</span><span class="sxs-lookup"><span data-stu-id="b83c8-105">This article shows you how to get started using Azure PowerShell in the Docker container.</span></span>

## <a name="finding-available-images"></a><span data-ttu-id="b83c8-106">Ermitteln verfügbarer Images</span><span class="sxs-lookup"><span data-stu-id="b83c8-106">Finding available images</span></span>

<span data-ttu-id="b83c8-107">Für die veröffentlichten Images ist mindestens Docker 17.05 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b83c8-107">The released images require Docker 17.05 or newer.</span></span> <span data-ttu-id="b83c8-108">Es wird auch erwartet, dass Sie Docker ohne `sudo` oder lokale Administratorrechte ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b83c8-108">It is also expected that you are able to run Docker without `sudo` or local administrative rights.</span></span> <span data-ttu-id="b83c8-109">Befolgen Sie die offiziellen [Anweisungen][install] von Docker zur ordnungsgemäßen Installation von `docker`.</span><span class="sxs-lookup"><span data-stu-id="b83c8-109">Please follow Docker's official [instructions][install] to install `docker` correctly.</span></span>

<span data-ttu-id="b83c8-110">Die veröffentlichten Container werden auf der Grundlage der offiziellen PowerShell-Container erstellt. Anschließend wird das Az-Modul als Ebene hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b83c8-110">The released containers are built from the official PowerShell containers, then the Az module added as a layer.</span></span>

<span data-ttu-id="b83c8-111">Das neueste stabile Image umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b83c8-111">The latest stable image includes:</span></span>

- <span data-ttu-id="b83c8-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="b83c8-112">Ubuntu 18.04</span></span>
- <span data-ttu-id="b83c8-113">PowerShell-Version 6.2.4</span><span class="sxs-lookup"><span data-stu-id="b83c8-113">PowerShell version 6.2.4</span></span>
- <span data-ttu-id="b83c8-114">Das aktuelle Az-Modul von Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b83c8-114">Azure PowerShell most current Az module</span></span>

<span data-ttu-id="b83c8-115">Eine vollständige Liste der verfügbaren Images finden Sie auf unserer Seite mit den [Docker-Images][az image].</span><span class="sxs-lookup"><span data-stu-id="b83c8-115">A full list of available images can be found on our [Docker image][az image] page.</span></span>

## <a name="using-azure-powershell-in-a-container"></a><span data-ttu-id="b83c8-116">Verwenden von Azure PowerShell in einem Container</span><span class="sxs-lookup"><span data-stu-id="b83c8-116">Using Azure PowerShell in a container</span></span>

<span data-ttu-id="b83c8-117">Die folgenden Schritte zeigen die Docker-Befehle, die zum Herunterladen des Images und zum Starten einer interaktiven PowerShell-Sitzung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b83c8-117">The following steps show the Docker commands required to download the image and start an interactive PowerShell session.</span></span>

1. <span data-ttu-id="b83c8-118">Laden Sie das aktuelle Azure PowerShell-Image herunter.</span><span class="sxs-lookup"><span data-stu-id="b83c8-118">Download the latest azure-powershell image.</span></span>

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. <span data-ttu-id="b83c8-119">Führen Sie den Azure PowerShell-Container im interaktiven Modus aus:</span><span class="sxs-lookup"><span data-stu-id="b83c8-119">Run the azure-powershell container in interactive mode:</span></span>

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a><span data-ttu-id="b83c8-120">Interaktives Ausführen des Azure PowerShell-Containers mithilfe der Hostauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="b83c8-120">Run the azure-powershell container interactively using host authentication</span></span>

<span data-ttu-id="b83c8-121">Wenn Sie Azure PowerShell bereits auf dem System installiert haben, auf dem auch Docker gehostet wird, haben Sie unter Umständen Azure-Anmeldeinformationen zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="b83c8-121">If you have Azure PowerShell already installed on the system hosting Docker, you may have cached Azure credentials.</span></span> <span data-ttu-id="b83c8-122">Diese Anmeldeinformationen können in der PowerShell-Sitzung verwendet werden, die im Docker-Container ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b83c8-122">These credentials can be used in the PowerShell session running in the Docker container.</span></span>

<span data-ttu-id="b83c8-123">Standardmäßig befinden sich die zwischengespeicherten Anmeldeinformationen im Verzeichnis `$HOME/.Azure` auf dem Host.</span><span class="sxs-lookup"><span data-stu-id="b83c8-123">By default, the cached credentials are in `$HOME/.Azure` directory on your host.</span></span> <span data-ttu-id="b83c8-124">Der Docker-Dienst muss Zugriff auf diesen Speicherort haben, um auf die Anmeldeinformationen zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="b83c8-124">The Docker service must have access to this location to access the credentials.</span></span> <span data-ttu-id="b83c8-125">Der folgende Befehl startet den Container mit dem eingebundenen Anmeldeinformationscache sowie eine interaktive PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b83c8-125">The following command starts the container with the credential cache mounted and starts an interactive PowerShell session.</span></span>

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a><span data-ttu-id="b83c8-126">Entfernen des Images, sobald es nicht mehr benötigt wird</span><span class="sxs-lookup"><span data-stu-id="b83c8-126">Remove the image when no longer needed</span></span>

<span data-ttu-id="b83c8-127">Der folgende Befehl dient zum Löschen des Docker-Containers, wenn Sie ihn nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b83c8-127">The following command is used to delete the Docker container when you no longer need it.</span></span>

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a><span data-ttu-id="b83c8-128">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="b83c8-128">Next steps</span></span>

<span data-ttu-id="b83c8-129">Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b83c8-129">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell