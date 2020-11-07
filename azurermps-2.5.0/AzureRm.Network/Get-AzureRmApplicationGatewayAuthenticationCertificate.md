---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 033ca62f766f854be27ad75a6b63a8f883ba58d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850760"
---
# <span data-ttu-id="7259b-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-101">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7259b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7259b-102">SYNOPSIS</span></span>
<span data-ttu-id="7259b-103">Ruft ein Authentifizierungszertifikat für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="7259b-103">Gets an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7259b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7259b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7259b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7259b-105">DESCRIPTION</span></span>
<span data-ttu-id="7259b-106">Das Cmdlet " **Get-AzureRmApplicationGatewayAuthenticationCertificate** " Ruft ein Authentifizierungszertifikat für ein Azure Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="7259b-106">The **Get-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet gets an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7259b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7259b-107">EXAMPLES</span></span>

### <span data-ttu-id="7259b-108">1:</span><span class="sxs-lookup"><span data-stu-id="7259b-108">1:</span></span>
```

```

## <span data-ttu-id="7259b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7259b-109">PARAMETERS</span></span>

### <span data-ttu-id="7259b-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7259b-110">-ApplicationGateway</span></span>
<span data-ttu-id="7259b-111">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet ein Authentifizierungszertifikat erhält.</span><span class="sxs-lookup"><span data-stu-id="7259b-111">Specifies the name of application gateway for which this cmdlet gets an authentication certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7259b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7259b-112">-DefaultProfile</span></span>
<span data-ttu-id="7259b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7259b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7259b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7259b-114">-Name</span></span>
<span data-ttu-id="7259b-115">Gibt den Namen des Authentifizierungszertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7259b-115">Specifies the name of the authentication certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7259b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7259b-116">CommonParameters</span></span>
<span data-ttu-id="7259b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7259b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7259b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7259b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7259b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7259b-119">INPUTS</span></span>

### <span data-ttu-id="7259b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7259b-120">System.String</span></span>

## <span data-ttu-id="7259b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7259b-121">OUTPUTS</span></span>

### <span data-ttu-id="7259b-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="7259b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7259b-123">NOTES</span></span>
* <span data-ttu-id="7259b-124">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="7259b-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="7259b-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7259b-125">RELATED LINKS</span></span>

[<span data-ttu-id="7259b-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-126">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7259b-127">Neu – AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-127">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7259b-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-128">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="7259b-129">Satz-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="7259b-129">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


