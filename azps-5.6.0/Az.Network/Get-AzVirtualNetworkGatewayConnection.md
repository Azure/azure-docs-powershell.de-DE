---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: e4b972944f757c9b0072f091dc820de5fa5d5b1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924744"
---
# Get-AzVirtualNetworkGatewayConnection

## SYNOPSIS
Ruft eine Verbindung mit einem virtuellen Netzwerkgateway ab

## SYNTAX

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Die Virtual Network Gateway Connection ist das Objekt, das den IPsec-Tunnel (Site-to-Site oder Vnet-to-Vnet) darstellt, der mit Ihrem Virtuellen Netzwerkgateway in Azure verbunden ist.
Das **Get-AzVirtualNetworkGatewayConnection-Cmdlet** gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppenname zurück.
Wenn das **Get-AzVirtualNetworkGatewayConnection-Cmdlet** ohne Angabe des -Name-Parameters ausgegeben wird, werden in der Ausgabe keine Details zu ConnectionStatus und SharedKey angezeigt.

## BEISPIELE

### 1: Herstellen einer Virtuellen Netzwerkgatewayverbindung
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

Gibt das Objekt der Virtual Network Gateway Connection mit dem Namen "myTunnel" innerhalb der Ressourcengruppe "myRG" zurück.

### 2: Alle Verbindungen des virtuellen Netzwerkgateways mithilfe der Filterung
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

Gibt alle Virtuellen Netzwerkgatewayverbindungen zurück, die mit "myTunnel" innerhalb der Ressourcengruppe "myRG" beginnen.

## PARAMETER

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
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection

## NOTIZEN

## VERWANDTE LINKS

[New-AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[Remove-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Set-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
