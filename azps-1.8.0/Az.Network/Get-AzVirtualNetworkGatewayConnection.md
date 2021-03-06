---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 9ce01263acde5b30533a23d55a8e7cedaba6b53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660685"
---
# Get-AzVirtualNetworkGatewayConnection

## Synopsis
Ruft eine Verbindung mit einem virtuellen Netzwerk Gateway ab

## Syntax

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Die VPN-Gatewayverbindung ist das Objekt, das den IPSec-Tunnel (Site-to-Site oder vnet-to-vnet) darstellt, der mit dem virtuellen Netzwerkgateway in Azure verbunden ist.
Das Cmdlet " **Get-AzVirtualNetworkGatewayConnection** " gibt das Objekt Ihrer Verbindung basierend auf Name und Ressourcengruppennamen zurück.
Wenn das Cmdlet **Get-AzVirtualNetworkGatewayConnection** ohne Angabe des-Name-Parameters ausgegeben wird, werden in der Ausgabe keine Details zu ConnectionStatus und SharedKey angezeigt.

## Beispiele

### 1: Abrufen einer virtuellen Netzwerk Gateway-Verbindung
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

Gibt das Objekt der virtuellen Netzwerk Gateway-Verbindung mit dem Namen "mytunnel" innerhalb der Ressourcengruppe "myRG" zurück.

### 2: Abrufen aller virtuellen Netzwerk-Gateway-Verbindungen mithilfe von Filtern
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

Gibt alle virtuellen Netzwerk-Gateway-Verbindungen zurück, die mit "mytunnel" in der Ressourcengruppe "myRG" beginnen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection

## Notizen

## Verwandte Links

[Neu – AzVirtualNetworkGatewayConnection](./New-AzVirtualNetworkGatewayConnection.md)

[Remove-AzVirtualNetworkGatewayConnection](./Remove-AzVirtualNetworkGatewayConnection.md)

[Satz-AzVirtualNetworkGatewayConnection](./Set-AzVirtualNetworkGatewayConnection.md)
