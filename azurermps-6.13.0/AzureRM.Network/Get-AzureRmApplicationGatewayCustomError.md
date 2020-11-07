---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664550"
---
# Get-AzureRmApplicationGatewayCustomError

## Synopsis
Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmApplicationGatewayCustomError** " Ruft benutzerdefinierte Fehler (e) von einem Anwendungsgateway ab.

## Beispiele

### Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Anwendungsgateway ab
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

Dieser Befehl ruft den benutzerdefinierten Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw ab und gibt ihn zurück.

### Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Anwendungsgateway ab.
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGateway

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError

## Notizen

## Verwandte Links
