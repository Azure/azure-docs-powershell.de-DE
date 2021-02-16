---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157073"
---
# <span data-ttu-id="123f3-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="123f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="123f3-102">SYNOPSIS</span></span>
<span data-ttu-id="123f3-103">Ruft benutzerdefinierte Fehler von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="123f3-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="123f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="123f3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="123f3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="123f3-105">DESCRIPTION</span></span>
<span data-ttu-id="123f3-106">Das **Cmdlet "Get-AzApplicationGatewayCustomError"** ruft benutzerdefinierte Fehler von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="123f3-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="123f3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="123f3-107">EXAMPLES</span></span>

### <span data-ttu-id="123f3-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Anwendungsgateway ab</span><span class="sxs-lookup"><span data-stu-id="123f3-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="123f3-109">Dieser Befehl ruft den benutzerdefinierten Fehler des Http-Statuscodes 502 vom Anwendungsgateway auf und gibt $appgw.</span><span class="sxs-lookup"><span data-stu-id="123f3-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="123f3-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="123f3-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="123f3-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler vom Anwendungsgateway auf dem Server ab und $appgw.</span><span class="sxs-lookup"><span data-stu-id="123f3-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="123f3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="123f3-112">PARAMETERS</span></span>

### <span data-ttu-id="123f3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123f3-113">-ApplicationGateway</span></span>
<span data-ttu-id="123f3-114">Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="123f3-114">The Application Gateway</span></span>

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

### <span data-ttu-id="123f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123f3-115">-DefaultProfile</span></span>
<span data-ttu-id="123f3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="123f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="123f3-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="123f3-117">-StatusCode</span></span>
<span data-ttu-id="123f3-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="123f3-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123f3-119">CommonParameters</span></span>
<span data-ttu-id="123f3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="123f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123f3-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="123f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123f3-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="123f3-122">INPUTS</span></span>

### <span data-ttu-id="123f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="123f3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="123f3-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="123f3-124">OUTPUTS</span></span>

### <span data-ttu-id="123f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="123f3-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="123f3-126">NOTES</span></span>

## <span data-ttu-id="123f3-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="123f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="123f3-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="123f3-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="123f3-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="123f3-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="123f3-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
