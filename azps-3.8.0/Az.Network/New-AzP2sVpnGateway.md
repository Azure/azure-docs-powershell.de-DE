---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzP2sVpnGateway.md
ms.openlocfilehash: 6d16703b7f0492bb2c37291e135cb1b9c836a572
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996476"
---
# <span data-ttu-id="f0dc0-101">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f0dc0-101">New-AzP2sVpnGateway</span></span>

## <span data-ttu-id="f0dc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="f0dc0-103">Erstellen Sie unter VirtualHub eine neue P2SVpnGateway für Punkt-zu-Standort-Konnektivität.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-103">Create a new P2SVpnGateway under VirtualHub for point to site connectivity.</span></span>

## <span data-ttu-id="f0dc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0dc0-104">SYNTAX</span></span>

### <span data-ttu-id="f0dc0-105">ByVirtualHubNameByVpnServerConfigurationObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0dc0-105">ByVirtualHubNameByVpnServerConfigurationObject (Default)</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0dc0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f0dc0-106">ByVirtualHubNameByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubName <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0dc0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="f0dc0-107">ByVirtualHubObjectByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> [-VpnServerConfiguration <PSVpnServerConfiguration>]
 -VpnClientAddressPool <String[]> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0dc0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f0dc0-108">ByVirtualHubObjectByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHub <PSVirtualHub> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0dc0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="f0dc0-109">ByVirtualHubResourceIdByVpnServerConfigurationObject</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> [-VpnServerConfiguration <PSVpnServerConfiguration>] -VpnClientAddressPool <String[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0dc0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f0dc0-110">ByVirtualHubResourceIdByVpnServerConfigurationResourceId</span></span>
```
New-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> -VpnGatewayScaleUnit <UInt32>
 -VirtualHubId <String> -VpnServerConfigurationId <String> -VpnClientAddressPool <String[]> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0dc0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0dc0-111">DESCRIPTION</span></span>
<span data-ttu-id="f0dc0-112">Mit dem Cmdlet **New-AzP2sVpnGateway** können Sie einen neuen P2SVpnGateway unter VirtualHub für Punkt-zu-Standort-Konnektivität von Punkt zu Website Clients zu Azure VirtualWan erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-112">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity from Point to site clients to Azure VirtualWan.</span></span>

## <span data-ttu-id="f0dc0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0dc0-113">EXAMPLES</span></span>

### <span data-ttu-id="f0dc0-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0dc0-114">Example 1</span></span>
```powershell
PS C:\> $virtualHub = Get-AzVirtualHub -ResourceGroupName P2SCortexGATesting -Name WestUsVirtualHub
PS C:\> $vpnServerConfig1 = Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name WestUsConfig
PS C:\> $vpnClientAddressSpaces = New-Object string[] 1
PS C:\> $vpnClientAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $createdP2SVpnGateway = New-AzP2sVpnGateway -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw -VirtualHub $virtualHub -VpnGatewayScaleUnit 1 -VpnClientAddressPool $vpnClientAddressSpaces -VpnServerConfiguration $vpnServerConfig1

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
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="f0dc0-115">Mit dem Cmdlet **New-AzP2sVpnGateway** können Sie unter VirtualHub für Punkt-zu-Standort-Konnektivität ein neues P2SVpnGateway erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-115">The **New-AzP2sVpnGateway** cmdlet enables you to create a new P2SVpnGateway under VirtualHub for Point to site connectivity.</span></span>

## <span data-ttu-id="f0dc0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0dc0-116">PARAMETERS</span></span>

### <span data-ttu-id="f0dc0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0dc0-117">-AsJob</span></span>
<span data-ttu-id="f0dc0-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0dc0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0dc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0dc0-119">-DefaultProfile</span></span>
<span data-ttu-id="f0dc0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0dc0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f0dc0-121">-Name</span></span>
<span data-ttu-id="f0dc0-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-122">The resource name.</span></span>

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

### <span data-ttu-id="f0dc0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0dc0-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0dc0-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-124">The resource name.</span></span>

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

### <span data-ttu-id="f0dc0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0dc0-125">-Tag</span></span>
<span data-ttu-id="f0dc0-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f0dc0-127">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f0dc0-127">-VirtualHub</span></span>
<span data-ttu-id="f0dc0-128">Das VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-128">The VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="f0dc0-129">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="f0dc0-129">-VirtualHubId</span></span>
<span data-ttu-id="f0dc0-130">Die ID des VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-130">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="f0dc0-131">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="f0dc0-131">-VirtualHubName</span></span>
<span data-ttu-id="f0dc0-132">Die ID des VirtualHub, dem dieses P2SVpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-132">The Id of the VirtualHub this P2SVpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="f0dc0-133">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0dc0-133">-VpnClientAddressPool</span></span>
<span data-ttu-id="f0dc0-134">P2S VpnClient AddressPool P2SVpnGateway P2SConnectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-134">P2S VpnClient AddressPool for this P2SVpnGateway P2SConnectionConfiguration.</span></span>

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

### <span data-ttu-id="f0dc0-135">-VpnGatewayScaleUnit</span><span class="sxs-lookup"><span data-stu-id="f0dc0-135">-VpnGatewayScaleUnit</span></span>
<span data-ttu-id="f0dc0-136">Die Skalierungseinheit für diesen P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-136">The scale unit for this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="f0dc0-137">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0dc0-137">-VpnServerConfiguration</span></span>
<span data-ttu-id="f0dc0-138">Das VpnServerConfiguration, das an diesen P2SVpnGateway angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-138">The VpnServerConfiguration to be attached to this P2SVpnGateway.</span></span>

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

### <span data-ttu-id="f0dc0-139">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f0dc0-139">-VpnServerConfigurationId</span></span>
<span data-ttu-id="f0dc0-140">Die ID des VPN-Server-Konfigurationsobjekts, dem dieses P2SVpnGateway angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-140">The id of Vpn server configuration object this P2SVpnGateway will be attached to.</span></span>

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

### <span data-ttu-id="f0dc0-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0dc0-141">-Confirm</span></span>
<span data-ttu-id="f0dc0-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0dc0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0dc0-143">-WhatIf</span></span>
<span data-ttu-id="f0dc0-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0dc0-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0dc0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0dc0-146">CommonParameters</span></span>
<span data-ttu-id="f0dc0-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0dc0-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0dc0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0dc0-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0dc0-149">INPUTS</span></span>

### <span data-ttu-id="f0dc0-150">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f0dc0-150">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>
<span data-ttu-id="f0dc0-151">System. String Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0dc0-151">System.String Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="f0dc0-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0dc0-152">OUTPUTS</span></span>

### <span data-ttu-id="f0dc0-153">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="f0dc0-153">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="f0dc0-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0dc0-154">NOTES</span></span>

## <span data-ttu-id="f0dc0-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0dc0-155">RELATED LINKS</span></span>
