---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178553"
---
# Get-AzApplicationGatewayCustomError

## Synopsis
Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.

## Syntax

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzApplicationGatewayCustomError** " Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.

## Beispiele

### Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Anwendungsgateway ab
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

Dieser Befehl ruft den benutzerdefinierten Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw ab und gibt ihn zurück.

### Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Anwendungsgateway ab.
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem Application Gateway $appgw ab und gibt diese zurück.

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayCustomError](./Add-AzApplicationGatewayCustomError.md)

[Neu – AzApplicationGatewayCustomError](./New-AzApplicationGatewayCustomError.md)

[Remove-AzApplicationGatewayCustomError](./Remove-AzApplicationGatewayCustomError.md)

[Satz-AzApplicationGatewayCustomError](./Set-AzApplicationGatewayCustomError.md)
