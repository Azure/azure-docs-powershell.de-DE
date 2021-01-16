---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291898"
---
# <span data-ttu-id="f6654-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f6654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6654-102">SYNOPSIS</span></span>
<span data-ttu-id="f6654-103">Entfernt eine Umleitungskonfiguration von einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f6654-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f6654-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6654-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6654-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6654-105">DESCRIPTION</span></span>
<span data-ttu-id="f6654-106">Das **Cmdlet "Remove-AzApplicationGatewayRedirectConfiguration"** entfernt eine Umleitungskonfiguration von einem vorhandenen Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f6654-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="f6654-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6654-107">EXAMPLES</span></span>

### <span data-ttu-id="f6654-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6654-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="f6654-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="f6654-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f6654-110">Mit dem zweiten Befehl wird die Umleitungskonfiguration "Redirect01" aus dem Anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f6654-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f6654-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6654-111">PARAMETERS</span></span>

### <span data-ttu-id="f6654-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6654-112">-ApplicationGateway</span></span>
<span data-ttu-id="f6654-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6654-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f6654-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6654-114">-DefaultProfile</span></span>
<span data-ttu-id="f6654-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6654-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6654-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f6654-116">-Name</span></span>
<span data-ttu-id="f6654-117">Der Name der Umleitungskonfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="f6654-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6654-118">CommonParameters</span></span>
<span data-ttu-id="f6654-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6654-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6654-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6654-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6654-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6654-121">INPUTS</span></span>

### <span data-ttu-id="f6654-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6654-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6654-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6654-123">OUTPUTS</span></span>

### <span data-ttu-id="f6654-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6654-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6654-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6654-125">NOTES</span></span>

## <span data-ttu-id="f6654-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6654-126">RELATED LINKS</span></span>

[<span data-ttu-id="f6654-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6654-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6654-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="f6654-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6654-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
