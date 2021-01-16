---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: fbab2b1b9887fa7a5d509b46909f29eb741959bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292666"
---
# <span data-ttu-id="d26f1-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d26f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d26f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d26f1-103">Ruft ein Authentifizierungszertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="d26f1-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="d26f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d26f1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26f1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d26f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d26f1-106">Das **Cmdlet "Get-AzApplicationGatewayAuthenticationCertificate"** ruft ein Authentifizierungszertifikat für ein Azure-Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="d26f1-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d26f1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d26f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d26f1-108">Beispiel 1: Erhalten eines angegebenen Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="d26f1-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="d26f1-109">Der erste Befehl ruft das Anwendungsgateway namens "appGwName" ab und speichert es in der $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="d26f1-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="d26f1-110">Der zweite Befehl ruft das Authentifizierungszertifikat namens "pool01" ab und speichert es in der $pool Variable.</span><span class="sxs-lookup"><span data-stu-id="d26f1-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="d26f1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d26f1-111">PARAMETERS</span></span>

### <span data-ttu-id="d26f1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d26f1-112">-ApplicationGateway</span></span>
<span data-ttu-id="d26f1-113">Gibt den Namen des Anwendungsgateways an, für das dieses Cmdlet ein Authentifizierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="d26f1-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="d26f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26f1-114">-DefaultProfile</span></span>
<span data-ttu-id="d26f1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d26f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26f1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d26f1-116">-Name</span></span>
<span data-ttu-id="d26f1-117">Gibt den Namen des Authentifizierungszertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d26f1-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d26f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26f1-118">CommonParameters</span></span>
<span data-ttu-id="d26f1-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26f1-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d26f1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26f1-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d26f1-121">INPUTS</span></span>

### <span data-ttu-id="d26f1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d26f1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d26f1-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d26f1-123">OUTPUTS</span></span>

### <span data-ttu-id="d26f1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="d26f1-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d26f1-125">NOTES</span></span>
* <span data-ttu-id="d26f1-126">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="d26f1-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d26f1-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d26f1-127">RELATED LINKS</span></span>

[<span data-ttu-id="d26f1-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d26f1-129">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d26f1-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="d26f1-131">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="d26f1-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


