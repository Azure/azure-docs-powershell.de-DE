---
title: Verwenden von Azure PowerShell in Docker
description: Hier finden Sie Informationen zur Verwendung einer in einem Docker-Image vorinstallierten Azure PowerShell-Instanz.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/20/2020
ms.openlocfilehash: b5ad201abcabbdc1a88db241b028d88f05054a14
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363185"
---
# <a name="using-azure-powershell-in-docker"></a>Verwenden von Azure PowerShell in Docker

Wir veröffentlichen Docker-Images, für die Azure PowerShell vorinstalliert ist. Dieser Artikel veranschaulicht die ersten Schritte mit Azure PowerShell im Docker-Container.

## <a name="finding-available-images"></a>Ermitteln verfügbarer Images

Für die veröffentlichten Images ist mindestens Docker 17.05 erforderlich. Es wird auch erwartet, dass Sie Docker ohne `sudo` oder lokale Administratorrechte ausführen können. Befolgen Sie die offiziellen [Anweisungen][install] von Docker zur ordnungsgemäßen Installation von `docker`.

Das neueste Containerimage enthält die aktuelle PowerShell-Version sowie die aktuellen Azure PowerShell-Module, die für das Az-Modul unterstützt werden.

Für jede neue Version des Az-Moduls veröffentlichen wir ein Image für die folgenden Betriebssysteme:

- Ubuntu 18.04 (Standard)
- Debian 9
- CentOS 7

Eine vollständige Liste der verfügbaren Images finden Sie auf unserer Seite mit den [Docker-Images][az image].

## <a name="using-azure-powershell-in-a-container"></a>Verwenden von Azure PowerShell in einem Container

Die folgenden Schritte zeigen die Docker-Befehle, die zum Herunterladen des Images und zum Starten einer interaktiven PowerShell-Sitzung erforderlich sind.

1. Laden Sie das aktuelle Azure PowerShell-Image herunter.

   ```console
   docker pull mcr.microsoft.com/azure-powershell
   ```

1. Führen Sie den Azure PowerShell-Container im interaktiven Modus aus:

   ```console
   docker run -it mcr.microsoft.com/azure-powershell pwsh
   ```

Bei Windows Docker-Hosts müssen Sie die Docker-Dateifreigabe aktivieren, um zuzulassen, dass lokale Laufwerke unter Windows für Linux-Container freigegeben werden. Weitere Informationen finden Sie unter [Erste Schritte mit Docker für Windows][file-sharing].

### <a name="run-the-azure-powershell-container-interactively-using-host-authentication"></a>Interaktives Ausführen des Azure PowerShell-Containers mithilfe der Hostauthentifizierung

Wenn Sie Azure PowerShell bereits auf dem System installiert haben, auf dem auch Docker gehostet wird, haben Sie unter Umständen Azure-Anmeldeinformationen zwischengespeichert. Diese Anmeldeinformationen können in der PowerShell-Sitzung verwendet werden, die im Docker-Container ausgeführt wird.

Standardmäßig befinden sich die zwischengespeicherten Anmeldeinformationen im Verzeichnis `$HOME/.Azure` auf dem Host. Der Docker-Dienst muss Zugriff auf diesen Speicherort haben, um auf die Anmeldeinformationen zugreifen zu können. Der folgende Befehl startet den Container mit dem eingebundenen Anmeldeinformationscache sowie eine interaktive PowerShell-Sitzung.

```console
docker run -it -v ~/.Azure/AzureRmContext.json:/root/.Azure/AzureRmContext.json -v ~/.Azure/TokenCache.dat:/root/.Azure/TokenCache.dat mcr.microsoft.com/azure-powershell pwsh
```

### <a name="remove-the-image-when-no-longer-needed"></a>Entfernen des Images, sobald es nicht mehr benötigt wird

Der folgende Befehl dient zum Löschen des Docker-Containers, wenn Sie ihn nicht mehr benötigen.

```console
docker rmi mcr.microsoft.com/azure-powershell
```

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu Azure PowerShell-Modulen und den zugehörigen Features finden Sie unter [Erste Schritte mit Azure PowerShell](get-started-azureps.md).

<!-- link references -->
[install]: https://docs.docker.com/engine/installation/
[powershell image]: https://hub.docker.com/_/microsoft-powershell
[az image]: https://hub.docker.com/_/microsoft-azure-powershell
[file-sharing]: https://docs.docker.com/docker-for-windows/#file-sharing
