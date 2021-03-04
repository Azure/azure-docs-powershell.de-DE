---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzP2sVpnGateway.md
ms.openlocfilehash: 33a22ce2089dd1111fcafce20208a1b948ce1253
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918427"
---
# <span data-ttu-id="82969-101">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="82969-101">Update-AzP2sVpnGateway</span></span>

## <span data-ttu-id="82969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82969-102">SYNOPSIS</span></span>
<span data-ttu-id="82969-103">Aktualisieren Sie ein vorhandenes P2SVpnGateway unter VirtualHub, um auf die Websitekonnektivität zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="82969-103">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="82969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82969-104">SYNTAX</span></span>

### <span data-ttu-id="82969-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Standard)</span><span class="sxs-lookup"><span data-stu-id="82969-105">ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate (Default)</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>] [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="82969-106">ByP2SVpnGatewayNameByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="82969-107">ByP2SVpnGatewayNameByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82969-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="82969-108">ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="82969-109">ByP2SVpnGatewayObjectByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>]
 [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="82969-110">ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-VpnClientAddressPool <String[]>]
 -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span><span class="sxs-lookup"><span data-stu-id="82969-111">ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="82969-112">ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] [-VpnServerConfiguration <PSVpnServerConfiguration>] [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82969-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="82969-113">ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId</span></span>
```
Update-AzP2sVpnGateway -ResourceId <String> [-VpnClientAddressPool <String[]>] -VpnServerConfigurationId <String> [-VpnGatewayScaleUnit <UInt32>] [-CustomDnsServer <String[]>]  [-EnableInternetSecurityFlag] [-DisableInternetSecurityFlag] [-RoutingConfiguration <PSRoutingConfiguration>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82969-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82969-114">DESCRIPTION</span></span>
<span data-ttu-id="82969-115">Mit dem **Update-AzP2sVpnGateway-Cmdlet** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub mit dem neuen VpnClientAddressPool oder der neuen VpnServerConfiguration oder Änderung von VpnGatewayScaleUnit aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="82969-115">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool or new VpnServerConfiguration or change of VpnGatewayScaleUnit.</span></span>

## <span data-ttu-id="82969-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82969-116">EXAMPLES</span></span>

### <span data-ttu-id="82969-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82969-117">Example 1</span></span>
```powershell
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1 
PS C:\> $vpnClientAddressSpaces[0] = "101.10.0.0/16"
PS C:\> Update-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VpnClientAddressPool $vpnClientAddressSpaces -EnableInternetSecurityFlag                                

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/NilamdWestUsVirtualH
                                 ub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/NilamdWe
                                 stUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : null
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "101.10.0.0/16"
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
                                     "Etag": "W/\"d7debc2f-ccbb-4f00-bddc-42c99b52fda3\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="82969-118">Mit **dem Update-AzP2sVpnGateway-Cmdlet** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub mit dem neuen VpnClientAddressPool aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="82969-118">The **Update-AzP2sVpnGateway** cmdlet enables you to update an existing P2SVpnGateway under VirtualHub with new VpnClientAddressPool.</span></span> <span data-ttu-id="82969-119">Wenn der Point to-Websiteclient eine Verbindung mit diesem P2SVpnGateway herstellt, wird dem Client eine der IP-Adressen aus diesem VpnClientAddressPool zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="82969-119">When Point to site client connects with this P2SVpnGateway, one of the ip address from this VpnClientAddressPool gets allocated to that client.</span></span>

### <span data-ttu-id="82969-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="82969-120">Example 2</span></span>

<span data-ttu-id="82969-121">Aktualisieren Sie ein vorhandenes P2SVpnGateway unter VirtualHub, um auf die Websitekonnektivität zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="82969-121">Update an existing P2SVpnGateway under VirtualHub for point to site connectivity.</span></span> <span data-ttu-id="82969-122">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="82969-122">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzP2sVpnGateway -AsJob -Name 00000000-0000-0000-0000-00000000000000000-westus-gw -ResourceGroupName P2SCortexGATesting -VpnClientAddressPool <String[]> -VpnGatewayScaleUnit 1 -VpnServerConfiguration <PSVpnServerConfiguration>
```

## <span data-ttu-id="82969-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82969-123">PARAMETERS</span></span>

### <span data-ttu-id="82969-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82969-124">-AsJob</span></span>
<span data-ttu-id="82969-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82969-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82969-126">-CustomDnsServer</span><span class="sxs-lookup"><span data-stu-id="82969-126">-CustomDnsServer</span></span>
<span data-ttu-id="82969-127">Die Liste der benutzerdefinierten Dns-Server.</span><span class="sxs-lookup"><span data-stu-id="82969-127">The list of Custom Dns Servers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82969-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82969-128">-DefaultProfile</span></span>
<span data-ttu-id="82969-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82969-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82969-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82969-130">-InputObject</span></span>
<span data-ttu-id="82969-131">Das zu ändernde p2s-Vpn-Gatewayobjekt</span><span class="sxs-lookup"><span data-stu-id="82969-131">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObjectNoVpnServerConfigurationUpdate, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82969-132">-Name</span><span class="sxs-lookup"><span data-stu-id="82969-132">-Name</span></span>
<span data-ttu-id="82969-133">Der Name des P2S-Vpngateways.</span><span class="sxs-lookup"><span data-stu-id="82969-133">The P2S vpn gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases: ResourceName, P2SVpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82969-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82969-134">-ResourceGroupName</span></span>
<span data-ttu-id="82969-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="82969-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameNoVpnServerConfigurationUpdate, ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82969-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82969-136">-ResourceId</span></span>
<span data-ttu-id="82969-137">Die Azure-Ressourcen-ID des zu ändernden P2SVpnGateways.</span><span class="sxs-lookup"><span data-stu-id="82969-137">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayResourceIdNoVpnServerConfigurationUpdate, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82969-138">-EnableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="82969-138">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="82969-139">Aktivieren der Internetsicherheitsflagge für diese P2SVpnGateway-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="82969-139">Enable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="82969-140">-DisableInternetSecurityFlag</span><span class="sxs-lookup"><span data-stu-id="82969-140">-DisableInternetSecurityFlag</span></span>
<span data-ttu-id="82969-141">Deaktivieren des Internetsicherheitszeichens für diese P2SVpnGateway-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="82969-141">Disable internet security flag for this P2SVpnGateway connections</span></span>

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

### <span data-ttu-id="82969-142">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="82969-142">-RoutingConfiguration</span></span>
<span data-ttu-id="82969-143">Routingkonfiguration für diese Verbindung</span><span class="sxs-lookup"><span data-stu-id="82969-143">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="82969-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="82969-144">-Tag</span></span>
<span data-ttu-id="82969-145">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="82969-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82969-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="82969-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="82969-147">P2S VpnClient AddressPool für dieses P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82969-147">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82969-148">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="82969-148">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="82969-149">Die Skalierungseinheit für dieses P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="82969-149">The scale unit for this P2SVpnGateway.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82969-150">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="82969-150">-VpnServerConfiguration</span></span>
<span data-ttu-id="82969-151">Die VpnServerConfiguration, die an dieses P2SVpnGateway angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="82969-151">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationObject, ByP2SVpnGatewayObjectByVpnServerConfigurationObject, ByP2SVpnGatewayResourceIdByVpnServerConfigurationObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82969-152">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="82969-152">-VpnServerConfigurationId</span></span>
<span data-ttu-id="82969-153">Die ID des Vpn Server-Konfigurationsobjekts, an das dieses P2SVpnGateway angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="82969-153">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByP2SVpnGatewayNameByVpnServerConfigurationResourceId, ByP2SVpnGatewayObjectByVpnServerConfigurationResourceId, ByP2SVpnGatewayResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82969-154">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82969-154">-Confirm</span></span>
<span data-ttu-id="82969-155">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82969-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82969-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82969-156">-WhatIf</span></span>
<span data-ttu-id="82969-157">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82969-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82969-158">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82969-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82969-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82969-159">CommonParameters</span></span>
<span data-ttu-id="82969-160">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82969-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82969-161">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82969-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82969-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82969-162">INPUTS</span></span>

### <span data-ttu-id="82969-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="82969-163">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="82969-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="82969-164">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="82969-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82969-165">OUTPUTS</span></span>

### <span data-ttu-id="82969-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="82969-166">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="82969-167">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82969-167">NOTES</span></span>

## <span data-ttu-id="82969-168">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82969-168">RELATED LINKS</span></span>

[<span data-ttu-id="82969-169">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="82969-169">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
