---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: bfaf9773582b201de8f6066a30a55c0fd5f5b7ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472201"
---
# <span data-ttu-id="1d0b0-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1d0b0-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="1d0b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1d0b0-103">Ändert die SKU eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="1d0b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d0b0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d0b0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="1d0b0-106">Das **Cmdlet "Set-AzApplicationGatewaySku"** ändert die SKU (Stock Keeping Unit) eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="1d0b0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d0b0-107">EXAMPLES</span></span>

### <span data-ttu-id="1d0b0-108">Beispiel 1: Aktualisieren der Anwendungsgateway-SKU</span><span class="sxs-lookup"><span data-stu-id="1d0b0-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="1d0b0-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1d0b0-110">Mit dem zweiten Befehl wird die SKU des Anwendungsgateways aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="1d0b0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d0b0-111">PARAMETERS</span></span>

### <span data-ttu-id="1d0b0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d0b0-112">-ApplicationGateway</span></span>
<span data-ttu-id="1d0b0-113">Gibt das Anwendungsgatewayobjekt an, dem dieses Cmdlet die SKU zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="1d0b0-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="1d0b0-114">-Capacity</span></span>
<span data-ttu-id="1d0b0-115">Gibt die Instanzenanzahl des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d0b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d0b0-116">-DefaultProfile</span></span>
<span data-ttu-id="1d0b0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d0b0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1d0b0-118">-Name</span></span>
<span data-ttu-id="1d0b0-119">Gibt den Namen des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="1d0b0-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1d0b0-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d0b0-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="1d0b0-121">Standard_Small</span></span>
- <span data-ttu-id="1d0b0-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="1d0b0-122">Standard_Medium</span></span>
- <span data-ttu-id="1d0b0-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="1d0b0-123">Standard_Large</span></span>
- <span data-ttu-id="1d0b0-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="1d0b0-124">WAF_Medium</span></span>
- <span data-ttu-id="1d0b0-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="1d0b0-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d0b0-126">-Tier</span><span class="sxs-lookup"><span data-stu-id="1d0b0-126">-Tier</span></span>
<span data-ttu-id="1d0b0-127">Gibt die Stufe des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="1d0b0-128">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1d0b0-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d0b0-129">Standard</span><span class="sxs-lookup"><span data-stu-id="1d0b0-129">Standard</span></span>
- <span data-ttu-id="1d0b0-130">WAF</span><span class="sxs-lookup"><span data-stu-id="1d0b0-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d0b0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d0b0-131">CommonParameters</span></span>
<span data-ttu-id="1d0b0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d0b0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d0b0-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d0b0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d0b0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d0b0-134">INPUTS</span></span>

### <span data-ttu-id="1d0b0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d0b0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1d0b0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d0b0-136">OUTPUTS</span></span>

### <span data-ttu-id="1d0b0-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d0b0-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1d0b0-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d0b0-138">NOTES</span></span>

## <span data-ttu-id="1d0b0-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d0b0-139">RELATED LINKS</span></span>

[<span data-ttu-id="1d0b0-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1d0b0-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="1d0b0-141">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1d0b0-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


