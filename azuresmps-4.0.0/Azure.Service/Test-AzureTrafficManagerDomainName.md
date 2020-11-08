---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006141"
---
# Test-AzureTrafficManagerDomainName

## Synopsis
Überprüft, ob ein Domänenname als Datenverkehrs-Manager-Profil verfügbar ist.

## Syntax

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Test-AzureTrafficManagerDomainName** überprüft, ob ein Domänenname als Microsoft Azure Traffic Manager-Profil verfügbar ist.
Wenn der Domänenname verfügbar ist, gibt dieses Cmdlet den Wert $true zurück.

## Beispiele

### Beispiel 1: überprüfen, ob ein Domänenname verfügbar ist
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Dieser Befehl überprüft, ob der Domänenname ContosoApp.Trafficmanager.net als Datenverkehrs-Manager-Profil verfügbar ist.

## Parameter

### -Domänenname
Gibt den zu überprüfenden Domänennamen an.
Sie müssen die folgende Zeichenfolge einbeziehen: 

. Trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest. Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### System. Boolean
Dieses Cmdlet generiert $true oder $false.
Wenn der Domänenname verfügbar ist, gibt dieses Cmdlet den Wert $true zurück.

## Notizen

## Verwandte Links

