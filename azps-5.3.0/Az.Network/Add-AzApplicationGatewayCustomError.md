---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: e3bac58fca1c405aeef3366cb3ec1ee1b01a0891
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380356"
---
# <span data-ttu-id="bbaa3-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bbaa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbaa3-103">Fügt einem Anwendungsgateway einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="bbaa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbaa3-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbaa3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="bbaa3-106">Das **Cmdlet "Add-AzApplicationGatewayCustomError"** fügt einem Anwendungsgateway einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="bbaa3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bbaa3-107">EXAMPLES</span></span>

### <span data-ttu-id="bbaa3-108">Beispiel 1: Fügt der Ebene des Anwendungsgateways einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $resourceGroupName = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroup $resourceGroupName
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $AppGw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="bbaa3-109">Dieser Befehl fügt dem Anwendungsgateway den benutzerdefinierten Fehler "http-Statuscode 502" $appgw und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="bbaa3-110">Beispiel 2: Fügt der Listenerebene des Anwendungsgateways einen benutzerdefinierten Fehler hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
 $resourceGroupName = "resourceGroupName"
 $AppGWName = "applicationGatewayName"
 $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
 $listenerName = "listenerName"
 $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $resourceGroupName
 $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
 $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
 Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="bbaa3-111">Mit diesem Befehl wird dem Anwendungsgateway auf der Listenerebene ein benutzerdefinierter Fehler mit dem Http-Statuscode 502 $appgw und das aktualisierte Gateway zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="bbaa3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbaa3-112">PARAMETERS</span></span>

### <span data-ttu-id="bbaa3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbaa3-113">-ApplicationGateway</span></span>
<span data-ttu-id="bbaa3-114">Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="bbaa3-114">The Application Gateway</span></span>

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

### <span data-ttu-id="bbaa3-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="bbaa3-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="bbaa3-116">Fehlerseiten-URL des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bbaa3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbaa3-117">-DefaultProfile</span></span>
<span data-ttu-id="bbaa3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbaa3-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bbaa3-119">-StatusCode</span></span>
<span data-ttu-id="bbaa3-120">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bbaa3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbaa3-121">CommonParameters</span></span>
<span data-ttu-id="bbaa3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbaa3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbaa3-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbaa3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbaa3-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bbaa3-124">INPUTS</span></span>

### <span data-ttu-id="bbaa3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bbaa3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bbaa3-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bbaa3-126">OUTPUTS</span></span>

### <span data-ttu-id="bbaa3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bbaa3-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bbaa3-128">NOTES</span></span>

## <span data-ttu-id="bbaa3-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bbaa3-129">RELATED LINKS</span></span>

[<span data-ttu-id="bbaa3-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bbaa3-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bbaa3-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bbaa3-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bbaa3-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
