---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944044"
---
# Get-AzApplicationGatewayHttpListenerCustomError

## SYNOPSIS
Ruft benutzerdefinierte Fehler von einem http-Listener eines Anwendungsgateways ab.

## SYNTAX

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzApplicationGatewayCustomError-Cmdlet** ruft benutzerdefinierte Fehler von einem http-Listener eines Anwendungsgateways ab.

## BEISPIELE

### Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Http-Listener ab.
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

Dieser Befehl ruft den benutzerdefinierten Fehler von http-Statuscode 502 aus dem http-Listener-$listener 01 ab und gibt diesen zurück.

### Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Http-Listener ab.
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem http-Listener-$listener 01 ab und gibt sie zurück.

## PARAMETER

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -HttpListener
Der Http-Listener für das Anwendungsgateway

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
Statuscode des Kundenfehlers des Anwendungsgateways.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApplicationGatewayHttpListenerCustomError](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[Remove-AzApplicationGatewayHttpListenerCustomError](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[Set-AzApplicationGatewayHttpListenerCustomError](./Set-AzApplicationGatewayHttpListenerCustomError.md)
