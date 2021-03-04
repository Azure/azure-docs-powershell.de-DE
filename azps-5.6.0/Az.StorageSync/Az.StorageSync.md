---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929203"
---
# Az.StorageSync-Modul
## Beschreibung
Die Cmdlets im Speichersynchronisierungsmodul ermöglichen ihnen das Verwalten von Vorgängen im Zusammenhang mit Azure File Sync in PowerShell.

## Az.StorageSync-Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl werden alle Cloudendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Mit diesem Befehl werden alle Synchronisierungsgruppen innerhalb eines bestimmten Speichersynchronisierungsdiensts aufgeführt.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Mit diesem Befehl werden alle Server aufgeführt, die bei einem bestimmten Speichersynchronisierungsdienst registriert sind.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl werden alle Serverendpunkte innerhalb einer bestimmten Synchronisierungsgruppe aufgeführt.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Mit diesem Befehl werden alle Speichersynchronisierungsdienste in einem bestimmten Bereich der Abonnement-/Ressourcengruppe aufgeführt.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Dieser Befehl kann verwendet werden, um die Erkennung von Namespaceänderungen manuell zu initiieren. Sie kann auf die gesamte Freigabe, den Unterordner oder die gesamte Gruppe von Dateien ausgerichtet sein. Es können maximal 10.000 Änderungen erkannt werden. Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb eines Grenzwerts von 10.000 Änderungen abgeschlossen werden kann.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Sucht nach möglichen Kompatibilitätsproblemen zwischen Ihrem System und Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Dieser Befehl ruft alle mehrstufigen Dateien wieder auf den lokalen Datenträger zurück.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird ein Azure File Sync-Cloudendpunkt in einer Synchronisierungsgruppe erstellt.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Mit diesem Befehl wird eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speichersynchronisierungsdiensts erstellt.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt. Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Mit diesem Befehl wird ein neuer Speichersynchronisierungsdienst in einer Ressourcengruppe erstellt.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Mit diesem Befehl wird ein Speichersynchronisierungsdienst in einer Ressourcengruppe definiert.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Mit diesem Befehl wird ein Server bei einem Speichersynchronisierungsdienst registriert, der eine Vertrauensstellung erstellt. PowerShell oder das Azure-Portal können dann zum Konfigurieren der Synchronisierung auf diesem Server verwendet werden.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird der angegebene Cloudendpunkt aus einer Synchronisierungsgruppe gelöscht. Ohne mindestens einen Cloudendpunkt können keine anderen Serverendpunkte in dieser Synchronisierungsgruppe synchronisiert werden.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht. Die Synchronisierung mit diesem Speicherort wird sofort beendet.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Mit diesem Befehl wird der angegebene Speichersynchronisierungsdienst gelöscht.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Wird nur zur Problembehandlung verwendet. Mit diesem Befehl wird das Speichersynchronisierungsserverzertifikat rollt, das zum Beschreiben der Serveridentität für den Speichersynchronisierungsdienst verwendet wird.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Serverendpunkts.

### [Aufheben der Registrierung-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Warnung: Das Aufheben der Registrierung eines Servers führt dazu, dass alle Serverendpunkte auf diesem Server kaskadiert werden. Mit diesem Befehl wird die Registrierung eines Servers vom Speichersynchronisierungsdienst aufgehoben.

