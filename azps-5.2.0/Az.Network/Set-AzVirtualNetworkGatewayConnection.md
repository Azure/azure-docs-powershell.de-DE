---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293632"
---
# <span data-ttu-id="25dc8-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="25dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="25dc8-103">Konfiguriert eine virtuelle Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="25dc8-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="25dc8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25dc8-104">SYNTAX</span></span>

### <span data-ttu-id="25dc8-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="25dc8-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25dc8-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="25dc8-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25dc8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="25dc8-108">Das **Cmdlet Set-AzVirtualNetworkGatewayConnection** konfiguriert eine virtuelle Netzwerkgatewayverbindung.</span><span class="sxs-lookup"><span data-stu-id="25dc8-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="25dc8-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="25dc8-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="25dc8-110">Example 1:</span></span>
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

### <span data-ttu-id="25dc8-111">Beispiel 2: Hinzufügen/Aktualisieren von Tags zu einem vorhandenen VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="25dc8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25dc8-112">PARAMETERS</span></span>

### <span data-ttu-id="25dc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25dc8-113">-AsJob</span></span>
<span data-ttu-id="25dc8-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25dc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25dc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25dc8-115">-DefaultProfile</span></span>
<span data-ttu-id="25dc8-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25dc8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25dc8-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="25dc8-117">-EnableBgp</span></span>
<span data-ttu-id="25dc8-118">Verwenden einer BGP-Sitzung über einen S2S-VPN-Tunnel</span><span class="sxs-lookup"><span data-stu-id="25dc8-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="25dc8-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="25dc8-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="25dc8-120">Timeout für die Erkennung des in den In-Tote-Peers festgelegten Timeouts für die Verbindung in Sekunden</span><span class="sxs-lookup"><span data-stu-id="25dc8-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="25dc8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="25dc8-121">-Force</span></span>
<span data-ttu-id="25dc8-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="25dc8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25dc8-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="25dc8-123">-IpsecPolicies</span></span>
<span data-ttu-id="25dc8-124">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="25dc8-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="25dc8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="25dc8-125">-Tag</span></span>
<span data-ttu-id="25dc8-126">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="25dc8-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="25dc8-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="25dc8-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="25dc8-128">Eine Liste der Richtlinien für die Verkehrsauswahl.</span><span class="sxs-lookup"><span data-stu-id="25dc8-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="25dc8-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="25dc8-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="25dc8-130">Verwenden von PrivateIP für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="25dc8-130">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="25dc8-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="25dc8-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="25dc8-132">Verwenden richtlinienbasierter Datenverkehrsauswahlen für eine S2S-Verbindung</span><span class="sxs-lookup"><span data-stu-id="25dc8-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="25dc8-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="25dc8-134">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das von diesem Cmdlet zum Ändern der virtuellen Netzwerkgatewayverbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25dc8-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="25dc8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25dc8-135">-Confirm</span></span>
<span data-ttu-id="25dc8-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25dc8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25dc8-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25dc8-137">-WhatIf</span></span>
<span data-ttu-id="25dc8-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25dc8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25dc8-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25dc8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25dc8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dc8-140">CommonParameters</span></span>
<span data-ttu-id="25dc8-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25dc8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dc8-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25dc8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dc8-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25dc8-143">INPUTS</span></span>

### <span data-ttu-id="25dc8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="25dc8-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="25dc8-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="25dc8-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="25dc8-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="25dc8-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="25dc8-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="25dc8-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25dc8-148">OUTPUTS</span></span>

### <span data-ttu-id="25dc8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="25dc8-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25dc8-150">NOTES</span></span>

## <span data-ttu-id="25dc8-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25dc8-151">RELATED LINKS</span></span>

[<span data-ttu-id="25dc8-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="25dc8-153">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="25dc8-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="25dc8-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


