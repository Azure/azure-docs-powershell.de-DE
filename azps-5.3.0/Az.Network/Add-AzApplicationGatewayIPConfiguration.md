---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380272"
---
# <span data-ttu-id="b6468-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6468-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b6468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6468-102">SYNOPSIS</span></span>
<span data-ttu-id="b6468-103">Fügt einem Anwendungsgateway eine IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="b6468-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="b6468-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6468-104">SYNTAX</span></span>

### <span data-ttu-id="b6468-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6468-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6468-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6468-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6468-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6468-107">DESCRIPTION</span></span>
<span data-ttu-id="b6468-108">Das **Cmdlet "Add-AzApplicationGatewayIPConfiguration"** fügt einem Anwendungsgateway eine IP-Konfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="b6468-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="b6468-109">IP-Konfigurationen enthalten das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b6468-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b6468-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6468-110">EXAMPLES</span></span>

### <span data-ttu-id="b6468-111">Beispiel 1: Hinzufügen einer virtuellen Netzwerkkonfiguration zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b6468-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="b6468-112">Der erste Befehl ruft ein virtuelles Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="b6468-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="b6468-113">Der zweite Befehl ruft ein Subnetz mit dem zuvor erstellten virtuellen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="b6468-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="b6468-114">Der dritte Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="b6468-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b6468-115">Der vierte Befehl fügt die IP-Konfiguration dem Anwendungsgateway hinzu, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b6468-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b6468-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6468-116">PARAMETERS</span></span>

### <span data-ttu-id="b6468-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6468-117">-ApplicationGateway</span></span>
<span data-ttu-id="b6468-118">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine IP-Konfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b6468-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="b6468-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6468-119">-DefaultProfile</span></span>
<span data-ttu-id="b6468-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6468-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6468-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b6468-121">-Name</span></span>
<span data-ttu-id="b6468-122">Gibt den Namen der hinzuzufügenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b6468-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="b6468-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b6468-123">-Subnet</span></span>
<span data-ttu-id="b6468-124">Gibt ein Subnetz an.</span><span class="sxs-lookup"><span data-stu-id="b6468-124">Specifies a subnet.</span></span>
<span data-ttu-id="b6468-125">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b6468-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b6468-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b6468-126">-SubnetId</span></span>
<span data-ttu-id="b6468-127">Gibt eine Subnetz-ID an.</span><span class="sxs-lookup"><span data-stu-id="b6468-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="b6468-128">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b6468-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b6468-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6468-129">CommonParameters</span></span>
<span data-ttu-id="b6468-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6468-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6468-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6468-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6468-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6468-132">INPUTS</span></span>

### <span data-ttu-id="b6468-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6468-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6468-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6468-134">OUTPUTS</span></span>

### <span data-ttu-id="b6468-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6468-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6468-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b6468-136">NOTES</span></span>

## <span data-ttu-id="b6468-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b6468-137">RELATED LINKS</span></span>

[<span data-ttu-id="b6468-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6468-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b6468-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6468-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b6468-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6468-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b6468-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6468-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


