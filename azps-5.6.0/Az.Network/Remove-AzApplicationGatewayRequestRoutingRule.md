---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938579"
---
# Remove-AzApplicationGatewayRequestRoutingRule

## SYNOPSIS
Entfernt eine Anforderungsroutingregel aus einem Anwendungsgateway.

## SYNTAX

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Remove-AzApplicationGatewayRequestRoutingRule** entfernt eine Anforderungsroutingregel aus einem Azure-Anwendungsgateway.

## BEISPIELE

### Beispiel 1: Entfernen einer Anforderungsroutingregel aus einem Anwendungsgateway
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variablen.
Mit dem zweiten Befehl wird die Anforderungsroutingregel mit dem Namen Regel02 aus dem anwendungsgateway entfernt, das in $AppGw.

## PARAMETER

### -ApplicationGateway
Gibt das Anwendungsgateway an, aus dem eine Anforderungsroutingregel entfernt werden soll.

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
Gibt den Namen der Anforderungsroutingregel an, für die dieses Cmdlet entfernt wird.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule

## NOTIZEN

## VERWANDTE LINKS

[Add-AzApplicationGatewayRequestRoutingRule](./Add-AzApplicationGatewayRequestRoutingRule.md)

[Get-AzApplicationGatewayRequestRoutingRule](./Get-AzApplicationGatewayRequestRoutingRule.md)

[New-AzApplicationGatewayRequestRoutingRule](./New-AzApplicationGatewayRequestRoutingRule.md)

[Set-AzApplicationGatewayRequestRoutingRule](./Set-AzApplicationGatewayRequestRoutingRule.md)


