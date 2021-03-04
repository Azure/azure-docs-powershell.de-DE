---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924683"
---
# <span data-ttu-id="a568f-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a568f-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="a568f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a568f-102">SYNOPSIS</span></span>
<span data-ttu-id="a568f-103">Erstellt eine IP-Konfiguration für ein Virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="a568f-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="a568f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a568f-104">SYNTAX</span></span>

### <span data-ttu-id="a568f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a568f-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a568f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a568f-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a568f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a568f-107">DESCRIPTION</span></span>
<span data-ttu-id="a568f-108">Das **Cmdlet New-AzVirtualNetworkGatewayIpConfig** erstellt eine Konfiguration, die einem Virtuellen Netzwerkgateway mit einer (zuvor erstellten) öffentlichen IP-Adresse basierend auf der Subnetz-ID zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a568f-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="a568f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a568f-109">EXAMPLES</span></span>

### <span data-ttu-id="a568f-110">1: Erstellen einer IP-Konfiguration für ein Virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="a568f-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="a568f-111">Konfiguriert ein Virtuelles Netzwerkgateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="a568f-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="a568f-112">Die Variable $myGWsubnet wird mithilfe des **Get-AzVirtualNetworkSubnetConfig-Cmdlets** im "GatewaySubnet" im virtuellen Netzwerk ermittelt, das Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="a568f-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="a568f-113">Die Variable $myGWpip wird mithilfe des **Cmdlets New-AzPublicIpAddress** ermittelt.</span><span class="sxs-lookup"><span data-stu-id="a568f-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="a568f-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a568f-114">PARAMETERS</span></span>

### <span data-ttu-id="a568f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a568f-115">-DefaultProfile</span></span>
<span data-ttu-id="a568f-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a568f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a568f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a568f-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a568f-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a568f-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a568f-120">-PublicIpAddressId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-121">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="a568f-121">-Subnet</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a568f-122">-SubnetId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a568f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a568f-123">CommonParameters</span></span>
<span data-ttu-id="a568f-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a568f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a568f-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a568f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a568f-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a568f-126">INPUTS</span></span>

### <span data-ttu-id="a568f-127">Keine</span><span class="sxs-lookup"><span data-stu-id="a568f-127">None</span></span>

## <span data-ttu-id="a568f-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a568f-128">OUTPUTS</span></span>

### <span data-ttu-id="a568f-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a568f-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="a568f-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a568f-130">NOTES</span></span>

## <span data-ttu-id="a568f-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a568f-131">RELATED LINKS</span></span>

[<span data-ttu-id="a568f-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a568f-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="a568f-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a568f-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
