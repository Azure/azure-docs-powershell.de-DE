---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460147"
---
# Az.StorageSync-Modul
## Beschreibung
Mit den Cmdlets im Speichersynchronisierungsmodul können Sie Vorgänge im Zusammenhang mit der Azure File Sync in PowerShell verwalten.

## Az.StorageSync-Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl werden alle Cloudendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Dieser Befehl listet alle Synchronisierungsgruppen innerhalb eines bestimmten Speichersynchronisierungsdiensts auf.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Dieser Befehl listet alle Server auf, die für einen bestimmten Speichersynchronisierungsdienst registriert sind.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl werden alle Serverendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Mit diesem Befehl werden alle Speichersynchronisierungsdienste innerhalb eines bestimmten Bereichs der Abonnement-/Ressourcengruppe aufgeführt.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Mit diesem Befehl kann die Erkennung von Namespaceänderungen manuell initiiert werden. Es kann auf die gesamte Freigabe, den Unterordner oder eine Gruppe von Dateien ausgerichtet werden. Es können maximal 10.000 Änderungen erkannt werden. Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespace, damit die Änderungserkennung schnell und innerhalb eines Grenzwerts von 10.000 Änderungen abgeschlossen werden kann.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Sucht nach potenziellen Kompatibilitätsproblemen zwischen Ihrem System und der Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Dieser Befehl ruft alle mehrstufigen Dateien auf den lokalen Datenträger zurück.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird ein Azure File Sync-Cloudendpunkt in einer Synchronisierungsgruppe erstellt.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt. Dadurch kann der angegebene Pfad auf dem Server die Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe starten.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Dieser Befehl legt einen Speichersynchronisierungsdienst in einer Ressourcengruppe fest.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Mit diesem Befehl wird ein Server bei einem Speichersynchronisierungsdienst registriert, der eine Vertrauensstellung erstellt. PowerShell oder das Azure-Portal kann dann zum Konfigurieren der Synchronisierung auf diesem Server verwendet werden.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird der angegebene Cloudendpunkt aus einer Synchronisierungsgruppe gelöscht. Ohne mindestens einen Cloudendpunkt können keine anderen Serverendpunkte in dieser Synchronisierungsgruppe synchronisiert werden.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht. Die Synchronisierung mit diesem Speicherort wird sofort beendet.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Wird nur für die Problembehandlung verwendet. Mit diesem Befehl wird ein Rollup des Speichersynchronisierungsserverzertifikats ausgeführt, mit dem die Serveridentität für den Speichersynchronisierungsdienst beschrieben wird.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Warnung: Wenn Sie die Registrierung eines Servers aufheben, werden alle Serverendpunkte auf diesem Server überlappend gelöscht. Mit diesem Befehl wird die Registrierung eines Servers vom Speichersynchronisierungsdienst aufgehoben.

