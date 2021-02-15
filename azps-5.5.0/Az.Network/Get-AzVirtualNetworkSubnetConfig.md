---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151860"
---
# Get-AzVirtualNetworkSubnetConfig

## SYNOPSIS
Ruft ein Subnetz in einem virtuellen Netzwerk ab.

## SYNTAX

### GetByVirtualNetwork (Standard)
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzVirtualNetworkSubnetConfig"** ruft eine oder mehrere Subnetzkonfigurationen in einem virtuellen Azure-Netzwerk ab.

## BEISPIELE

### 1: Erhalten eines Subnetzes in einem virtuellen Netzwerk
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

In diesem Beispiel werden eine Ressourcengruppe und ein virtuelles Netzwerk mit einem einzelnen Subnetz in dieser Ressourcengruppe erstellt. Anschließend werden Daten zu diesem Subnetz abgerufen.

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
Gibt den Namen der Subnetzkonfiguration an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Gibt die Ressourcen-ID des Subnetzes an, das dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Gibt das **VirtualNetwork-Objekt** an, das die Subnetzkonfiguration enthält, die dieses Cmdlet erhält.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSSubnet

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzVirtualNetworkSubnetConfig](./Add-AzVirtualNetworkSubnetConfig.md)

[New-AzVirtualNetworkSubnetConfig](./New-AzVirtualNetworkSubnetConfig.md)

[Remove-AzVirtualNetworkSubnetConfig](./Remove-AzVirtualNetworkSubnetConfig.md)

[Set-AzVirtualNetworkSubnetConfig](./Set-AzVirtualNetworkSubnetConfig.md)
