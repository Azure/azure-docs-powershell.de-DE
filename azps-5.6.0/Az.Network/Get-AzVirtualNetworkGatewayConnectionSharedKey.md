---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 14a77eeaeb502c79663f9d95cbff3ffc199ddc67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930019"
---
# <span data-ttu-id="20e14-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20e14-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="20e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20e14-102">SYNOPSIS</span></span>
<span data-ttu-id="20e14-103">Zeigt den für die Verbindung verwendeten freigegebenen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="20e14-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="20e14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20e14-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20e14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20e14-105">DESCRIPTION</span></span>
<span data-ttu-id="20e14-106">Zeigt den für die Verbindung verwendeten freigegebenen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="20e14-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="20e14-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20e14-107">EXAMPLES</span></span>

### <span data-ttu-id="20e14-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20e14-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="20e14-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20e14-109">PARAMETERS</span></span>

### <span data-ttu-id="20e14-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e14-110">-DefaultProfile</span></span>
<span data-ttu-id="20e14-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20e14-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20e14-112">-Name</span><span class="sxs-lookup"><span data-stu-id="20e14-112">-Name</span></span>
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

### <span data-ttu-id="20e14-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e14-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="20e14-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e14-114">CommonParameters</span></span>
<span data-ttu-id="20e14-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e14-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e14-116">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20e14-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e14-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20e14-117">INPUTS</span></span>

### <span data-ttu-id="20e14-118">System.String</span><span class="sxs-lookup"><span data-stu-id="20e14-118">System.String</span></span>

## <span data-ttu-id="20e14-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20e14-119">OUTPUTS</span></span>

### <span data-ttu-id="20e14-120">System.String</span><span class="sxs-lookup"><span data-stu-id="20e14-120">System.String</span></span>

## <span data-ttu-id="20e14-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20e14-121">NOTES</span></span>

## <span data-ttu-id="20e14-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20e14-122">RELATED LINKS</span></span>

[<span data-ttu-id="20e14-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20e14-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="20e14-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20e14-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
