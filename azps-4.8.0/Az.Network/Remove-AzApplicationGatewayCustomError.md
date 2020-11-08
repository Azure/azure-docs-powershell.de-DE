---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009660"
---
# Remove-AzApplicationGatewayCustomError

## Synopsis
Entfernt einen benutzerdefinierten Fehler aus einem Anwendungsgateway.

## Syntax

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Remove-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler aus einem Anwendungsgateway entfernt.

## Beispiele

### Beispiel 1: Entfernen von benutzerdefiniertem Fehler aus einem Anwendungsgateway
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw entfernt, und das aktualisierte Gateway wird zurückgegeben.

## Parameter

### -ApplicationGateway
Das Anwendungs Gateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Statuscode
Status Code des Kunden Fehlers des Application Gateway-Kunden.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayCustomError](./Add-AzApplicationGatewayCustomError.md)

[Get-AzApplicationGatewayCustomError](./Get-AzApplicationGatewayCustomError.md)

[Neu – AzApplicationGatewayCustomError](./New-AzApplicationGatewayCustomError.md)

[Satz-AzApplicationGatewayCustomError](./Set-AzApplicationGatewayCustomError.md)
