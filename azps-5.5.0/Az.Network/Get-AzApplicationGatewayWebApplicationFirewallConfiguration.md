---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170027"
---
# <span data-ttu-id="d062a-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d062a-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d062a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d062a-102">SYNOPSIS</span></span>
<span data-ttu-id="d062a-103">Ruft die WAF-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="d062a-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="d062a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d062a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d062a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d062a-105">DESCRIPTION</span></span>
<span data-ttu-id="d062a-106">Das **Cmdlet "Get-AzApplicationGatewayWebApplicationFirewallConfiguration"** ruft die Web Application Firewall (WAF)-Konfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="d062a-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="d062a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d062a-107">EXAMPLES</span></span>

### <span data-ttu-id="d062a-108">Beispiel 1: Firewallkonfiguration eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="d062a-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="d062a-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert es dann in der $AppGW Variable.</span><span class="sxs-lookup"><span data-stu-id="d062a-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="d062a-110">Der zweite Befehl ruft die Firewallkonfiguration des Anwendungsgateways in $AppGW und speichert sie dann in $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="d062a-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="d062a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d062a-111">PARAMETERS</span></span>

### <span data-ttu-id="d062a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d062a-112">-ApplicationGateway</span></span>
<span data-ttu-id="d062a-113">Gibt ein Anwendungsgatewayobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d062a-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="d062a-114">Sie können das cmdlet Get-AzApplicationGateway verwenden, um ein Anwendungsgatewayobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d062a-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="d062a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d062a-115">-DefaultProfile</span></span>
<span data-ttu-id="d062a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d062a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d062a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d062a-117">CommonParameters</span></span>
<span data-ttu-id="d062a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d062a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d062a-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d062a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d062a-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d062a-120">INPUTS</span></span>

### <span data-ttu-id="d062a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d062a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d062a-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d062a-122">OUTPUTS</span></span>

### <span data-ttu-id="d062a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d062a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d062a-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d062a-124">NOTES</span></span>

## <span data-ttu-id="d062a-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d062a-125">RELATED LINKS</span></span>

[<span data-ttu-id="d062a-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d062a-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d062a-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d062a-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d062a-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d062a-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


