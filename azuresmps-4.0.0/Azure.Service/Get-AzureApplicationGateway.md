---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005876"
---
# Get-AzureApplicationGateway

## Synopsis
Ruft ein Anwendungs Gateway ab.

## Syntax

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureApplicationGateway** " Ruft ein vorhandenes Azure Application-Gateway ab.

## Beispiele

### Beispiel 1: Abrufen eines Anwendungs Gateways
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

Dieser Befehl ruft das Anwendungs Gateway mit dem Namen ApplicationGateway06 ab.

### Beispiel 2: Abrufen aller Anwendungs Gateways
```
PS C:\> Get-AzureApplicationGateway
```

Dieser Befehl ruft alle Anwendungs Gateways unter Ihrem Abonnement ab.

## Parameter

### -Name
Gibt den Namen des Anwendungs Gateways an, das dieses Cmdlet erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## Ausgaben

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway>

## Notizen

## Verwandte Links

[Neu – AzureApplicationGateway](./New-AzureApplicationGateway.md)

[Remove-AzureApplicationGateway](./Remove-AzureApplicationGateway.md)

[Anfang-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stopp-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[Update-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


