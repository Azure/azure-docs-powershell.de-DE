---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 459880d6ab771e48a9fe2d5ba69abffae35db7b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941771"
---
# <span data-ttu-id="40546-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="40546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40546-102">SYNOPSIS</span></span>
<span data-ttu-id="40546-103">Ruft benutzerdefinierte Fehler von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="40546-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="40546-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40546-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40546-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40546-105">DESCRIPTION</span></span>
<span data-ttu-id="40546-106">Das **Cmdlet Get-AzApplicationGatewayCustomError** ruft benutzerdefinierte Fehler von einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="40546-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="40546-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40546-107">EXAMPLES</span></span>

### <span data-ttu-id="40546-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem Anwendungsgateway ab</span><span class="sxs-lookup"><span data-stu-id="40546-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="40546-109">Dieser Befehl ruft den benutzerdefinierten Fehler von http-Statuscode 502 aus dem Anwendungsgateway ab und gibt $appgw.</span><span class="sxs-lookup"><span data-stu-id="40546-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="40546-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="40546-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="40546-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem Anwendungsgateway ab und gibt $appgw.</span><span class="sxs-lookup"><span data-stu-id="40546-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="40546-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="40546-112">PARAMETERS</span></span>

### <span data-ttu-id="40546-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40546-113">-ApplicationGateway</span></span>
<span data-ttu-id="40546-114">Das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="40546-114">The Application Gateway</span></span>

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

### <span data-ttu-id="40546-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40546-115">-DefaultProfile</span></span>
<span data-ttu-id="40546-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40546-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40546-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="40546-117">-StatusCode</span></span>
<span data-ttu-id="40546-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="40546-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="40546-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40546-119">CommonParameters</span></span>
<span data-ttu-id="40546-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40546-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40546-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40546-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40546-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40546-122">INPUTS</span></span>

### <span data-ttu-id="40546-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40546-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40546-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40546-124">OUTPUTS</span></span>

### <span data-ttu-id="40546-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="40546-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="40546-126">NOTES</span></span>

## <span data-ttu-id="40546-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="40546-127">RELATED LINKS</span></span>

[<span data-ttu-id="40546-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="40546-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="40546-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="40546-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="40546-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
