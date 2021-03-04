---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: e134fafb8f7089b803b09a0202d3c43b0948f7ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920995"
---
# <span data-ttu-id="bb215-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb215-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="bb215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb215-102">SYNOPSIS</span></span>
<span data-ttu-id="bb215-103">Ändert einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bb215-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="bb215-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb215-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb215-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb215-105">DESCRIPTION</span></span>
<span data-ttu-id="bb215-106">Das **Cmdlet Set-AzApplicationGatewayFrontendPort** ändert einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="bb215-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="bb215-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bb215-107">EXAMPLES</span></span>

### <span data-ttu-id="bb215-108">Beispiel 1: Festlegen eines Front-End-Ports für ein Anwendungsgateway auf 80</span><span class="sxs-lookup"><span data-stu-id="bb215-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="bb215-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="bb215-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bb215-110">Der zweite Befehl ändert das Gateway in $AppGw, um Port 80 für den Front-End-Port namens FrontEndPort01 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb215-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="bb215-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bb215-111">PARAMETERS</span></span>

### <span data-ttu-id="bb215-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb215-112">-ApplicationGateway</span></span>
<span data-ttu-id="bb215-113">Gibt das Anwendungsgatewayobjekt an, dem dieses Cmdlet den Front-End-Port zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="bb215-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="bb215-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb215-114">-DefaultProfile</span></span>
<span data-ttu-id="bb215-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb215-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb215-116">-Name</span><span class="sxs-lookup"><span data-stu-id="bb215-116">-Name</span></span>
<span data-ttu-id="bb215-117">Gibt den Namen des zu ändernden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="bb215-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="bb215-118">-Port</span><span class="sxs-lookup"><span data-stu-id="bb215-118">-Port</span></span>
<span data-ttu-id="bb215-119">Gibt die Portnummer an, die für den Front-End-Port verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb215-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb215-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb215-120">CommonParameters</span></span>
<span data-ttu-id="bb215-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb215-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb215-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb215-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb215-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bb215-123">INPUTS</span></span>

### <span data-ttu-id="bb215-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb215-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb215-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bb215-125">OUTPUTS</span></span>

### <span data-ttu-id="bb215-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb215-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb215-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bb215-127">NOTES</span></span>

## <span data-ttu-id="bb215-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bb215-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb215-129">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb215-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="bb215-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb215-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="bb215-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb215-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="bb215-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="bb215-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
