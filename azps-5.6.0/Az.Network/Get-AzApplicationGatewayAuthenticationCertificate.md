---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 7f5dbd73158e5328ece78b1064a78ff5c4627035
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924016"
---
# <span data-ttu-id="3eccb-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3eccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eccb-102">SYNOPSIS</span></span>
<span data-ttu-id="3eccb-103">Ruft ein Authentifizierungszertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="3eccb-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="3eccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eccb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eccb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eccb-105">DESCRIPTION</span></span>
<span data-ttu-id="3eccb-106">Das **Cmdlet Get-AzApplicationGatewayAuthenticationCertificate** erhält ein Authentifizierungszertifikat für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3eccb-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="3eccb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3eccb-107">EXAMPLES</span></span>

### <span data-ttu-id="3eccb-108">Beispiel 1: Erhalten eines angegebenen Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="3eccb-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $cert = Get-AzApplicationGatewayAuthenticationCertificate -Name "cert01" -ApplicationGateway $appgw
```

<span data-ttu-id="3eccb-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen "appGwName" ab und speichert es in der $appgw-Variable.</span><span class="sxs-lookup"><span data-stu-id="3eccb-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="3eccb-110">Der zweite Befehl ruft das Authentifizierungszertifikat mit dem Namen cert01 ab und speichert es in der $cert-Variable.</span><span class="sxs-lookup"><span data-stu-id="3eccb-110">The second command gets the authentication certificate named cert01 and stores it in the $cert variable.</span></span>

## <span data-ttu-id="3eccb-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3eccb-111">PARAMETERS</span></span>

### <span data-ttu-id="3eccb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3eccb-112">-ApplicationGateway</span></span>
<span data-ttu-id="3eccb-113">Gibt den Namen des Anwendungsgateways an, für das dieses Cmdlet ein Authentifizierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="3eccb-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="3eccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eccb-114">-DefaultProfile</span></span>
<span data-ttu-id="3eccb-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eccb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eccb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3eccb-116">-Name</span></span>
<span data-ttu-id="3eccb-117">Gibt den Namen des Authentifizierungszertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3eccb-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3eccb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eccb-118">CommonParameters</span></span>
<span data-ttu-id="3eccb-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eccb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eccb-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3eccb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eccb-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3eccb-121">INPUTS</span></span>

### <span data-ttu-id="3eccb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3eccb-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3eccb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3eccb-123">OUTPUTS</span></span>

### <span data-ttu-id="3eccb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="3eccb-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3eccb-125">NOTES</span></span>
* <span data-ttu-id="3eccb-126">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="3eccb-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3eccb-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3eccb-127">RELATED LINKS</span></span>

[<span data-ttu-id="3eccb-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3eccb-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3eccb-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="3eccb-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="3eccb-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


