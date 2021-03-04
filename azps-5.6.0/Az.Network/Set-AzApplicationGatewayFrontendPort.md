---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920995"
---
# Set-AzApplicationGatewayFrontendPort

## SYNOPSIS
Ändert einen Front-End-Port für ein Anwendungsgateway.

## SYNTAX

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Set-AzApplicationGatewayFrontendPort** ändert einen Front-End-Port für ein Anwendungsgateway.

## BEISPIELE

### Beispiel 1: Festlegen eines Front-End-Ports für ein Anwendungsgateway auf 80
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variablen.
Der zweite Befehl ändert das Gateway in $AppGw, um Port 80 für den Front-End-Port namens FrontEndPort01 zu verwenden.

## PARAMETER

### -ApplicationGateway
Gibt das Anwendungsgatewayobjekt an, dem dieses Cmdlet den Front-End-Port zu ordnet.

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
Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Namen des zu ändernden Front-End-Ports an.

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
Gibt die Portnummer an, die für den Front-End-Port verwendet werden soll.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApplicationGatewayFrontendPort](./Add-AzApplicationGatewayFrontendPort.md)

[Get-AzApplicationGatewayFrontendPort](./Get-AzApplicationGatewayFrontendPort.md)

[New-AzApplicationGatewayFrontendPort](./New-AzApplicationGatewayFrontendPort.md)

[Remove-AzApplicationGatewayFrontendPort](./Remove-AzApplicationGatewayFrontendPort.md)
