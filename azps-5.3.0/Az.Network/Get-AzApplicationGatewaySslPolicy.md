---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468172"
---
# <span data-ttu-id="d0c98-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c98-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d0c98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c98-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c98-103">Ruft die "SSL"-Richtlinie eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="d0c98-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="d0c98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0c98-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0c98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0c98-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c98-106">Das **Cmdlet "Get-AzApplicationGatewaySslPolicy"** ruft die "SSL-Richtlinie" eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="d0c98-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="d0c98-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0c98-107">EXAMPLES</span></span>

### <span data-ttu-id="d0c98-108">1:</span><span class="sxs-lookup"><span data-stu-id="d0c98-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="d0c98-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab und speichert das Ergebnis in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d0c98-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="d0c98-110">Der zweite Befehl ruft die ssl-Richtlinie vom Anwendungsgateway ab, das in der Variablen namens $AppGW.</span><span class="sxs-lookup"><span data-stu-id="d0c98-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="d0c98-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0c98-111">PARAMETERS</span></span>

### <span data-ttu-id="d0c98-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0c98-112">-ApplicationGateway</span></span>
<span data-ttu-id="d0c98-113">Gibt das Anwendungsgateway der SSL-Richtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d0c98-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0c98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c98-114">-DefaultProfile</span></span>
<span data-ttu-id="d0c98-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0c98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0c98-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c98-116">CommonParameters</span></span>
<span data-ttu-id="d0c98-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c98-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c98-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0c98-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c98-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0c98-119">INPUTS</span></span>

### <span data-ttu-id="d0c98-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0c98-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0c98-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0c98-121">OUTPUTS</span></span>

### <span data-ttu-id="d0c98-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c98-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d0c98-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0c98-123">NOTES</span></span>
* <span data-ttu-id="d0c98-124">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="d0c98-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d0c98-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0c98-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0c98-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c98-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="d0c98-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c98-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


