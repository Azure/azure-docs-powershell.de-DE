---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822316"
---
# <span data-ttu-id="f2f5d-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2f5d-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="f2f5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f5d-103">Ruft eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-103">Gets a network security group.</span></span>

## <span data-ttu-id="f2f5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2f5d-104">SYNTAX</span></span>

### <span data-ttu-id="f2f5d-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="f2f5d-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f5d-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="f2f5d-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f5d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f5d-108">Das Cmdlet " **Get-AzNetworkSecurityGroup** " Ruft eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="f2f5d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="f2f5d-110">1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="f2f5d-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="f2f5d-111">Dieser Befehl gibt den Inhalt der Azure Network Security-Gruppe "nsg1" in der Ressourcengruppe "RG1" zurück.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="f2f5d-112">2: Auflisten vorhandener Netzwerk Sicherheitsgruppen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="f2f5d-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="f2f5d-113">Dieser Befehl gibt Inhalte von Azure Network Security-Gruppen zurück, die mit "NSG" beginnen.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="f2f5d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="f2f5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f5d-115">-DefaultProfile</span></span>
<span data-ttu-id="f2f5d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2f5d-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f2f5d-117">-ExpandResource</span></span>
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

### <span data-ttu-id="f2f5d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f2f5d-118">-Name</span></span>
<span data-ttu-id="f2f5d-119">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2f5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2f5d-121">Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

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

### <span data-ttu-id="f2f5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f5d-122">CommonParameters</span></span>
<span data-ttu-id="f2f5d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f5d-124">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2f5d-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f5d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2f5d-125">INPUTS</span></span>

### <span data-ttu-id="f2f5d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f2f5d-126">System.String</span></span>

## <span data-ttu-id="f2f5d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2f5d-127">OUTPUTS</span></span>

### <span data-ttu-id="f2f5d-128">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2f5d-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f2f5d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2f5d-129">NOTES</span></span>

## <span data-ttu-id="f2f5d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2f5d-130">RELATED LINKS</span></span>

[<span data-ttu-id="f2f5d-131">Neu – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2f5d-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f2f5d-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2f5d-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="f2f5d-133">Satz-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2f5d-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


