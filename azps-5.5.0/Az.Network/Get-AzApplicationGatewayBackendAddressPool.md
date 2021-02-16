---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4B2066B6-51D7-46D8-8A72-1A232B3E6589
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 6ca7bc3e5d1af477c7d6750f674272ff64d54889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157100"
---
# <span data-ttu-id="fae92-101">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-101">Get-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="fae92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae92-102">SYNOPSIS</span></span>
<span data-ttu-id="fae92-103">Ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="fae92-103">Gets a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="fae92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fae92-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendAddressPool [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fae92-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fae92-105">DESCRIPTION</span></span>
<span data-ttu-id="fae92-106">Das **Cmdlet "Get-AzApplicationGatewayBackendAddressPool"** ruft eine oder mehrere Back-End-Adresspoolkonfigurationen von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="fae92-106">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets one or more backend address pool configurations from an application gateway.</span></span>

## <span data-ttu-id="fae92-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fae92-107">EXAMPLES</span></span>

### <span data-ttu-id="fae92-108">Beispiel 1: Einen angegebenen Back-End-Serverpool erhalten</span><span class="sxs-lookup"><span data-stu-id="fae92-108">Example 1: Get a specified back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPool = Get-AzApplicationGatewayBackendAddressPool -Name "Pool01" -ApplicationGateway $AppGw
```

<span data-ttu-id="fae92-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="fae92-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fae92-110">Der zweite Befehl ruft den Back-End-Adresspool ab, der $AppGw "Pool01" zugeordnet ist, und speichert ihn in der $BackendPool Variable.</span><span class="sxs-lookup"><span data-stu-id="fae92-110">The second command gets the back-end address pool associated with $AppGw named Pool01 and stores it in the $BackendPool variable.</span></span>

### <span data-ttu-id="fae92-111">Beispiel 2: Erhalten einer Liste des Back-End-Serverpools</span><span class="sxs-lookup"><span data-stu-id="fae92-111">Example 2: Get a list of back-end server pool</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $BackendPools = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw
```

<span data-ttu-id="fae92-112">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="fae92-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fae92-113">Der zweite Befehl ruft eine Liste der Back-End-Adresspools ab, die $AppGw zugeordnet sind, und speichert die Liste in der $BackendPools Variable.</span><span class="sxs-lookup"><span data-stu-id="fae92-113">The second command gets a list of the back-end address pools associated with $AppGw, and stores the list in the $BackendPools variable.</span></span>

## <span data-ttu-id="fae92-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fae92-114">PARAMETERS</span></span>

### <span data-ttu-id="fae92-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fae92-115">-ApplicationGateway</span></span>
<span data-ttu-id="fae92-116">Das **Cmdlet "Get-AzApplicationGatewayBackendAddressPool"** ruft einen Back-End-Adresspool für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="fae92-116">The **Get-AzApplicationGatewayBackendAddressPool** cmdlet gets a back-end address pool for an application gateway.</span></span>

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

### <span data-ttu-id="fae92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae92-117">-DefaultProfile</span></span>
<span data-ttu-id="fae92-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fae92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae92-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fae92-119">-Name</span></span>
<span data-ttu-id="fae92-120">Gibt den Namen des Back-End-Adresspools an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="fae92-120">Specifies the name of the back-end address pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fae92-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae92-121">CommonParameters</span></span>
<span data-ttu-id="fae92-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae92-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae92-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fae92-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae92-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fae92-124">INPUTS</span></span>

### <span data-ttu-id="fae92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fae92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fae92-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fae92-126">OUTPUTS</span></span>

### <span data-ttu-id="fae92-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="fae92-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fae92-128">NOTES</span></span>

## <span data-ttu-id="fae92-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fae92-129">RELATED LINKS</span></span>

[<span data-ttu-id="fae92-130">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-130">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fae92-131">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-131">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fae92-132">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-132">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="fae92-133">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fae92-133">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


