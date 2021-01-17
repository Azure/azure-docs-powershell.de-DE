---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473500"
---
# <span data-ttu-id="1e0a2-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1e0a2-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="1e0a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0a2-103">Ruft eine Firewallrichtlinie für das Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="1e0a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e0a2-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e0a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e0a2-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0a2-106">Das **Cmdlet "Get-AzApplicationGatewayFirewallPolicy"** ruft eine Firewallrichtlinie für das Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="1e0a2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e0a2-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0a2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e0a2-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1e0a2-109">Dieser Befehl ruft die Firewallrichtlinie des Anwendungsgateways namens "FirewallPolicy1" ab, die zur Ressourcengruppe "ResourceGroup01" gehört, und speichert sie in der $AppGwFirewallPolicy Variable.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="1e0a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e0a2-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0a2-111">-DefaultProfile</span></span>
<span data-ttu-id="1e0a2-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e0a2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1e0a2-113">-Name</span></span>
<span data-ttu-id="1e0a2-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e0a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="1e0a2-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0a2-117">CommonParameters</span></span>
<span data-ttu-id="1e0a2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0a2-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e0a2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0a2-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e0a2-120">INPUTS</span></span>

### <span data-ttu-id="1e0a2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1e0a2-121">System.String</span></span>

## <span data-ttu-id="1e0a2-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e0a2-122">OUTPUTS</span></span>

### <span data-ttu-id="1e0a2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1e0a2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="1e0a2-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e0a2-124">NOTES</span></span>

## <span data-ttu-id="1e0a2-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e0a2-125">RELATED LINKS</span></span>
