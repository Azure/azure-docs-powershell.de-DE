---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302950"
---
# AZ. StorageSync-Modul
## Beschreibung
Mit den Cmdlets im Speicher Synchronisierungsmodul können Sie Vorgänge in Bezug auf die Azure-Dateisynchronisierung in PowerShell verwalten.

## AZ. StorageSync-Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Dieser Befehl listet alle Cloud-Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Dieser Befehl listet alle Synchronisierungsgruppen in einem bestimmten Speicher Synchronisierungsdienst auf.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Dieser Befehl listet alle Server auf, die für einen bestimmten Speicher Synchronisierungsdienst registriert sind.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Dieser Befehl listet alle Server Endpunkte innerhalb einer bestimmten Synchronisierungsgruppe auf.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Dieser Befehl listet alle Speicher Synchronisierungsdienste in einem bestimmten Bereich des Abonnements/der Ressourcengruppe auf.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren. Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden. Es können maximal 10.000 Änderungen erkannt werden. Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb einer 10.000-Änderungs Grenze abgeschlossen werden kann.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Überprüft mögliche Kompatibilitätsprobleme zwischen der System-und Azure-Dateisynchronisierung.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Dieser Befehl ruft alle Tiered-Dateien wieder auf den lokalen Datenträger zurück.

### [Neu – AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt in einer Synchronisierungsgruppe erstellt.

### [Neu – AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Dieser Befehl erstellt eine neue Synchronisierungsgruppe innerhalb eines angegebenen Speicher Synchronisierungs Diensts.

### [Neu – AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird ein neuer Serverendpunkt auf einem registrierten Server erstellt. Dadurch kann der angegebene Pfad auf dem Server mit der Synchronisierung der Dateien mit anderen Endpunkten in der Synchronisierungsgruppe beginnen.

### [Neu – AzStorageSyncService](New-AzStorageSyncService.md)
Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.

### [Satz-AzStorageSyncService](New-AzStorageSyncService.md)
Dieser Befehl legt einen Speicher Synchronisierungsdienst in einer Ressourcengruppe fest.

### [Registrieren-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Mit diesem Befehl wird ein Server für einen Speicher Synchronisierungsdienst registriert, der eine Vertrauensstellung herstellt. PowerShell oder das Azure-Portal kann dann verwendet werden, um die Synchronisierung auf diesem Server zu konfigurieren.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Mit diesem Befehl wird der angegebene Cloud-Endpunkt aus einer Synchronisierungsgruppe gelöscht. Ohne mindestens einen Cloud-Endpunkt können keine anderen Server Endpunkte in dieser Synchronisierungsgruppe synchronisiert werden.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht. Die Synchronisierung mit diesem Speicherort wird sofort beendet.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Mit diesem Befehl wird der angegebene Speicher Synchronisierungsdienst gelöscht.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Nur zur Problembehandlung verwenden. Mit diesem Befehl wird das Storage-Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.

### [Satz-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Dieser Befehl ermöglicht Änderungen an den anpassbaren Parametern eines Server Endpunkts.

### [Registrierung aufheben-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht. Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.

