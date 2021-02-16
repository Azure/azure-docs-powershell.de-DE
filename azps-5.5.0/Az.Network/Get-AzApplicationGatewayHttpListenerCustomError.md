---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 34f92bfa7566679c4cee9f7a4281ac15c55676b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152009"
---
# <span data-ttu-id="52749-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="52749-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="52749-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52749-102">SYNOPSIS</span></span>
<span data-ttu-id="52749-103">Ruft benutzerdefinierte Fehler aus einem http-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="52749-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="52749-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52749-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52749-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52749-105">DESCRIPTION</span></span>
<span data-ttu-id="52749-106">Das **Cmdlet "Get-AzApplicationGatewayCustomError"** ruft benutzerdefinierte Fehler aus einem http-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="52749-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="52749-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="52749-107">EXAMPLES</span></span>

### <span data-ttu-id="52749-108">Beispiel 1: Ruft einen benutzerdefinierten Fehler in einem http-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="52749-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="52749-109">Dieser Befehl ruft den benutzerdefinierten Fehler des Http-Statuscodes 502 aus dem http-Listener-$listener 01 ab und gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="52749-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="52749-110">Beispiel 2: Ruft die Liste aller benutzerdefinierten Fehler in einem Http-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="52749-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="52749-111">Dieser Befehl ruft die Liste aller benutzerdefinierten Fehler aus dem http-Listener-$listener 01 ab und gibt sie zurück.</span><span class="sxs-lookup"><span data-stu-id="52749-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="52749-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52749-112">PARAMETERS</span></span>

### <span data-ttu-id="52749-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52749-113">-DefaultProfile</span></span>
<span data-ttu-id="52749-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52749-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52749-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="52749-115">-HttpListener</span></span>
<span data-ttu-id="52749-116">Der Http-Listener für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="52749-116">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52749-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="52749-117">-StatusCode</span></span>
<span data-ttu-id="52749-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="52749-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="52749-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52749-119">CommonParameters</span></span>
<span data-ttu-id="52749-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52749-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52749-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52749-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52749-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="52749-122">INPUTS</span></span>

### <span data-ttu-id="52749-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52749-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="52749-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="52749-124">OUTPUTS</span></span>

### <span data-ttu-id="52749-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="52749-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="52749-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="52749-126">NOTES</span></span>

## <span data-ttu-id="52749-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="52749-127">RELATED LINKS</span></span>

[<span data-ttu-id="52749-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="52749-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="52749-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="52749-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="52749-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="52749-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
