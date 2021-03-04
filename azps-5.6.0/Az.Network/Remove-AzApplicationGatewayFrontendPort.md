---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 4b28feb85ebc8f4d5669f28609aa4723061c1709
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939464"
---
# <span data-ttu-id="8e63b-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e63b-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="8e63b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e63b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e63b-103">Entfernt einen Front-End-Port aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8e63b-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="8e63b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e63b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e63b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e63b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e63b-106">Das **Cmdlet Remove-AzApplicationGatewayFrontendPort** entfernt einen Front-End-Port aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8e63b-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="8e63b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e63b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e63b-108">Beispiel: Entfernen eines Front-End-Ports aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="8e63b-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="8e63b-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört und das Gateway in einer $AppGw speichert.</span><span class="sxs-lookup"><span data-stu-id="8e63b-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="8e63b-110">Der zweite Befehl entfernt den Port mit dem Namen FrontEndPort02 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="8e63b-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="8e63b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e63b-111">PARAMETERS</span></span>

### <span data-ttu-id="8e63b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e63b-112">-ApplicationGateway</span></span>
<span data-ttu-id="8e63b-113">Gibt das Anwendungsgateway an, aus dem ein Front-End-Port entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e63b-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="8e63b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e63b-114">-DefaultProfile</span></span>
<span data-ttu-id="8e63b-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e63b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e63b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8e63b-116">-Name</span></span>
<span data-ttu-id="8e63b-117">Gibt den Namen des zu entfernenden Frontendports an.</span><span class="sxs-lookup"><span data-stu-id="8e63b-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="8e63b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e63b-118">CommonParameters</span></span>
<span data-ttu-id="8e63b-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e63b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e63b-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e63b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e63b-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-121">INPUTS</span></span>

### <span data-ttu-id="8e63b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e63b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e63b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-123">OUTPUTS</span></span>

### <span data-ttu-id="8e63b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e63b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e63b-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e63b-125">NOTES</span></span>

## <span data-ttu-id="8e63b-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e63b-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e63b-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e63b-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8e63b-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e63b-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8e63b-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e63b-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="8e63b-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e63b-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


