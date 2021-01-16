---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291143"
---
# <span data-ttu-id="390de-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="390de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="390de-102">SYNOPSIS</span></span>
<span data-ttu-id="390de-103">Ruft den Front-End-Port eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="390de-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="390de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="390de-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="390de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="390de-105">DESCRIPTION</span></span>
<span data-ttu-id="390de-106">Das **Cmdlet "Get-AzApplicationGatewayFrontendPort"** ruft den Front-End-Port eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="390de-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="390de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="390de-107">EXAMPLES</span></span>

### <span data-ttu-id="390de-108">Beispiel 1: Erhalten eines angegebenen Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="390de-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="390de-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="390de-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="390de-110">Der zweite Befehl ruft den Front-End-Port namens "FrontEndPort01" aus $AppGw und speichert ihn in der $FrontEndPort Variable.</span><span class="sxs-lookup"><span data-stu-id="390de-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="390de-111">Beispiel 2: Erhalten einer Liste der Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="390de-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="390de-112">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="390de-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="390de-113">Der zweite Befehl ruft eine Liste der Front-End-Ports von $AppGw und speichert sie in der $FrontEndPorts Variable.</span><span class="sxs-lookup"><span data-stu-id="390de-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="390de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="390de-114">PARAMETERS</span></span>

### <span data-ttu-id="390de-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="390de-115">-ApplicationGateway</span></span>
<span data-ttu-id="390de-116">Gibt das Anwendungsgatewayobjekt an, das den Front-End-Port enthält.</span><span class="sxs-lookup"><span data-stu-id="390de-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="390de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390de-117">-DefaultProfile</span></span>
<span data-ttu-id="390de-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="390de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="390de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="390de-119">-Name</span></span>
<span data-ttu-id="390de-120">Gibt den Namen des zu erhaltenden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="390de-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="390de-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390de-121">CommonParameters</span></span>
<span data-ttu-id="390de-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="390de-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390de-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="390de-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390de-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="390de-124">INPUTS</span></span>

### <span data-ttu-id="390de-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="390de-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="390de-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="390de-126">OUTPUTS</span></span>

### <span data-ttu-id="390de-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="390de-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="390de-128">NOTES</span></span>

## <span data-ttu-id="390de-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="390de-129">RELATED LINKS</span></span>

[<span data-ttu-id="390de-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="390de-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="390de-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="390de-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="390de-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


