---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381015"
---
# <span data-ttu-id="74d45-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="74d45-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="74d45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d45-102">SYNOPSIS</span></span>
<span data-ttu-id="74d45-103">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74d45-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="74d45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74d45-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74d45-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74d45-105">DESCRIPTION</span></span>
<span data-ttu-id="74d45-106">Zeigt den freigegebenen Schlüssel an, der für die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74d45-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="74d45-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74d45-107">EXAMPLES</span></span>

### <span data-ttu-id="74d45-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74d45-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="74d45-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74d45-109">PARAMETERS</span></span>

### <span data-ttu-id="74d45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d45-110">-DefaultProfile</span></span>
<span data-ttu-id="74d45-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74d45-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d45-112">-Name</span><span class="sxs-lookup"><span data-stu-id="74d45-112">-Name</span></span>
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

### <span data-ttu-id="74d45-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d45-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d45-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d45-114">CommonParameters</span></span>
<span data-ttu-id="74d45-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74d45-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d45-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74d45-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d45-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74d45-117">INPUTS</span></span>

### <span data-ttu-id="74d45-118">System.String</span><span class="sxs-lookup"><span data-stu-id="74d45-118">System.String</span></span>

## <span data-ttu-id="74d45-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74d45-119">OUTPUTS</span></span>

### <span data-ttu-id="74d45-120">System.String</span><span class="sxs-lookup"><span data-stu-id="74d45-120">System.String</span></span>

## <span data-ttu-id="74d45-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74d45-121">NOTES</span></span>

## <span data-ttu-id="74d45-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74d45-122">RELATED LINKS</span></span>

[<span data-ttu-id="74d45-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="74d45-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="74d45-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="74d45-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
