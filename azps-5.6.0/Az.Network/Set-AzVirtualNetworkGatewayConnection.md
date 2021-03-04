---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: bb937dab16e30eba28b247d5010e3fa8fcc37954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932347"
---
# <span data-ttu-id="fb99e-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="fb99e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb99e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb99e-103">Konfiguriert eine Verbindung mit einem virtuellen Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="fb99e-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="fb99e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb99e-104">SYNTAX</span></span>

### <span data-ttu-id="fb99e-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb99e-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb99e-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="fb99e-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb99e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb99e-107">DESCRIPTION</span></span>
<span data-ttu-id="fb99e-108">Das **Cmdlet Set-AzVirtualNetworkGatewayConnection** konfiguriert eine Gatewayverbindung für virtuelle Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="fb99e-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="fb99e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb99e-109">EXAMPLES</span></span>

### <span data-ttu-id="fb99e-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="fb99e-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="fb99e-111">Beispiel 2: Hinzufügen/Aktualisieren von Tags zu einem vorhandenen VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="fb99e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fb99e-112">PARAMETERS</span></span>

### <span data-ttu-id="fb99e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb99e-113">-AsJob</span></span>
<span data-ttu-id="fb99e-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fb99e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb99e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb99e-115">-DefaultProfile</span></span>
<span data-ttu-id="fb99e-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb99e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb99e-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fb99e-117">-EnableBgp</span></span>
<span data-ttu-id="fb99e-118">Verwenden einer BGP-Sitzung über einen S2S-VPN-Tunnel</span><span class="sxs-lookup"><span data-stu-id="fb99e-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="fb99e-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="fb99e-120">Timeout für die Erkennung von "Tote Peers" der Verbindung in Sekunden</span><span class="sxs-lookup"><span data-stu-id="fb99e-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-121">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="fb99e-121">-ConnectionMode</span></span>
<span data-ttu-id="fb99e-122">Verbindungsmodus für virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="fb99e-122">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fb99e-123">-Force</span></span>
<span data-ttu-id="fb99e-124">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="fb99e-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb99e-125">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="fb99e-125">-IpsecPolicies</span></span>
<span data-ttu-id="fb99e-126">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="fb99e-126">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb99e-127">-Tag</span></span>
<span data-ttu-id="fb99e-128">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb99e-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-129">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="fb99e-129">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="fb99e-130">Eine Liste der Richtlinien für die Verkehrsauswahl.</span><span class="sxs-lookup"><span data-stu-id="fb99e-130">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-131">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb99e-131">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="fb99e-132">Verwenden von PrivateIP für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="fb99e-132">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="fb99e-133">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="fb99e-133">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="fb99e-134">Verwenden von richtlinienbasierten Datenverkehrsauswahlen für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="fb99e-134">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="fb99e-135">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-135">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="fb99e-136">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das von diesem Cmdlet zum Ändern der Verbindung des virtuellen Netzwerkgateways verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb99e-136">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb99e-137">-Confirm</span></span>
<span data-ttu-id="fb99e-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb99e-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb99e-139">-WhatIf</span></span>
<span data-ttu-id="fb99e-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb99e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb99e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb99e-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb99e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb99e-142">CommonParameters</span></span>
<span data-ttu-id="fb99e-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb99e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb99e-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb99e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb99e-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb99e-145">INPUTS</span></span>

### <span data-ttu-id="fb99e-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="fb99e-147">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb99e-147">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb99e-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="fb99e-148">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="fb99e-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="fb99e-149">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="fb99e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb99e-150">OUTPUTS</span></span>

### <span data-ttu-id="fb99e-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-151">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="fb99e-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fb99e-152">NOTES</span></span>

## <span data-ttu-id="fb99e-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fb99e-153">RELATED LINKS</span></span>

[<span data-ttu-id="fb99e-154">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-154">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fb99e-155">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-155">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="fb99e-156">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fb99e-156">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


