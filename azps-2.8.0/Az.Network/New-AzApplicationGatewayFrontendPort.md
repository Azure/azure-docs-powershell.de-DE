---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822187"
---
# New-AzApplicationGatewayFrontendPort

## Synopsis
Erstellt einen Front-End-Port für ein Anwendungsgateway.

## Syntax

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzApplicationGatewayFrontendPort** erstellt einen Front-End-Port für ein Azure Application Gateway.

## Beispiele

### Beispiel1: Erstellen eines Front-End-Ports
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

Dieser Befehl erstellt einen Front-End-Port mit dem Namen FrontEndPort01 auf Port 80 und speichert das Ergebnis in der Variablen mit dem Namen $FrontEndPort.

## Parameter

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

### -Name
Gibt den Namen des Front-End-Ports an, der vom Cmdlet erstellt wird.

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

### -Port
Gibt die Portnummer des Front-End-Ports an.

```yaml
Type: System.Int32
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayFrontendPort](./Add-AzApplicationGatewayFrontendPort.md)

[Get-AzApplicationGatewayFrontendPort](./Get-AzApplicationGatewayFrontendPort.md)

[Remove-AzApplicationGatewayFrontendPort](./Remove-AzApplicationGatewayFrontendPort.md)

[Satz-AzApplicationGatewayFrontendPort](./Set-AzApplicationGatewayFrontendPort.md)


