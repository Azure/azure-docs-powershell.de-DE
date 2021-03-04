---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944026"
---
# <span data-ttu-id="42d5b-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="42d5b-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="42d5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="42d5b-103">Holen Sie sich die dem Anwendungsgateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="42d5b-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="42d5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42d5b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d5b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42d5b-105">DESCRIPTION</span></span>
<span data-ttu-id="42d5b-106">Das **Get-AzApplicationGatewayIdentity-Cmdlet** ruft dem Anwendungsgateway die Dem Anwendungsgateway zugewiesene Identität ab.</span><span class="sxs-lookup"><span data-stu-id="42d5b-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="42d5b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42d5b-107">EXAMPLES</span></span>

### <span data-ttu-id="42d5b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42d5b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="42d5b-109">In diesen Beispielen wird gezeigt, wie Sie die Anwendungsgatewayidentität aus dem Anwendungsgateway erhalten.</span><span class="sxs-lookup"><span data-stu-id="42d5b-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="42d5b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42d5b-110">PARAMETERS</span></span>

### <span data-ttu-id="42d5b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42d5b-111">-ApplicationGateway</span></span>
<span data-ttu-id="42d5b-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42d5b-112">The applicationGateway</span></span>

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

### <span data-ttu-id="42d5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d5b-113">-DefaultProfile</span></span>
<span data-ttu-id="42d5b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42d5b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d5b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d5b-115">CommonParameters</span></span>
<span data-ttu-id="42d5b-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d5b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d5b-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42d5b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d5b-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42d5b-118">INPUTS</span></span>

### <span data-ttu-id="42d5b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42d5b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42d5b-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42d5b-120">OUTPUTS</span></span>

### <span data-ttu-id="42d5b-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="42d5b-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="42d5b-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="42d5b-122">NOTES</span></span>

## <span data-ttu-id="42d5b-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="42d5b-123">RELATED LINKS</span></span>
