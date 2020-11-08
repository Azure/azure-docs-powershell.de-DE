---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005870"
---
# Get-AzureApplicationGatewaySslCertificate

## Synopsis
Ruft Application Gateway-Zertifikate ab.

## Syntax

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureApplicationGatewaySslCertificate** " ruft SSL-Zertifikate (Secure Sockets Layer) für ein Azure Application Gateway ab.

## Beispiele

### Beispiel 1: Abrufen eines SSL-Zertifikats
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

Dieser Befehl ruft ein SSL-Zertifikat mit dem Namen SslCertificate13 auf dem Anwendungs Gateway mit dem Namen ApplicationGateway08 ab.

### Beispiel 2: Abrufen aller SSL-Zertifikate
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

Dieser Befehl ruft alle SSL-Zertifikate auf dem Application Gateway mit dem Namen ApplicationGateway08 ab.

## Parameter

### -CertificateName
Gibt den Namen eines SSL-Zertifikats an.
Dieses Cmdlet ruft das Zertifikat ab, das dieser Parameter angibt.

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

### -Name
Gibt den Namen des Anwendungs Gateways an, von dem dieses Cmdlet ein SSL-Zertifikat erhält.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate>

## Notizen

## Verwandte Links

[Add-AzureApplicationGatewaySslCertificate](./Add-AzureApplicationGatewaySslCertificate.md)

[Remove-AzureApplicationGatewaySslCertificate](./Remove-AzureApplicationGatewaySslCertificate.md)
