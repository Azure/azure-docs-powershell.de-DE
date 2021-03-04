---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 7d4cce44aa76628011b35d6723b1ae34a869a2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936720"
---
# <span data-ttu-id="f65d7-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f65d7-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f65d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f65d7-102">SYNOPSIS</span></span>
<span data-ttu-id="f65d7-103">Entfernt eine Identität aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f65d7-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="f65d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f65d7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f65d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f65d7-105">DESCRIPTION</span></span>
<span data-ttu-id="f65d7-106">**Das Cmdlet Remove-AzApplicationGatewayIdentity** entfernt die Identität aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f65d7-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="f65d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f65d7-107">EXAMPLES</span></span>

### <span data-ttu-id="f65d7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f65d7-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="f65d7-109">In diesem Beispiel wird die Identität aus einem vorhandenen Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="f65d7-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="f65d7-110">Hinweis: Wenn das Gateway auf einen Schlüsselvaultschlüssel verweist, ist es auch wichtig, diese Sslzertifikatverweise entlang dieses Vorgangs zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f65d7-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="f65d7-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f65d7-111">PARAMETERS</span></span>

### <span data-ttu-id="f65d7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f65d7-112">-ApplicationGateway</span></span>
<span data-ttu-id="f65d7-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f65d7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f65d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65d7-114">-DefaultProfile</span></span>
<span data-ttu-id="f65d7-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f65d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f65d7-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f65d7-116">-Confirm</span></span>
<span data-ttu-id="f65d7-117">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f65d7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f65d7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f65d7-118">-WhatIf</span></span>
<span data-ttu-id="f65d7-119">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f65d7-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f65d7-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f65d7-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f65d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65d7-121">CommonParameters</span></span>
<span data-ttu-id="f65d7-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65d7-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65d7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65d7-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f65d7-124">INPUTS</span></span>

### <span data-ttu-id="f65d7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f65d7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f65d7-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f65d7-126">OUTPUTS</span></span>

### <span data-ttu-id="f65d7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f65d7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f65d7-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f65d7-128">NOTES</span></span>

## <span data-ttu-id="f65d7-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f65d7-129">RELATED LINKS</span></span>
