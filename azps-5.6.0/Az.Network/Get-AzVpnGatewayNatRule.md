---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpngatewaynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnGatewayNatRule.md
ms.openlocfilehash: 1670e8549f561f0b1fae12711303bb3e1ac83280
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925464"
---
# <span data-ttu-id="4a6ec-101">Get-AzVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="4a6ec-101">Get-AzVpnGatewayNatRule</span></span>

## <span data-ttu-id="4a6ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4a6ec-103">Ruft eine NAT-Regel ab, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-103">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="4a6ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a6ec-104">SYNTAX</span></span>

### <span data-ttu-id="4a6ec-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnGatewayNatRule -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a6ec-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4a6ec-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnGatewayNatRule -ParentObject <PSVpnGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a6ec-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6ec-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnGatewayNatRule -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a6ec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a6ec-108">DESCRIPTION</span></span>
<span data-ttu-id="4a6ec-109">Ruft eine NAT-Regel ab, die vpnGateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-109">Gets a NAT rule associated with VpnGateway.</span></span>

## <span data-ttu-id="4a6ec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a6ec-110">EXAMPLES</span></span>

### <span data-ttu-id="4a6ec-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a6ec-111">Example</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> New-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule" -Type Static -Mode EgressSnat -InternalMapping "10.0.0.1/26" -ExternalMapping "192.168.0.0/26"
PS C:\> Get-AzVpnGatewayNatRule -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testNatRule"

Type                      : Static
Mode                      : EgressSnat
VpnConnectionProtocolType : IKEv2
InternalMappings          : 10.0.0.1/26
ExternalMappings          : 192.168.0.0/26
IpConfigurationId         :
IngressVpnSiteLinkConnections : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
EgressVpnSiteLinkConnections  : [Microsoft.Azure.Commands.Network.Models.PSResourceId]
ProvisioningState         : Provisioned
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/natRules/testNatRule

```

<span data-ttu-id="4a6ec-112">Mit dem vorstehenden Beispiel wird eine Ressourcengruppe, virtuelles WAN, virtuelles Netzwerk, virtueller Hub und VpnGateway & nat-Regel erstellt, die vpngateway zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and VpnGateway & a NAT rule associated with Vpngateway.</span></span>
<span data-ttu-id="4a6ec-113">Anschließend ruft sie die NAT-Regel mit dem Namen der NAT-Regel ab.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-113">Then it gets the NAT rule using the NAT rule name.</span></span>

## <span data-ttu-id="4a6ec-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a6ec-114">PARAMETERS</span></span>

### <span data-ttu-id="4a6ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a6ec-115">-DefaultProfile</span></span>
<span data-ttu-id="4a6ec-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a6ec-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4a6ec-117">-Name</span></span>
<span data-ttu-id="4a6ec-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnGatewayNatRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6ec-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a6ec-119">-ParentObject</span></span>
<span data-ttu-id="4a6ec-120">Das übergeordnete VpnGateway für dieses VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-120">The parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6ec-121">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4a6ec-121">-ParentResourceId</span></span>
<span data-ttu-id="4a6ec-122">Die Ressourcen-ID des übergeordneten VpnGateways für dieses VpnGatewayNatRule.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-122">The resource id of the parent VpnGateway for this VpnGatewayNatRule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a6ec-123">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="4a6ec-123">-ParentResourceName</span></span>
<span data-ttu-id="4a6ec-124">Der übergeordnete Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a6ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a6ec-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a6ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a6ec-127">CommonParameters</span></span>
<span data-ttu-id="4a6ec-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a6ec-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a6ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a6ec-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a6ec-130">INPUTS</span></span>

### <span data-ttu-id="4a6ec-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4a6ec-131">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="4a6ec-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4a6ec-132">System.String</span></span>

## <span data-ttu-id="4a6ec-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a6ec-133">OUTPUTS</span></span>

### <span data-ttu-id="4a6ec-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span><span class="sxs-lookup"><span data-stu-id="4a6ec-134">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayNatRule</span></span>

## <span data-ttu-id="4a6ec-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a6ec-135">NOTES</span></span>

## <span data-ttu-id="4a6ec-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a6ec-136">RELATED LINKS</span></span>
