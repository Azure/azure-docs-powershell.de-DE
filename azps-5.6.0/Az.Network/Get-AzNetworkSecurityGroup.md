---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: ad97cb949550778ff40ce1d18f67caca20d7d5af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945959"
---
# Get-AzNetworkSecurityGroup

## SYNOPSIS
Ruft eine Netzwerksicherheitsgruppe ab.

## SYNTAX

### NoExpand
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Erweitern
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzNetworkSecurityGroup-Cmdlet** ruft eine Azure-Netzwerksicherheitsgruppe ab.

## BEISPIELE

### Beispiel 1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe
```powershell
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

Dieser Befehl gibt den Inhalt der Azure-Netzwerksicherheitsgruppe "nsg1" in der Ressourcengruppe "rg1" zurück.

### Beispiel 2: Auflisten vorhandener Netzwerksicherheitsgruppen mithilfe von Filterung
```powershell
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkSecurityGroups/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
SecurityRules               : []
DefaultSecurityRules        : [
                                {
                                  "Name": "AllowVnetInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetInBound",
                                  "Description": "Allow inbound traffic from all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowAzureLoadBalancerInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowAzureLoadBalancerInBou
                              nd",
                                  "Description": "Allow inbound traffic from azure load balancer",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "AzureLoadBalancer"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllInBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllInBound",
                                  "Description": "Deny all inbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Inbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowVnetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowVnetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to all VMs in VNET",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "VirtualNetwork"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65000,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "AllowInternetOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/AllowInternetOutBound",
                                  "Description": "Allow outbound traffic from all VMs to Internet",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "Internet"
                                  ],
                                  "Access": "Allow",
                                  "Priority": 65001,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                },
                                {
                                  "Name": "DenyAllOutBound",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provide
                              rs/Microsoft.Network/networkSecurityGroups/nsg1/defaultSecurityRules/DenyAllOutBound",
                                  "Description": "Deny all outbound traffic",
                                  "Protocol": "*",
                                  "SourcePortRange": [
                                    "*"
                                  ],
                                  "DestinationPortRange": [
                                    "*"
                                  ],
                                  "SourceAddressPrefix": [
                                    "*"
                                  ],
                                  "DestinationAddressPrefix": [
                                    "*"
                                  ],
                                  "Access": "Deny",
                                  "Priority": 65500,
                                  "Direction": "Outbound",
                                  "ProvisioningState": "Succeeded",
                                  "SourceApplicationSecurityGroups": [],
                                  "DestinationApplicationSecurityGroups": []
                                }
                              ]
NetworkInterfaces           : []
Subnets                     : []
```

Dieser Befehl gibt Inhalte von Azure-Netzwerksicherheitsgruppen zurück, die mit "nsg" beginnen.

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

### -ExpandResource
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
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

### Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup

## NOTIZEN

## VERWANDTE LINKS

[New-AzNetworkSecurityGroup](./New-AzNetworkSecurityGroup.md)

[Remove-AzNetworkSecurityGroup](./Remove-AzNetworkSecurityGroup.md)

[Set-AzNetworkSecurityGroup](./Set-AzNetworkSecurityGroup.md)


