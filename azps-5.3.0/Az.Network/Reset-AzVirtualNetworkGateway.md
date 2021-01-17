---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468847"
---
# <span data-ttu-id="fb621-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="fb621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb621-102">SYNOPSIS</span></span>
<span data-ttu-id="fb621-103">Setzt das virtuelle Netzwerkgateway zurück.</span><span class="sxs-lookup"><span data-stu-id="fb621-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="fb621-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb621-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb621-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb621-105">DESCRIPTION</span></span>
<span data-ttu-id="fb621-106">Setzt das virtuelle Netzwerkgateway zurück.</span><span class="sxs-lookup"><span data-stu-id="fb621-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="fb621-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fb621-107">EXAMPLES</span></span>

### <span data-ttu-id="fb621-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="fb621-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="fb621-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb621-109">PARAMETERS</span></span>

### <span data-ttu-id="fb621-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb621-110">-AsJob</span></span>
<span data-ttu-id="fb621-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fb621-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb621-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb621-112">-DefaultProfile</span></span>
<span data-ttu-id="fb621-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb621-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb621-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="fb621-114">-GatewayVip</span></span>
<span data-ttu-id="fb621-115">Die Gateway-VIP, um eine bestimmte Gatewayinstanz zurückzusetzen (z. B. bei Active-Active Gateways mit aktivierter Funktion) Standardmäßig wird die primäre Gatewayinstanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb621-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb621-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-116">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb621-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb621-117">CommonParameters</span></span>
<span data-ttu-id="fb621-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb621-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb621-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb621-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb621-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fb621-120">INPUTS</span></span>

### <span data-ttu-id="fb621-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="fb621-122">System.String</span><span class="sxs-lookup"><span data-stu-id="fb621-122">System.String</span></span>

## <span data-ttu-id="fb621-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fb621-123">OUTPUTS</span></span>

### <span data-ttu-id="fb621-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fb621-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fb621-125">NOTES</span></span>

## <span data-ttu-id="fb621-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fb621-126">RELATED LINKS</span></span>

[<span data-ttu-id="fb621-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb621-128">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb621-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb621-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="fb621-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fb621-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
