---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172921"
---
# <span data-ttu-id="faf7c-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="faf7c-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="faf7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf7c-102">SYNOPSIS</span></span>
<span data-ttu-id="faf7c-103">Sie erhalten die dem Anwendungsgateway zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="faf7c-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="faf7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="faf7c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf7c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="faf7c-105">DESCRIPTION</span></span>
<span data-ttu-id="faf7c-106">Das **Cmdlet "Get-AzApplicationGatewayIdentity"** wird dem Anwendungsgateway zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="faf7c-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="faf7c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="faf7c-107">EXAMPLES</span></span>

### <span data-ttu-id="faf7c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faf7c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="faf7c-109">In diesen Beispielen wird veranschaulicht, wie Sie die Anwendungsgatewayidentität vom Anwendungsgateway erhalten.</span><span class="sxs-lookup"><span data-stu-id="faf7c-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="faf7c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faf7c-110">PARAMETERS</span></span>

### <span data-ttu-id="faf7c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faf7c-111">-ApplicationGateway</span></span>
<span data-ttu-id="faf7c-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faf7c-112">The applicationGateway</span></span>

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

### <span data-ttu-id="faf7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf7c-113">-DefaultProfile</span></span>
<span data-ttu-id="faf7c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="faf7c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf7c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf7c-115">CommonParameters</span></span>
<span data-ttu-id="faf7c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf7c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf7c-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faf7c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf7c-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="faf7c-118">INPUTS</span></span>

### <span data-ttu-id="faf7c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="faf7c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="faf7c-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="faf7c-120">OUTPUTS</span></span>

### <span data-ttu-id="faf7c-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="faf7c-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="faf7c-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="faf7c-122">NOTES</span></span>

## <span data-ttu-id="faf7c-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="faf7c-123">RELATED LINKS</span></span>
