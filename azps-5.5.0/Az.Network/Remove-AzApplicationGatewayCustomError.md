---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154204"
---
# <span data-ttu-id="8bcbe-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8bcbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcbe-103">Entfernt einen benutzerdefinierten Fehler von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="8bcbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bcbe-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bcbe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8bcbe-105">DESCRIPTION</span></span>
<span data-ttu-id="8bcbe-106">Das **Cmdlet "Remove-AzApplicationGatewayCustomError"** entfernt einen benutzerdefinierten Fehler von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="8bcbe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8bcbe-107">EXAMPLES</span></span>

### <span data-ttu-id="8bcbe-108">Beispiel 1: Entfernt benutzerdefinierten Fehler von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="8bcbe-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="8bcbe-109">Dieser Befehl entfernt den benutzerdefinierten Fehler des Http-Statuscodes 502 aus dem $appgw und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="8bcbe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bcbe-110">PARAMETERS</span></span>

### <span data-ttu-id="8bcbe-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bcbe-111">-ApplicationGateway</span></span>
<span data-ttu-id="8bcbe-112">Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="8bcbe-112">The Application Gateway</span></span>

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

### <span data-ttu-id="8bcbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcbe-113">-DefaultProfile</span></span>
<span data-ttu-id="8bcbe-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcbe-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8bcbe-115">-StatusCode</span></span>
<span data-ttu-id="8bcbe-116">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcbe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcbe-117">CommonParameters</span></span>
<span data-ttu-id="8bcbe-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcbe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcbe-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcbe-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcbe-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8bcbe-120">INPUTS</span></span>

### <span data-ttu-id="8bcbe-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8bcbe-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8bcbe-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8bcbe-122">OUTPUTS</span></span>

### <span data-ttu-id="8bcbe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8bcbe-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8bcbe-124">NOTES</span></span>

## <span data-ttu-id="8bcbe-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8bcbe-125">RELATED LINKS</span></span>

[<span data-ttu-id="8bcbe-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8bcbe-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8bcbe-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="8bcbe-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8bcbe-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
