---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152001"
---
# <span data-ttu-id="e7f60-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e7f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f60-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f60-103">Ruft die IP-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="e7f60-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="e7f60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7f60-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7f60-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7f60-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f60-106">Das **Cmdlet "Get-AzApplicationGatewayIPConfiguration"** ruft die IP-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="e7f60-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="e7f60-107">Die IP-Konfiguration enthält das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e7f60-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="e7f60-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7f60-108">EXAMPLES</span></span>

### <span data-ttu-id="e7f60-109">Beispiel 1: Erhalten einer bestimmten IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="e7f60-110">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft eine IP-Konfiguration namens "GateSubnet01" aus dem Gateway ab, das in der $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e7f60-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="e7f60-111">Beispiel 2: Erhalten einer Liste der IP-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="e7f60-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="e7f60-112">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable. Der zweite Befehl ruft eine Liste aller IP-Konfigurationen ab.</span><span class="sxs-lookup"><span data-stu-id="e7f60-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="e7f60-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f60-113">PARAMETERS</span></span>

### <span data-ttu-id="e7f60-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7f60-114">-ApplicationGateway</span></span>
<span data-ttu-id="e7f60-115">Gibt das Anwendungsgatewayobjekt an, das die IP-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="e7f60-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="e7f60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f60-116">-DefaultProfile</span></span>
<span data-ttu-id="e7f60-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7f60-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f60-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e7f60-118">-Name</span></span>
<span data-ttu-id="e7f60-119">Gibt den Namen der IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e7f60-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="e7f60-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f60-120">CommonParameters</span></span>
<span data-ttu-id="e7f60-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f60-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f60-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7f60-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f60-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7f60-123">INPUTS</span></span>

### <span data-ttu-id="e7f60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e7f60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e7f60-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7f60-125">OUTPUTS</span></span>

### <span data-ttu-id="e7f60-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="e7f60-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e7f60-127">NOTES</span></span>

## <span data-ttu-id="e7f60-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e7f60-128">RELATED LINKS</span></span>

[<span data-ttu-id="e7f60-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7f60-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7f60-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="e7f60-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7f60-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


