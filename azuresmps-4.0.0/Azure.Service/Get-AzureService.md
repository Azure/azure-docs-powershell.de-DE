---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006515"
---
# Get-AzureService

## Synopsis
Gibt ein Objekt mit Informationen zu den Cloud-Diensten für das aktuelle Abonnement zurück.

## Syntax

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureService** " gibt ein List-Objekt mit allen Azure-Cloud-Diensten zurück, die dem aktuellen Abonnement zugeordnet sind.
Wenn Sie den Parameter *ServiceName* angeben, gibt **Get-AzureService** Informationen nur für den übereinstimmenden Dienst zurück.

## Beispiele

### Beispiel 1: Abrufen von Informationen zu allen Diensten
```
PS C:\> Get-AzureService
```

Dieser Befehl gibt ein Objekt zurück, das Informationen zu allen Azure-Diensten enthält, die dem aktuellen Abonnement zugeordnet sind.

### Beispiel 2: Abrufen von Informationen zu einem bestimmten Dienst
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Dieser Befehl gibt Informationen zum $MySvc Dienst zurück.

### Beispiel 3: Anzeigen verfügbarer Methoden und Eigenschaften
```
PS C:\> Get-AzureService | Get-Member
```

Mit diesem Befehl werden die Eigenschaften und Methoden angezeigt, die über das Cmdlet **Get-AzureService** zur Verfügung stehen.

## Parameter

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

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

### -ServiceName
Gibt den Namen eines Diensts an, auf dem Informationen zurückgegeben werden sollen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### HostedServiceContext

## Notizen

## Verwandte Links

[Neu – AzureService](./New-AzureService.md)

[Satz-AzureService](./Set-AzureService.md)


