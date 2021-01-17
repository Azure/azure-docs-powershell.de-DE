---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472572"
---
# Get-AzVirtualNetworkGatewayConnection

## SYNOPSIS
Ruft eine Virtuelle Netzwerkgatewayverbindung ab

## SYNTAX

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Die Virtuelle Netzwerkgatewayverbindung ist das Objekt, das den mit dem virtuellen Netzwerkgateway in Azure verbundenen IPsec-Tunnel (Site-to-Site oder Vnet-zu-Vnet) darstellt.
Das **Cmdlet "Get-AzVirtualNetworkGatewayConnection"** gibt das Objekt Ihrer Verbindung basierend auf "Name" und "Ressourcengruppenname" zurück.
Wenn das **Cmdlet "Get-AzVirtualNetworkGatewayConnection"** ohne Angabe des Parameters "-Name" ausgegeben wird, werden in der Ausgabe keine ConnectionStatus- und SharedKey-Details angezeigt.

## BEISPIELE

### 1: Herstellen einer Virtuellen Netzwerkgatewayverbindung
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

Gibt das Objekt der Virtuellen Netzwerkgatewayverbindung mit dem Namen "myKg" innerhalb der Ressourcengruppe "myRG" zurück.

### 2: Erhalten aller Verbindungen des virtuellen Netzwerkgateways mithilfe der Filterung
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

Gibt alle Virtuellen Netzwerkgatewayverbindungen zurück, die mit "my Ganz" in der Ressourcengruppe "myRG" beginnen.

## PARAMETERS

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[Remove-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Set-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
