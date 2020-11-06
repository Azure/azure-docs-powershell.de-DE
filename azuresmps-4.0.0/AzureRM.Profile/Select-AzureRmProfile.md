---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475209"
---
# Select-AzureRmProfile

## Synopsis
Lädt Azure-Authentifizierungsinformationen aus einer Datei.

## Syntax

### InMemoryProfile
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### ProfileFromDisk
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## Beschreibung
Das Select-AzureRmProfile-Cmdlet lädt Authentifizierungsinformationen aus einer Datei, um die Azure-Umgebung und den Kontext zu definieren.
Cmdlets, die Sie in der aktuellen Sitzung ausführen, verwenden diese Informationen, um Anforderungen an den Azure Resource Manager zu authentifizieren.

## Beispiele

### Beispiel 1: Auswählen eines Profils aus einem PSAzureProfile
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

In diesem Beispiel wird ein Profil aus einem PSAzureProfile ausgewählt, das an das Cmdlet übergeben wird.

### Beispiel 2: Auswählen eines Profils aus einer JSON-Datei
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

In diesem Beispiel wird ein Profil aus einer JSON-Datei ausgewählt, die an das Cmdlet übergeben wird. Diese JSON-Datei kann aus Save-AzureRmProfile erstellt werden.

## Parameter

### -Path
Gibt den Pfad zu Profilinformationen an, die mithilfe von Save-AzureRMProfile gespeichert werden.

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### PSAzureProfile

## Notizen

## Verwandte Links

[Get-AzureRMContext]()

