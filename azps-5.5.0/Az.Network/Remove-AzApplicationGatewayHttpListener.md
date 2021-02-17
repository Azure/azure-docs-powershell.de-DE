---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159028"
---
# <span data-ttu-id="f29fb-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f29fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f29fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f29fb-103">Entfernt einen HTTP-Listener aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f29fb-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="f29fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f29fb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f29fb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f29fb-105">DESCRIPTION</span></span>
<span data-ttu-id="f29fb-106">Das **Cmdlet "Remove-AzApplicationGatewayHttpListener"** entfernt einen HTTP-Listener aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f29fb-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="f29fb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f29fb-107">EXAMPLES</span></span>

### <span data-ttu-id="f29fb-108">Beispiel 1: Entfernen eines HTTP-Listeners für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f29fb-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="f29fb-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="f29fb-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f29fb-110">Der zweite Befehl entfernt den HTTP-Listener mit dem Namen Listener02 aus dem Anwendungsgateway, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f29fb-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f29fb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f29fb-111">PARAMETERS</span></span>

### <span data-ttu-id="f29fb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f29fb-112">-ApplicationGateway</span></span>
<span data-ttu-id="f29fb-113">Gibt das Anwendungsgateway an, aus dem ein HTTP-Listener entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f29fb-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="f29fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29fb-114">-DefaultProfile</span></span>
<span data-ttu-id="f29fb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f29fb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f29fb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f29fb-116">-Name</span></span>
<span data-ttu-id="f29fb-117">Gibt den Namen des HTTP-Listeners an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="f29fb-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f29fb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29fb-118">CommonParameters</span></span>
<span data-ttu-id="f29fb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29fb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29fb-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f29fb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29fb-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f29fb-121">INPUTS</span></span>

### <span data-ttu-id="f29fb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f29fb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f29fb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f29fb-123">OUTPUTS</span></span>

### <span data-ttu-id="f29fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f29fb-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f29fb-125">NOTES</span></span>

## <span data-ttu-id="f29fb-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f29fb-126">RELATED LINKS</span></span>

[<span data-ttu-id="f29fb-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f29fb-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f29fb-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f29fb-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f29fb-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


