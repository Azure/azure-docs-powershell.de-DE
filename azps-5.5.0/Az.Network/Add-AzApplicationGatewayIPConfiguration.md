---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157233"
---
# Add-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Fügt einem Anwendungsgateway eine IP-Konfiguration hinzu.

## SYNTAX

### SetByResourceId
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Add-AzApplicationGatewayIPConfiguration"** fügt einem Anwendungsgateway eine IP-Konfiguration hinzu.
IP-Konfigurationen enthalten das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

## BEISPIELE

### Beispiel 1: Hinzufügen einer virtuellen Netzwerkkonfiguration zu einem Anwendungsgateway
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk ab.
Der zweite Befehl ruft ein Subnetz mit dem zuvor erstellten virtuellen Netzwerk ab.
Der dritte Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.
Der vierte Befehl fügt die IP-Konfiguration dem Anwendungsgateway hinzu, das in $AppGw.

## PARAMETERS

### -ApplicationGateway
Gibt das Anwendungsgateway an, dem dieses Cmdlet eine IP-Konfiguration hinzufügt.

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

### -Name
Gibt den Namen der hinzuzufügenden IP-Konfiguration an.

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

### -Subnet
Gibt ein Subnetz an.
Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetId
Gibt eine Subnetz-ID an.
Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzApplicationGatewayIPConfiguration](./Get-AzApplicationGatewayIPConfiguration.md)

[New-AzApplicationGatewayIPConfiguration](./New-AzApplicationGatewayIPConfiguration.md)

[Remove-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


