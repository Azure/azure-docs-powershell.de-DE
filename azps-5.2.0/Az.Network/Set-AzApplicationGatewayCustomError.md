---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370935"
---
# <span data-ttu-id="e1790-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e1790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1790-102">SYNOPSIS</span></span>
<span data-ttu-id="e1790-103">Aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e1790-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="e1790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1790-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1790-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1790-105">DESCRIPTION</span></span>
<span data-ttu-id="e1790-106">Das **Cmdlet "Set-AzApplicationGatewayCustomError"** aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e1790-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="e1790-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1790-107">EXAMPLES</span></span>

### <span data-ttu-id="e1790-108">Beispiel 1: Aktualisieren eines benutzerdefinierten Fehlers in einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e1790-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e1790-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des Http-Statuscodes 502 im Anwendungsgateway $appgw aktualisiert und das aktualisierte Gateway zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e1790-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="e1790-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1790-110">PARAMETERS</span></span>

### <span data-ttu-id="e1790-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1790-111">-ApplicationGateway</span></span>
<span data-ttu-id="e1790-112">Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e1790-112">The Application Gateway</span></span>

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

### <span data-ttu-id="e1790-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e1790-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e1790-114">Fehlerseiten-URL des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="e1790-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e1790-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1790-115">-DefaultProfile</span></span>
<span data-ttu-id="e1790-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1790-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1790-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e1790-117">-StatusCode</span></span>
<span data-ttu-id="e1790-118">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="e1790-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e1790-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1790-119">CommonParameters</span></span>
<span data-ttu-id="e1790-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1790-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1790-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1790-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1790-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1790-122">INPUTS</span></span>

### <span data-ttu-id="e1790-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1790-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1790-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1790-124">OUTPUTS</span></span>

### <span data-ttu-id="e1790-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e1790-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1790-126">NOTES</span></span>

## <span data-ttu-id="e1790-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1790-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1790-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e1790-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e1790-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e1790-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e1790-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
