---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174260"
---
# <span data-ttu-id="b6b38-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b6b38-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6b38-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b38-103">Konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b6b38-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b6b38-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6b38-104">SYNTAX</span></span>

### <span data-ttu-id="b6b38-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6b38-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6b38-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="b6b38-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b38-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6b38-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b38-108">Das Cmdlet " **Satz-AzVirtualNetworkGatewayConnection** " konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b6b38-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="b6b38-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6b38-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b38-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="b6b38-110">Example 1:</span></span>
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

### <span data-ttu-id="b6b38-111">Beispiel 2: Hinzufügen/Aktualisieren von Tags zu einem vorhandenen VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="b6b38-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6b38-112">PARAMETERS</span></span>

### <span data-ttu-id="b6b38-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6b38-113">-AsJob</span></span>
<span data-ttu-id="b6b38-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b6b38-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6b38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b38-115">-DefaultProfile</span></span>
<span data-ttu-id="b6b38-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6b38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6b38-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="b6b38-117">-EnableBgp</span></span>
<span data-ttu-id="b6b38-118">Ob eine BGP-Sitzung über einen S2S-VPN-Tunnel verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="b6b38-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="b6b38-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="b6b38-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="b6b38-120">Timeout der Peer Erkennung für die Verbindung in Sekunden</span><span class="sxs-lookup"><span data-stu-id="b6b38-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="b6b38-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b6b38-121">-Force</span></span>
<span data-ttu-id="b6b38-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b6b38-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6b38-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="b6b38-123">-IpsecPolicies</span></span>
<span data-ttu-id="b6b38-124">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="b6b38-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="b6b38-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6b38-125">-Tag</span></span>
<span data-ttu-id="b6b38-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="b6b38-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b6b38-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="b6b38-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="b6b38-128">Eine Liste der Datenverkehrs Auswahlrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="b6b38-128">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="b6b38-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="b6b38-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="b6b38-130">Ob PrivateIP für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="b6b38-130">Whether to use PrivateIP for a S2S connection</span></span>

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

### <span data-ttu-id="b6b38-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="b6b38-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="b6b38-132">Ob richtlinienbasierte Datenverkehrs Auswahl für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="b6b38-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="b6b38-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="b6b38-134">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das dieses Cmdlet zum Ändern der virtuellen Netzwerkgateway-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6b38-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="b6b38-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6b38-135">-Confirm</span></span>
<span data-ttu-id="b6b38-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6b38-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b38-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b38-137">-WhatIf</span></span>
<span data-ttu-id="b6b38-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6b38-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b38-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6b38-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b38-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b38-140">CommonParameters</span></span>
<span data-ttu-id="b6b38-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6b38-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b38-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b38-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b38-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6b38-143">INPUTS</span></span>

### <span data-ttu-id="b6b38-144">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="b6b38-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6b38-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6b38-146">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="b6b38-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="b6b38-147">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="b6b38-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="b6b38-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6b38-148">OUTPUTS</span></span>

### <span data-ttu-id="b6b38-149">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b6b38-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6b38-150">NOTES</span></span>

## <span data-ttu-id="b6b38-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6b38-151">RELATED LINKS</span></span>

[<span data-ttu-id="b6b38-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b6b38-153">Neu – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b6b38-154">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b6b38-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


