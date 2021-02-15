---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151561"
---
# <span data-ttu-id="bb10d-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="bb10d-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="bb10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb10d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb10d-103">Entfernt eine Identität von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bb10d-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="bb10d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb10d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb10d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb10d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb10d-106">**Mit dem Cmdlet "Remove-AzApplicationGatewayIdentity"** wird die Identität von einem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb10d-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="bb10d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb10d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb10d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bb10d-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="bb10d-109">In diesem Beispiel wird die Identität von einem vorhandenen Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="bb10d-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="bb10d-110">Hinweis: Wenn das Gateway auf einen geheimen Schlüsselverweis verweist, ist es auch wichtig, diese Ssl-Zertifikatverweise zusammen mit diesem Vorgang zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="bb10d-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="bb10d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb10d-111">PARAMETERS</span></span>

### <span data-ttu-id="bb10d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb10d-112">-ApplicationGateway</span></span>
<span data-ttu-id="bb10d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb10d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="bb10d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb10d-114">-DefaultProfile</span></span>
<span data-ttu-id="bb10d-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb10d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb10d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb10d-116">-Confirm</span></span>
<span data-ttu-id="bb10d-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb10d-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb10d-118">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bb10d-118">-WhatIf</span></span>
<span data-ttu-id="bb10d-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bb10d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb10d-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bb10d-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb10d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb10d-121">CommonParameters</span></span>
<span data-ttu-id="bb10d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb10d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb10d-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb10d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb10d-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb10d-124">INPUTS</span></span>

### <span data-ttu-id="bb10d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb10d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb10d-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb10d-126">OUTPUTS</span></span>

### <span data-ttu-id="bb10d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb10d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb10d-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bb10d-128">NOTES</span></span>

## <span data-ttu-id="bb10d-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bb10d-129">RELATED LINKS</span></span>
