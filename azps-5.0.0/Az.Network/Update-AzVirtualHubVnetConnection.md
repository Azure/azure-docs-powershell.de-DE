---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 0c07686b59f89bfee656701e14a7c938f49eeb86
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303053"
---
# <span data-ttu-id="faf33-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="faf33-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="faf33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faf33-102">SYNOPSIS</span></span>
<span data-ttu-id="faf33-103">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="faf33-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="faf33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faf33-104">SYNTAX</span></span>

### <span data-ttu-id="faf33-105">ByHubVirtualNetworkConnectionName (Standard)</span><span class="sxs-lookup"><span data-stu-id="faf33-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faf33-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="faf33-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faf33-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="faf33-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf33-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faf33-108">DESCRIPTION</span></span>
<span data-ttu-id="faf33-109">Aktualisiert eine vorhandene HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="faf33-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="faf33-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faf33-110">EXAMPLES</span></span>

### <span data-ttu-id="faf33-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faf33-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="faf33-112">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="faf33-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="faf33-113">Darüber hinaus wird eine virtuelle Netzwerkverbindung erstellt, die dem virtuellen Netzwerk Peer entspricht.</span><span class="sxs-lookup"><span data-stu-id="faf33-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="faf33-114">Diese virtuelle Netzwerkverbindung wird dann aktualisiert, um die Internetsicherheit zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="faf33-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="faf33-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="faf33-115">PARAMETERS</span></span>

### <span data-ttu-id="faf33-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="faf33-116">-AsJob</span></span>
<span data-ttu-id="faf33-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="faf33-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf33-118">-DefaultProfile</span></span>
<span data-ttu-id="faf33-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faf33-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="faf33-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="faf33-121">Aktivieren Sie die Internetsicherheit für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="faf33-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="faf33-122">-InputObject</span></span>
<span data-ttu-id="faf33-123">Die zu ändernde hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="faf33-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-124">-Name</span><span class="sxs-lookup"><span data-stu-id="faf33-124">-Name</span></span>
<span data-ttu-id="faf33-125">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="faf33-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="faf33-126">-ParentResourceName</span></span>
<span data-ttu-id="faf33-127">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="faf33-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf33-128">-ResourceGroupName</span></span>
<span data-ttu-id="faf33-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="faf33-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="faf33-130">-ResourceId</span></span>
<span data-ttu-id="faf33-131">Die Ressourcen-ID der zu ändernden hubvirtualnetworkconnection-Ressource.</span><span class="sxs-lookup"><span data-stu-id="faf33-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-132">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf33-132">-RoutingConfiguration</span></span>
<span data-ttu-id="faf33-133">Routing Konfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="faf33-133">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="faf33-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="faf33-134">-Confirm</span></span>
<span data-ttu-id="faf33-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="faf33-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf33-136">-WhatIf</span></span>
<span data-ttu-id="faf33-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="faf33-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faf33-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="faf33-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf33-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf33-139">CommonParameters</span></span>
<span data-ttu-id="faf33-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf33-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf33-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf33-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf33-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faf33-142">INPUTS</span></span>

### <span data-ttu-id="faf33-143">System. String</span><span class="sxs-lookup"><span data-stu-id="faf33-143">System.String</span></span>

### <span data-ttu-id="faf33-144">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="faf33-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="faf33-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faf33-145">OUTPUTS</span></span>

### <span data-ttu-id="faf33-146">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="faf33-146">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="faf33-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="faf33-147">NOTES</span></span>

## <span data-ttu-id="faf33-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faf33-148">RELATED LINKS</span></span>

[<span data-ttu-id="faf33-149">Neu – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf33-149">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
