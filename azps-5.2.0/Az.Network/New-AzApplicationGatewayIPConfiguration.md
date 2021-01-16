---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305699"
---
# New-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Erstellt eine IP-Konfiguration für ein Anwendungsgateway.

## SYNTAX

### SetByResourceId
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzApplicationGatewayIPConfiguration"** erstellt eine IP-Konfiguration für ein Anwendungsgateway.
Die IP-Konfiguration enthält das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

## BEISPIELE

### Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway.
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört.
Der zweite Befehl ruft die Subnetzkonfiguration für das Subnetz ab, dem das virtuelle Netzwerk im vorherigen Befehl angehört, und speichert es in $Subnet Variable.
Der dritte Befehl erstellt die IP-Konfiguration mithilfe $Subnet.

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
Gibt den Namen der zu erstellenden IP-Konfiguration an.

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
Gibt das Subnetzobjekt an.
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
Gibt die Subnetz-ID an.
Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt würde.

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

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Add-AzApplicationGatewayIPConfiguration](./Add-AzApplicationGatewayIPConfiguration.md)

[Get-AzApplicationGatewayIPConfiguration](./Get-AzApplicationGatewayIPConfiguration.md)

[Remove-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


