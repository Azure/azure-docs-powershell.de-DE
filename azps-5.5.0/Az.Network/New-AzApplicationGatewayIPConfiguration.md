---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146961"
---
# <span data-ttu-id="7ad17-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7ad17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ad17-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad17-103">Erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7ad17-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="7ad17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ad17-104">SYNTAX</span></span>

### <span data-ttu-id="7ad17-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad17-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ad17-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7ad17-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ad17-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ad17-107">DESCRIPTION</span></span>
<span data-ttu-id="7ad17-108">Das **Cmdlet "New-AzApplicationGatewayIPConfiguration"** erstellt eine IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7ad17-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="7ad17-109">Die IP-Konfiguration enthält das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ad17-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="7ad17-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ad17-110">EXAMPLES</span></span>

### <span data-ttu-id="7ad17-111">Beispiel 1: Erstellen einer IP-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7ad17-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="7ad17-112">Der erste Befehl ruft ein virtuelles Netzwerk namens VNet01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört.</span><span class="sxs-lookup"><span data-stu-id="7ad17-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="7ad17-113">Der zweite Befehl ruft die Subnetzkonfiguration für das Subnetz ab, dem das virtuelle Netzwerk im vorherigen Befehl angehört, und speichert es in $Subnet Variable.</span><span class="sxs-lookup"><span data-stu-id="7ad17-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="7ad17-114">Der dritte Befehl erstellt die IP-Konfiguration mithilfe $Subnet.</span><span class="sxs-lookup"><span data-stu-id="7ad17-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="7ad17-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ad17-115">PARAMETERS</span></span>

### <span data-ttu-id="7ad17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad17-116">-DefaultProfile</span></span>
<span data-ttu-id="7ad17-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ad17-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ad17-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7ad17-118">-Name</span></span>
<span data-ttu-id="7ad17-119">Gibt den Namen der zu erstellenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="7ad17-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="7ad17-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="7ad17-120">-Subnet</span></span>
<span data-ttu-id="7ad17-121">Gibt das Subnetzobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7ad17-121">Specifies the subnet object.</span></span>
<span data-ttu-id="7ad17-122">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ad17-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7ad17-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7ad17-123">-SubnetId</span></span>
<span data-ttu-id="7ad17-124">Gibt die Subnetz-ID an.</span><span class="sxs-lookup"><span data-stu-id="7ad17-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="7ad17-125">Dies ist das Subnetz, in dem das Anwendungsgateway bereitgestellt würde.</span><span class="sxs-lookup"><span data-stu-id="7ad17-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="7ad17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad17-126">CommonParameters</span></span>
<span data-ttu-id="7ad17-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad17-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad17-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad17-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ad17-129">INPUTS</span></span>

### <span data-ttu-id="7ad17-130">Keine</span><span class="sxs-lookup"><span data-stu-id="7ad17-130">None</span></span>

## <span data-ttu-id="7ad17-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ad17-131">OUTPUTS</span></span>

### <span data-ttu-id="7ad17-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7ad17-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ad17-133">NOTES</span></span>

## <span data-ttu-id="7ad17-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ad17-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ad17-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad17-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad17-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7ad17-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7ad17-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


