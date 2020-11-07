---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: a888ccb62af9437117f7039e29cc9c874f7bc5bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821800"
---
# <span data-ttu-id="4bff7-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bff7-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="4bff7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bff7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bff7-103">Ruft eine Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4bff7-103">Gets a network interface.</span></span>

## <span data-ttu-id="4bff7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bff7-104">SYNTAX</span></span>

### <span data-ttu-id="4bff7-105">NoExpandStandAloneNic (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bff7-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bff7-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="4bff7-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bff7-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="4bff7-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bff7-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="4bff7-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bff7-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bff7-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bff7-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bff7-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bff7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bff7-111">DESCRIPTION</span></span>
<span data-ttu-id="4bff7-112">Das Cmdlet " **Get-AzNetworkInterface** " Ruft eine Azure-Netzwerkschnittstelle oder eine Liste von Azure-Netzwerkschnittstellen in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4bff7-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="4bff7-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bff7-113">EXAMPLES</span></span>

### <span data-ttu-id="4bff7-114">Beispiel 1: Abrufen aller Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="4bff7-114">Example 1: Get all network interfaces</span></span>
```
PS C:\> Get-AzNetworkInterface

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="4bff7-115">Dieser Befehl ruft alle Netzwerkschnittstellen für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="4bff7-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="4bff7-116">Beispiel 2: Abrufen aller Netzwerkschnittstellen mit einem bestimmten Bereitstellungsstatus</span><span class="sxs-lookup"><span data-stu-id="4bff7-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="4bff7-117">Dieser Befehl ruft alle Netzwerkschnittstellen in der Ressourcengruppe mit dem Namen ResourceGroup1 ab, deren Bereitstellungsstatus "erfolgreich" lautet.</span><span class="sxs-lookup"><span data-stu-id="4bff7-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="4bff7-118">Beispiel 3: Abrufen von Netzwerkschnittstellen mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="4bff7-118">Example 3: Get network interfaces using filtering</span></span>
```
PS C:\> Get-AzNetworkInterface -Name test*

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="4bff7-119">Dieser Befehl ruft alle Netzwerkschnittstellen für das aktuelle Abonnement ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="4bff7-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="4bff7-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bff7-120">PARAMETERS</span></span>

### <span data-ttu-id="4bff7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bff7-121">-DefaultProfile</span></span>
<span data-ttu-id="4bff7-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bff7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bff7-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4bff7-123">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bff7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4bff7-124">-Name</span></span>
<span data-ttu-id="4bff7-125">Gibt den Namen der Netzwerkschnittstelle an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4bff7-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4bff7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bff7-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bff7-127">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bff7-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4bff7-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4bff7-128">-ResourceId</span></span>
<span data-ttu-id="4bff7-129">Die Azure Resource Manager-ID der Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4bff7-129">The Azure resource manager id of the network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bff7-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="4bff7-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="4bff7-131">Gibt den virtuellen Computer Index des Skalierungs Satzes für virtuelle Maschinen an, von dem dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bff7-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bff7-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bff7-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="4bff7-133">Gibt den Namen des Skalierungs Satzes für virtuelle Maschinen an, von dem dieses Cmdlet Netzwerkschnittstellen erhält.</span><span class="sxs-lookup"><span data-stu-id="4bff7-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bff7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bff7-134">CommonParameters</span></span>
<span data-ttu-id="4bff7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bff7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bff7-136">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bff7-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bff7-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bff7-137">INPUTS</span></span>

### <span data-ttu-id="4bff7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4bff7-138">System.String</span></span>

## <span data-ttu-id="4bff7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bff7-139">OUTPUTS</span></span>

### <span data-ttu-id="4bff7-140">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bff7-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4bff7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bff7-141">NOTES</span></span>

## <span data-ttu-id="4bff7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bff7-142">RELATED LINKS</span></span>

[<span data-ttu-id="4bff7-143">Neu – AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bff7-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="4bff7-144">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bff7-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="4bff7-145">Satz-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bff7-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


