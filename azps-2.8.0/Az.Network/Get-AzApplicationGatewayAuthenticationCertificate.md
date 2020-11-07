---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 1743ed0427fdc0dd952c9b86d51c13c3ed855620
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821955"
---
# <span data-ttu-id="e2104-101">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-101">Get-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e2104-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2104-102">SYNOPSIS</span></span>
<span data-ttu-id="e2104-103">Ruft ein Authentifizierungszertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="e2104-103">Gets an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="e2104-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2104-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAuthenticationCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2104-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2104-105">DESCRIPTION</span></span>
<span data-ttu-id="e2104-106">Das Cmdlet " **Get-AzApplicationGatewayAuthenticationCertificate** " Ruft ein Authentifizierungszertifikat für ein Azure Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="e2104-106">The **Get-AzApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e2104-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2104-107">EXAMPLES</span></span>

### <span data-ttu-id="e2104-108">Beispiel 1: Abrufen eines angegebenen Authentifizierungszertifikats</span><span class="sxs-lookup"><span data-stu-id="e2104-108">Example 1: Get a specified authentication certificate</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -Name "pool01" -ApplicationGateway $appgw
```

<span data-ttu-id="e2104-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen appGwName ab und speichert es in der $appgw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e2104-109">The first command gets the application gateway named appGwName and stores it in the $appgw variable.</span></span>
<span data-ttu-id="e2104-110">Der zweite Befehl ruft das Authentifizierungszertifikat mit dem Namen pool01 ab und speichert es in der $Pool-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e2104-110">The second command gets the authentication certificate named pool01 and stores it in the $pool variable.</span></span>

## <span data-ttu-id="e2104-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2104-111">PARAMETERS</span></span>

### <span data-ttu-id="e2104-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2104-112">-ApplicationGateway</span></span>
<span data-ttu-id="e2104-113">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="e2104-113">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

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

### <span data-ttu-id="e2104-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2104-114">-DefaultProfile</span></span>
<span data-ttu-id="e2104-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2104-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2104-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e2104-116">-Name</span></span>
<span data-ttu-id="e2104-117">Gibt den Namen des Authentifizierungszertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e2104-117">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2104-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2104-118">CommonParameters</span></span>
<span data-ttu-id="e2104-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2104-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2104-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2104-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2104-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2104-121">INPUTS</span></span>

### <span data-ttu-id="e2104-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2104-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2104-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2104-123">OUTPUTS</span></span>

### <span data-ttu-id="e2104-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="e2104-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2104-125">NOTES</span></span>
* <span data-ttu-id="e2104-126">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="e2104-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e2104-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2104-127">RELATED LINKS</span></span>

[<span data-ttu-id="e2104-128">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-128">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e2104-129">Neu – AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-129">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e2104-130">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-130">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="e2104-131">Satz-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="e2104-131">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


