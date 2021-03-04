---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: a0e8cbdb9ec64d4f65b859f70c1a1bb7f843132b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941755"
---
# <span data-ttu-id="50bb6-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="50bb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50bb6-102">SYNOPSIS</span></span>
<span data-ttu-id="50bb6-103">Ruft den Front-End-Port eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="50bb6-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="50bb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50bb6-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50bb6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50bb6-105">DESCRIPTION</span></span>
<span data-ttu-id="50bb6-106">Das **Get-AzApplicationGatewayFrontendPort-Cmdlet** ruft den Front-End-Port eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="50bb6-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="50bb6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="50bb6-107">EXAMPLES</span></span>

### <span data-ttu-id="50bb6-108">Beispiel 1: Erhalten eines angegebenen Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="50bb6-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="50bb6-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="50bb6-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50bb6-110">Der zweite Befehl ruft den Front-End-Port namens FrontEndPort01 von $AppGw ab und speichert ihn in der $FrontEndPort Variablen.</span><span class="sxs-lookup"><span data-stu-id="50bb6-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="50bb6-111">Beispiel 2: Erhalten einer Liste der Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="50bb6-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="50bb6-112">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="50bb6-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50bb6-113">Der zweite Befehl ruft eine Liste der Front-End-Ports aus $AppGw ab und speichert sie in der $FrontEndPorts Variablen.</span><span class="sxs-lookup"><span data-stu-id="50bb6-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="50bb6-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="50bb6-114">PARAMETERS</span></span>

### <span data-ttu-id="50bb6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50bb6-115">-ApplicationGateway</span></span>
<span data-ttu-id="50bb6-116">Gibt das Anwendungsgatewayobjekt an, das den Front-End-Port enthält.</span><span class="sxs-lookup"><span data-stu-id="50bb6-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="50bb6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bb6-117">-DefaultProfile</span></span>
<span data-ttu-id="50bb6-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50bb6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50bb6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="50bb6-119">-Name</span></span>
<span data-ttu-id="50bb6-120">Gibt den Namen des zu erhaltenden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="50bb6-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="50bb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bb6-121">CommonParameters</span></span>
<span data-ttu-id="50bb6-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bb6-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50bb6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bb6-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="50bb6-124">INPUTS</span></span>

### <span data-ttu-id="50bb6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50bb6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50bb6-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="50bb6-126">OUTPUTS</span></span>

### <span data-ttu-id="50bb6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="50bb6-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="50bb6-128">NOTES</span></span>

## <span data-ttu-id="50bb6-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="50bb6-129">RELATED LINKS</span></span>

[<span data-ttu-id="50bb6-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50bb6-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50bb6-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50bb6-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50bb6-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


