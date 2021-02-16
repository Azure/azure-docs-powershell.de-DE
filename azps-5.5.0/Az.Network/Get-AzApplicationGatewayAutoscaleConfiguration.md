---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157137"
---
# <span data-ttu-id="a0ef7-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ef7-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a0ef7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ef7-103">Ruft die Autoskalierungskonfiguration des Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="a0ef7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0ef7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ef7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="a0ef7-106">Das **Cmdlet "Get-AzApplicationGatewayAutoscaleConfiguration"** ruft die Autoskalenkonfiguration des Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="a0ef7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="a0ef7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0ef7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="a0ef7-109">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in $gw Variable.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="a0ef7-110">Mit dem zweiten Befehl wird die Autoskalenkonfiguration aus dem Anwendungsgateway extrahiert.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="a0ef7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0ef7-111">PARAMETERS</span></span>

### <span data-ttu-id="a0ef7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0ef7-112">-ApplicationGateway</span></span>
<span data-ttu-id="a0ef7-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0ef7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a0ef7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ef7-114">-DefaultProfile</span></span>
<span data-ttu-id="a0ef7-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ef7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ef7-116">CommonParameters</span></span>
<span data-ttu-id="a0ef7-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ef7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ef7-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0ef7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ef7-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0ef7-119">INPUTS</span></span>

### <span data-ttu-id="a0ef7-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0ef7-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0ef7-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0ef7-121">OUTPUTS</span></span>

### <span data-ttu-id="a0ef7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ef7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="a0ef7-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0ef7-123">NOTES</span></span>

## <span data-ttu-id="a0ef7-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0ef7-124">RELATED LINKS</span></span>

[<span data-ttu-id="a0ef7-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ef7-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a0ef7-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ef7-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="a0ef7-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0ef7-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
