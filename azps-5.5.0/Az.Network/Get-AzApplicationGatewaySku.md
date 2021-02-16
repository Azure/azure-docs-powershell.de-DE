---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157057"
---
# <span data-ttu-id="38282-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="38282-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="38282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38282-102">SYNOPSIS</span></span>
<span data-ttu-id="38282-103">Ruft die SKU eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="38282-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="38282-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38282-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38282-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38282-105">DESCRIPTION</span></span>
<span data-ttu-id="38282-106">Das **Cmdlet "Get-AzApplicationGatewaySku"** ruft die SKU (Stock Keeping Unit) eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="38282-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="38282-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38282-107">EXAMPLES</span></span>

### <span data-ttu-id="38282-108">Beispiel 1: Erhalten einer Anwendungsgateway-SKU</span><span class="sxs-lookup"><span data-stu-id="38282-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="38282-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="38282-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="38282-110">Der zweite Befehl ruft die SKU eines Anwendungsgateways namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $SKU.</span><span class="sxs-lookup"><span data-stu-id="38282-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="38282-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38282-111">PARAMETERS</span></span>

### <span data-ttu-id="38282-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38282-112">-ApplicationGateway</span></span>
<span data-ttu-id="38282-113">Gibt das Anwendungsgatewayobjekt an.</span><span class="sxs-lookup"><span data-stu-id="38282-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="38282-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38282-114">-DefaultProfile</span></span>
<span data-ttu-id="38282-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38282-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38282-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38282-116">CommonParameters</span></span>
<span data-ttu-id="38282-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38282-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38282-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38282-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38282-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38282-119">INPUTS</span></span>

### <span data-ttu-id="38282-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38282-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38282-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38282-121">OUTPUTS</span></span>

### <span data-ttu-id="38282-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="38282-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="38282-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38282-123">NOTES</span></span>

## <span data-ttu-id="38282-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38282-124">RELATED LINKS</span></span>

[<span data-ttu-id="38282-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="38282-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="38282-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="38282-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


