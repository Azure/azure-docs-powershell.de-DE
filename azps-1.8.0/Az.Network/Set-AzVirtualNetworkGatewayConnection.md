---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 15023fbbb0576f99f66519198c893080ebe1c92f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660167"
---
# <span data-ttu-id="f649c-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f649c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f649c-102">SYNOPSIS</span></span>
<span data-ttu-id="f649c-103">Konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f649c-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="f649c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f649c-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f649c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f649c-105">DESCRIPTION</span></span>
<span data-ttu-id="f649c-106">Das Cmdlet " **Satz-AzVirtualNetworkGatewayConnection** " konfiguriert eine virtuelle Netzwerkgateway-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="f649c-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="f649c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f649c-107">EXAMPLES</span></span>

### <span data-ttu-id="f649c-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="f649c-108">Example 1:</span></span>
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

## <span data-ttu-id="f649c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f649c-109">PARAMETERS</span></span>

### <span data-ttu-id="f649c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f649c-110">-AsJob</span></span>
<span data-ttu-id="f649c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f649c-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f649c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f649c-112">-DefaultProfile</span></span>
<span data-ttu-id="f649c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f649c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f649c-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f649c-114">-EnableBgp</span></span>
<span data-ttu-id="f649c-115">Ob eine BGP-Sitzung über einen S2S-VPN-Tunnel verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f649c-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="f649c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f649c-116">-Force</span></span>
<span data-ttu-id="f649c-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f649c-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f649c-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="f649c-118">-IpsecPolicies</span></span>
<span data-ttu-id="f649c-119">Eine Liste der IPSec-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="f649c-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="f649c-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f649c-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f649c-121">Ob richtlinienbasierte Datenverkehrs Auswahl für eine S2S-Verbindung verwendet werden soll</span><span class="sxs-lookup"><span data-stu-id="f649c-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="f649c-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="f649c-123">Gibt das PSVirtualNetworkGatewayConnection-Objekt an, das dieses Cmdlet zum Ändern der virtuellen Netzwerkgateway-Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f649c-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="f649c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f649c-124">-Confirm</span></span>
<span data-ttu-id="f649c-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f649c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f649c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f649c-126">-WhatIf</span></span>
<span data-ttu-id="f649c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f649c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f649c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f649c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f649c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f649c-129">CommonParameters</span></span>
<span data-ttu-id="f649c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f649c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f649c-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f649c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f649c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f649c-132">INPUTS</span></span>

### <span data-ttu-id="f649c-133">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="f649c-134">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f649c-134">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f649c-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f649c-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="f649c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f649c-136">OUTPUTS</span></span>

### <span data-ttu-id="f649c-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f649c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f649c-138">NOTES</span></span>

## <span data-ttu-id="f649c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f649c-139">RELATED LINKS</span></span>

[<span data-ttu-id="f649c-140">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-140">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f649c-141">Neu – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-141">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f649c-142">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f649c-142">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


