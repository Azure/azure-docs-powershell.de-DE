---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: fe21bc83fce1e43e036f68ea64c8a10cf2f3c90e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146785"
---
# <span data-ttu-id="12ec5-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="12ec5-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="12ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="12ec5-103">Entfernt einen Front-End-Port von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="12ec5-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="12ec5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12ec5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ec5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="12ec5-106">Das **Cmdlet "Remove-AzApplicationGatewayFrontendPort"** entfernt einen Front-End-Port von einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="12ec5-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="12ec5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="12ec5-108">Beispiel: Entfernen eines Front-End-Ports von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="12ec5-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="12ec5-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört und das Gateway in einer $AppGw speichert.</span><span class="sxs-lookup"><span data-stu-id="12ec5-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="12ec5-110">Der zweite Befehl entfernt den Port namens "FrontEndPort02" vom Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="12ec5-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="12ec5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12ec5-111">PARAMETERS</span></span>

### <span data-ttu-id="12ec5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12ec5-112">-ApplicationGateway</span></span>
<span data-ttu-id="12ec5-113">Gibt das Anwendungsgateway an, von dem ein Front-End-Port entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12ec5-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="12ec5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ec5-114">-DefaultProfile</span></span>
<span data-ttu-id="12ec5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12ec5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12ec5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="12ec5-116">-Name</span></span>
<span data-ttu-id="12ec5-117">Gibt den Namen des zu entfernenden Frontendports an.</span><span class="sxs-lookup"><span data-stu-id="12ec5-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="12ec5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ec5-118">CommonParameters</span></span>
<span data-ttu-id="12ec5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ec5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ec5-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ec5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ec5-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12ec5-121">INPUTS</span></span>

### <span data-ttu-id="12ec5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12ec5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12ec5-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12ec5-123">OUTPUTS</span></span>

### <span data-ttu-id="12ec5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12ec5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12ec5-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12ec5-125">NOTES</span></span>

## <span data-ttu-id="12ec5-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12ec5-126">RELATED LINKS</span></span>

[<span data-ttu-id="12ec5-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="12ec5-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="12ec5-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="12ec5-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="12ec5-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="12ec5-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="12ec5-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="12ec5-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


