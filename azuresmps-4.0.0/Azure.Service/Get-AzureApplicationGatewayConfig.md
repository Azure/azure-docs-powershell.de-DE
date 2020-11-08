---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005871"
---
# Get-AzureApplicationGatewayConfig

## Synopsis
Ruft einen Anwendungs Gateway-Konfigurationskontext ab.

## Syntax

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureApplicationGatewayConfig** " Ruft einen Azure Application Gateway-Konfigurationskontext ab.
Ein Kontext umfasst sowohl ein Konfigurationsobjekt als auch eine XML-Konfiguration.
Sie können die XML-Konfiguration in einer Datei speichern.

## Beispiele

### Beispiel 1: Abrufen einer Application Gateway-Konfiguration und speichern in einer Datei
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

Dieser Befehl ruft die Konfiguration für ein Anwendungs Gateway mit dem Namen ApplicationGateway06 ab.
Der Befehl speichert ihn in der Datei im angegebenen Pfad.

## Parameter

### -ExportToFile
Gibt einen Dateipfad an, zu dem dieses Cmdlet die Konfiguration im XML-Format speichert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet Konfigurationsinformationen erhält.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext

## Notizen

## Verwandte Links

[Satz-AzureApplicationGatewayConfig](./Set-AzureApplicationGatewayConfig.md)


