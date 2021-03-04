---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941752"
---
# <span data-ttu-id="1871f-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1871f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1871f-102">SYNOPSIS</span></span>
<span data-ttu-id="1871f-103">Ruft den HTTP-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="1871f-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="1871f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1871f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1871f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1871f-105">DESCRIPTION</span></span>
<span data-ttu-id="1871f-106">Das **Get-AzApplicationGatewayHttpListener-Cmdlet** ruft den HTTP-Listener eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="1871f-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="1871f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1871f-107">EXAMPLES</span></span>

### <span data-ttu-id="1871f-108">Beispiel 1: Einen bestimmten HTTP-Listener erhalten</span><span class="sxs-lookup"><span data-stu-id="1871f-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="1871f-109">Dieser Befehl ruft einen HTTP-Listener namens Listener01 ab.</span><span class="sxs-lookup"><span data-stu-id="1871f-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="1871f-110">Beispiel 2: Erhalten einer Liste von HTTP-Listenern</span><span class="sxs-lookup"><span data-stu-id="1871f-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="1871f-111">Dieser Befehl ruft eine Liste der HTTP-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="1871f-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="1871f-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1871f-112">PARAMETERS</span></span>

### <span data-ttu-id="1871f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1871f-113">-ApplicationGateway</span></span>
<span data-ttu-id="1871f-114">Gibt das Anwendungsgatewayobjekt an, das den HTTP-Listener enthält.</span><span class="sxs-lookup"><span data-stu-id="1871f-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="1871f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1871f-115">-DefaultProfile</span></span>
<span data-ttu-id="1871f-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1871f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1871f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1871f-117">-Name</span></span>
<span data-ttu-id="1871f-118">Gibt den Namen des HTTP-Listeners an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1871f-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="1871f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1871f-119">CommonParameters</span></span>
<span data-ttu-id="1871f-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1871f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1871f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1871f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1871f-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1871f-122">INPUTS</span></span>

### <span data-ttu-id="1871f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1871f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1871f-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1871f-124">OUTPUTS</span></span>

### <span data-ttu-id="1871f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1871f-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1871f-126">NOTES</span></span>

## <span data-ttu-id="1871f-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1871f-127">RELATED LINKS</span></span>

[<span data-ttu-id="1871f-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1871f-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1871f-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1871f-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1871f-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


