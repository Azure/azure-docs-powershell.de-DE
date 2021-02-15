---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 401fa91682e68b74e950d5010b22ce140436b06a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151657"
---
# New-AzP2sVpnGateway

## SYNOPSIS
Erstellen Sie ein neues P2SVpnGateway unter VirtualHub, um auf die Websitekonnektivität zu verweisen.

## SYNTAX

### ByVirtualHubNameByVpnServerConfigurationObject (Standard)
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubNameByVpnServerConfigurationResourceId
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubObjectByVpnServerConfigurationObject
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-CustomDnsServer <String[]>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubObjectByVpnServerConfigurationResourceId
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubResourceIdByVpnServerConfigurationObject
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubResourceIdByVpnServerConfigurationResourceId
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-CustomDnsServer <String[]>] [-RoutingConfiguration <PSRoutingConfiguration>] [-EnableInternetSecurityFlag]
 [-EnableRoutingPreferenceInternetFlag] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Mit New-AzP2sVpnGateway A0 können Sie ein neues P2SVpnGateway unter VirtualHub für die Point-to-Site-Konnektivität von Point-to-Site-Clients zu Azure VirtualWan erstellen.

## BEISPIELE

### Beispiel 1
```
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1 -EnableInternetSecurityFlag -EnableRoutingPreferenceInternetFlag

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "EnableInternetSecurity": True,
                                     "RoutingConfiguration": {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                       }
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                            "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub/hubRouteTables/defaultRouteTable"
                                           }
                                        ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

Mit New-AzP2sVpnGateway A0 können Sie unter VirtualHub ein neues P2SVpnGateway für die Point-to-Site-Konnektivität erstellen.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDnsServer
Die Liste der benutzerdefinierten Dns-Server.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Ressourcenname.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Der Ressourcenname.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableInternetSecurityFlag
Aktivieren des Internetsicherheitsflags für diese P2SVpnGateway-Verbindungen

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoutingConfiguration
Routingkonfiguration für diese Verbindung

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Eine Hashtable, die Ressourcentags darstellt.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualHub
Der VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualHubId
Die ID des VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualHubName
Die ID des VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VpnClientAddressPool
P2S VpnClient AddressPool für dieses P2SVpnGateway P2SConnectionConfiguration.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VpnGatewayScaleUnit
Die Skalierungseinheit für dieses P2SVpnGateway.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VpnServerConfiguration
Die an dieses P2SVpnGateway angefügte VpnServerConfiguration.

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationObject, ByVirtualHubObjectByVpnServerConfigurationObject, ByVirtualHubResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnServerConfigurationId
Die ID des Vpn-Server-Konfigurationsobjekts, an das dieses P2SVpnGateway angefügt wird.

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByVpnServerConfigurationResourceId, ByVirtualHubObjectByVpnServerConfigurationResourceId, ByVirtualHubResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableRoutingPreferenceInternetFlag
Zum Aktivieren der Routingeinstellung Internet in diesem P2SVpnGateway kennzeichnen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Network.Models.PSVirtualHub
System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzRoutingConfiguration]()

