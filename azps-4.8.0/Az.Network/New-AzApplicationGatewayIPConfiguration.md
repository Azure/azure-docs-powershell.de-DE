---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173232"
---
# New-AzApplicationGatewayIPConfiguration

## Synopsis
Erstellt eine IP-Konfiguration für ein Anwendungsgateway.

## Syntax

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

## Beschreibung
Das Cmdlet **New-AzApplicationGatewayIPConfiguration** erstellt eine IP-Konfiguration für ein Anwendungsgateway.
Die IP-Konfiguration enthält das Subnetz, in dem Application Gateway bereitgestellt wird.

## Beispiele

### Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

Der erste Befehl ruft ein virtuelles Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört.
Der zweite Befehl ruft die Subnetz-Konfiguration für das Subnetz ab, zu dem das virtuelle Netzwerk im vorherigen Befehl gehört, und speichert es in der $Subnet-Variablen.
Der dritte Befehl erstellt die IP-Konfiguration mithilfe von $Subnet.

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
Gibt den Namen der zu erstellende IP-Konfiguration an.

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

### -Subnetz
Gibt das Subnet-Objekt an.
Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

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

### -Subnet-Nr
Gibt die Subnet-ID an.
Hierbei handelt es sich um das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration

## Notizen

## Verwandte Links

[Add-AzApplicationGatewayIPConfiguration](./Add-AzApplicationGatewayIPConfiguration.md)

[Get-AzApplicationGatewayIPConfiguration](./Get-AzApplicationGatewayIPConfiguration.md)

[Remove-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Satz-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


