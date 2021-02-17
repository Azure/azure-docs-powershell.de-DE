---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169781"
---
# <span data-ttu-id="d2a0d-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2a0d-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d2a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a0d-103">Erstellt eine IP-Konfiguration für ein virtuelles Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="d2a0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2a0d-104">SYNTAX</span></span>

### <span data-ttu-id="d2a0d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d2a0d-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2a0d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d2a0d-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a0d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2a0d-107">DESCRIPTION</span></span>
<span data-ttu-id="d2a0d-108">Das **Cmdlet "New-AzVirtualNetworkGatewayIpConfig"** erstellt eine Konfiguration, die einem virtuellen Netzwerkgateway zugewiesen ist, mit einer (zuvor erstellten) öffentlichen IP-Adresse, die auf einer Subnetz-ID basiert.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="d2a0d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2a0d-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a0d-110">1: Erstellen einer IP-Konfiguration für ein virtuelles Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="d2a0d-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="d2a0d-111">Konfiguriert ein virtuelles Netzwerkgateway mit einer öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="d2a0d-112">Die Variable $myGWsubnet wird mithilfe des **Cmdlets "Get-AzVirtualNetworkSubnetConfig"** auf dem "GatewaySubnet" im virtuellen Netzwerk, das Sie erstellen möchten, ermittelt.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="d2a0d-113">Die variable $myGWpip wird mit dem **Cmdlet "New-AzPublicIpAddress"** ermittelt.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="d2a0d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2a0d-114">PARAMETERS</span></span>

### <span data-ttu-id="d2a0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a0d-115">-DefaultProfile</span></span>
<span data-ttu-id="d2a0d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a0d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d2a0d-117">-Name</span></span>
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

### <span data-ttu-id="d2a0d-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d2a0d-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="d2a0d-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d2a0d-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="d2a0d-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d2a0d-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="d2a0d-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d2a0d-121">-Subnet</span></span>
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

### <span data-ttu-id="d2a0d-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d2a0d-122">-SubnetId</span></span>
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

### <span data-ttu-id="d2a0d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a0d-123">CommonParameters</span></span>
<span data-ttu-id="d2a0d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a0d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a0d-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a0d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a0d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2a0d-126">INPUTS</span></span>

### <span data-ttu-id="d2a0d-127">Keine</span><span class="sxs-lookup"><span data-stu-id="d2a0d-127">None</span></span>

## <span data-ttu-id="d2a0d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2a0d-128">OUTPUTS</span></span>

### <span data-ttu-id="d2a0d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2a0d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="d2a0d-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2a0d-130">NOTES</span></span>

## <span data-ttu-id="d2a0d-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2a0d-131">RELATED LINKS</span></span>

[<span data-ttu-id="d2a0d-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2a0d-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d2a0d-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2a0d-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
