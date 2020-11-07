---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658690"
---
# Register-AzStorageSyncServer

## Synopsis
Mit diesem Befehl wird ein Server für einen Speicher Synchronisierungsdienst registriert, der eine Vertrauensstellung herstellt. PowerShell oder das Azure-Portal kann dann verwendet werden, um die Synchronisierung auf diesem Server zu konfigurieren.

## Syntax

### Objectparameterset (Standard)
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StringParameterSet
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentStringParameterSet
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit diesem Befehl wird ein Server für einen Speicher Synchronisierungsdienst, die Ressource der obersten Ebene für Azure-Dateisynchronisierung, registriert. Es wird eine Vertrauensstellung zwischen Server-und Speicher Synchronisierungsdienst erstellt, die sichere Datenübertragung und Verwaltungs Kanäle gewährleistet. PowerShell oder das Azure-Portal kann dann verwendet werden, um die Synchronisierungen auf diesem Server zu konfigurieren. Ein Server kann nur für einen einzelnen Speicher Synchronisierungsdienst registriert werden. Wenn Server jemals an der Synchronisierung desselben Satzes von Dateien teilnehmen müssen, registrieren Sie diese beim gleichen Speicher Synchronisierungsdienst.
Der Befehl muss lokal auf dem Server ausgeführt werden, der registriert werden soll, entweder direkt oder über eine Remote-PowerShell-Sitzung ausgeführt. Ein Remotecomputer Objekt kann nicht akzeptiert werden.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

Mit diesem Befehl wird der lokale Server registriert, auf dem dieser Befehl ausgeführt wird.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
StorageSyncService übergeordnete Ressourcen-ID

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageSyncServiceName
Der Name des StorageSyncService.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService

## Ausgaben

### Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer

## Notizen

## Verwandte Links
