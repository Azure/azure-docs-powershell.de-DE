---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940328"
---
# <span data-ttu-id="bf860-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bf860-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bf860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf860-102">SYNOPSIS</span></span>
<span data-ttu-id="bf860-103">Ruft die SSL-Richtlinie eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="bf860-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="bf860-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf860-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf860-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf860-105">DESCRIPTION</span></span>
<span data-ttu-id="bf860-106">Das **Cmdlet Get-AzApplicationGatewaySslPolicy** ruft die SSL-Richtlinie eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="bf860-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="bf860-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf860-107">EXAMPLES</span></span>

### <span data-ttu-id="bf860-108">1:</span><span class="sxs-lookup"><span data-stu-id="bf860-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="bf860-109">Der erste Befehl ruft das Application Gateway mit dem Namen ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf860-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="bf860-110">Der zweite Befehl ruft die SSL-Richtlinie aus dem Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="bf860-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="bf860-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf860-111">PARAMETERS</span></span>

### <span data-ttu-id="bf860-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf860-112">-ApplicationGateway</span></span>
<span data-ttu-id="bf860-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="bf860-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bf860-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf860-114">-DefaultProfile</span></span>
<span data-ttu-id="bf860-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf860-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf860-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf860-116">CommonParameters</span></span>
<span data-ttu-id="bf860-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf860-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf860-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf860-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf860-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf860-119">INPUTS</span></span>

### <span data-ttu-id="bf860-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf860-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf860-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf860-121">OUTPUTS</span></span>

### <span data-ttu-id="bf860-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bf860-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="bf860-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf860-123">NOTES</span></span>
* <span data-ttu-id="bf860-124">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="bf860-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bf860-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf860-125">RELATED LINKS</span></span>

[<span data-ttu-id="bf860-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bf860-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="bf860-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="bf860-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


