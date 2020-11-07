---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658692"
---
# New-AzStorageSyncService

## Synopsis
Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt.

## Syntax

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ein Speicher Synchronisierungsdienst ist die Ressource der obersten Ebene für Azure-Dateisynchronisierung. Mit diesem Befehl wird ein neuer Speicher Synchronisierungsdienst in einer Ressourcengruppe erstellt. Wir empfehlen, so wenige Speicher Synchronisierungsdienste wie unbedingt erforderlich zu erstellen, um unterschiedliche Servergruppen in Ihrer Organisation zu unterscheiden. Ein Speicher Synchronisierungsdienst enthält Synchronisierungsgruppen und funktioniert auch als Ziel für die Registrierung Ihrer Server. Ein Server kann nur für einen einzelnen Speicher Synchronisierungsdienst registriert werden. Wenn Server jemals an der Synchronisierung desselben Satzes von Dateien teilnehmen müssen, registrieren Sie diese beim gleichen Speicher Synchronisierungsdienst.

## Beispiele

### Beispiel 1
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

Mit diesem Befehl wird ein Speicher Synchronisierungsdienst erstellt.

## Parameter

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

### -Standort
Speicherort für den Speicher Synchronisierungsdienst

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name des Speicher Synchronisierungs Diensts.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Synchronisierungsdienst-Tags für den Speicher.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService

## Notizen

## Verwandte Links
