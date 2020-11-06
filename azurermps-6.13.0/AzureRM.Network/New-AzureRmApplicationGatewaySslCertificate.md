---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 37ad789afeaf8776eeab1c8977dfab8b4cd2681a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500194"
---
# New-AzureRmApplicationGatewaySslCertificate

## Synopsis
Erstellt ein SSL-Zertifikat für ein Azure Application-Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmApplicationGatewaySslCertificate** erstellt ein SSL-Zertifikat für ein Azure Application Gateway.

## Beispiele

### Beispiel 1: Erstellen eines SSL-Zertifikats für ein Azure Application Gateway
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

Dieser Befehl erstellt ein SSL-Zertifikat mit dem Namen "Cert01" für das Standard Anwendungsgateway und speichert das Ergebnis in der Variablen mit dem Namen "$CERT".

## Parameter

### -Certificatedatei
Gibt den Pfad der PFX-Datei des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des SSL-Zertifikats an, das von diesem Cmdlet erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kennwort
Gibt das Kennwort des SSL an, das von diesem Cmdlet erstellt wird.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate

## Notizen

## Verwandte Links

[Add-AzureRmApplicationGatewaySslCertificate](./Add-AzureRmApplicationGatewaySslCertificate.md)

[Get-AzureRmApplicationGatewaySslCertificate](./Get-AzureRmApplicationGatewaySslCertificate.md)

[Remove-AzureRmApplicationGatewaySslCertificate](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[Satz-AzureRmApplicationGatewaySslCertificate](./Set-AzureRmApplicationGatewaySslCertificate.md)


