---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944891"
---
# <span data-ttu-id="2bb4f-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2bb4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb4f-103">Ändert eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="2bb4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bb4f-104">SYNTAX</span></span>

### <span data-ttu-id="2bb4f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2bb4f-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bb4f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2bb4f-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bb4f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bb4f-107">DESCRIPTION</span></span>
<span data-ttu-id="2bb4f-108">Das **Cmdlet Set-AzApplicationGatewayIPConfiguration** ändert eine IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="2bb4f-109">Eine IP-Konfiguration enthält das Subnetz, in dem ein Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="2bb4f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2bb4f-110">EXAMPLES</span></span>

### <span data-ttu-id="2bb4f-111">Beispiel 1: Aktualisieren einer IP-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="2bb4f-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="2bb4f-112">Der erste Befehl ruft das virtuelle Netzwerk mit dem Namen VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $VNet Variablen.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="2bb4f-113">Der zweite Befehl ruft die Subnetzkonfiguration namens Subnetz01 mit $VNet ab und speichert sie in der $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="2bb4f-114">Der dritte Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört und es in der $AppGw speichert.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2bb4f-115">Mit dem vierten Befehl wird die IP-Konfiguration des in $AppGw gespeicherten Anwendungsgateways auf die in der App gespeicherte Subnetzkonfiguration $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="2bb4f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2bb4f-116">PARAMETERS</span></span>

### <span data-ttu-id="2bb4f-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bb4f-117">-ApplicationGateway</span></span>
<span data-ttu-id="2bb4f-118">Gibt ein Anwendungsgatewayobjekt an, dem dieses Cmdlet eine IP-Konfiguration zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb4f-119">-DefaultProfile</span></span>
<span data-ttu-id="2bb4f-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb4f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2bb4f-121">-Name</span></span>
<span data-ttu-id="2bb4f-122">Gibt den Namen der IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="2bb4f-123">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="2bb4f-123">-Subnet</span></span>
<span data-ttu-id="2bb4f-124">Gibt das Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-124">Specifies the subnet.</span></span>
<span data-ttu-id="2bb4f-125">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2bb4f-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2bb4f-126">-SubnetId</span></span>
<span data-ttu-id="2bb4f-127">Gibt die Subnetz-ID an.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="2bb4f-128">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2bb4f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb4f-129">CommonParameters</span></span>
<span data-ttu-id="2bb4f-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bb4f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb4f-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb4f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb4f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2bb4f-132">INPUTS</span></span>

### <span data-ttu-id="2bb4f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bb4f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2bb4f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2bb4f-134">OUTPUTS</span></span>

### <span data-ttu-id="2bb4f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bb4f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2bb4f-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2bb4f-136">NOTES</span></span>

## <span data-ttu-id="2bb4f-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2bb4f-137">RELATED LINKS</span></span>

[<span data-ttu-id="2bb4f-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2bb4f-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2bb4f-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2bb4f-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2bb4f-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb4f-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


