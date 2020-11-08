---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e9156887f328242f8c4896dc707a1814f58f2869
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174567"
---
# <span data-ttu-id="589d9-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="589d9-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="589d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="589d9-102">SYNOPSIS</span></span>
<span data-ttu-id="589d9-103">Mit dem New-AzVirtualHubVnetConnection-Cmdlet wird eine HubVirtualNetworkConnection-Ressource erstellt, die einem virtuellen Netzwerk mit dem Azure Virtual-Hub Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="589d9-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="589d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="589d9-104">SYNTAX</span></span>

### <span data-ttu-id="589d9-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="589d9-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589d9-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="589d9-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589d9-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="589d9-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589d9-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="589d9-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="589d9-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="589d9-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="589d9-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="589d9-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="589d9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="589d9-111">DESCRIPTION</span></span>
<span data-ttu-id="589d9-112">Mit dem New-AzVirtualHubVnetConnection-Cmdlet wird eine HubVirtualNetworkConnection-Ressource erstellt, die einem virtuellen Netzwerk mit dem Azure Virtual-Hub Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="589d9-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="589d9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="589d9-113">EXAMPLES</span></span>

### <span data-ttu-id="589d9-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="589d9-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
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

<span data-ttu-id="589d9-115">In der obigen Abbildung wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub in Zentralamerika, in dieser Ressourcengruppe in Azure erstellt.</span><span class="sxs-lookup"><span data-stu-id="589d9-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="589d9-116">Anschließend wird eine virtuelle Netzwerkverbindung erstellt, die das virtuelle Netzwerk mit dem virtuellen Hub unter seinesgleichen führt.</span><span class="sxs-lookup"><span data-stu-id="589d9-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="589d9-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="589d9-117">Example 2</span></span>

<span data-ttu-id="589d9-118">Mit dem New-AzVirtualHubVnetConnection-Cmdlet wird eine HubVirtualNetworkConnection-Ressource erstellt, die einem virtuellen Netzwerk mit dem Azure Virtual-Hub Peers entspricht.</span><span class="sxs-lookup"><span data-stu-id="589d9-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="589d9-119">automatisch</span><span class="sxs-lookup"><span data-stu-id="589d9-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```

## <span data-ttu-id="589d9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="589d9-120">PARAMETERS</span></span>

### <span data-ttu-id="589d9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="589d9-121">-AsJob</span></span>
<span data-ttu-id="589d9-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="589d9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="589d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="589d9-123">-DefaultProfile</span></span>
<span data-ttu-id="589d9-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="589d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="589d9-125">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="589d9-125">-EnableInternetSecurity</span></span>
<span data-ttu-id="589d9-126">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="589d9-126">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="589d9-127">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="589d9-127">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="589d9-128">Aktivieren der Internetsicherheit für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="589d9-128">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="589d9-129">-Name</span><span class="sxs-lookup"><span data-stu-id="589d9-129">-Name</span></span>
<span data-ttu-id="589d9-130">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="589d9-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="589d9-131">-ParentObject</span></span>
<span data-ttu-id="589d9-132">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="589d9-132">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="589d9-133">-ParentResourceId</span></span>
<span data-ttu-id="589d9-134">Die übergeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="589d9-134">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-135">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="589d9-135">-ParentResourceName</span></span>
<span data-ttu-id="589d9-136">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="589d9-136">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-137">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="589d9-137">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="589d9-138">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Hub-Netzwerkverbindung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="589d9-138">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-139">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="589d9-139">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="589d9-140">Das virtuelle Remotenetzwerk, mit dem diese virtuelle Hub-Netzwerkverbindung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="589d9-140">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="589d9-141">-ResourceGroupName</span></span>
<span data-ttu-id="589d9-142">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="589d9-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-143">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="589d9-143">-RoutingConfiguration</span></span>
<span data-ttu-id="589d9-144">Routing Konfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="589d9-144">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="589d9-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="589d9-145">-Confirm</span></span>
<span data-ttu-id="589d9-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="589d9-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="589d9-147">-WhatIf</span></span>
<span data-ttu-id="589d9-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="589d9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="589d9-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="589d9-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="589d9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="589d9-150">CommonParameters</span></span>
<span data-ttu-id="589d9-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="589d9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="589d9-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="589d9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="589d9-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="589d9-153">INPUTS</span></span>

### <span data-ttu-id="589d9-154">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="589d9-154">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="589d9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="589d9-155">System.String</span></span>

## <span data-ttu-id="589d9-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="589d9-156">OUTPUTS</span></span>

### <span data-ttu-id="589d9-157">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="589d9-157">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="589d9-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="589d9-158">NOTES</span></span>

## <span data-ttu-id="589d9-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="589d9-159">RELATED LINKS</span></span>

[<span data-ttu-id="589d9-160">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="589d9-160">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="589d9-161">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="589d9-161">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="589d9-162">Neu – AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="589d9-162">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
