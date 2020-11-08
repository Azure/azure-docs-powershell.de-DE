---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996742"
---
# <span data-ttu-id="00fa3-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="00fa3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="00fa3-103">Entfernt einen benutzerdefinierten Fehler aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="00fa3-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="00fa3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00fa3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00fa3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="00fa3-106">Mit dem Cmdlet **Remove-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler aus einem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="00fa3-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="00fa3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="00fa3-108">Beispiel 1: Entfernen von benutzerdefiniertem Fehler aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="00fa3-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="00fa3-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw entfernt, und das aktualisierte Gateway wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00fa3-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="00fa3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="00fa3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00fa3-111">-ApplicationGateway</span></span>
<span data-ttu-id="00fa3-112">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="00fa3-112">The Application Gateway</span></span>

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

### <span data-ttu-id="00fa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fa3-113">-DefaultProfile</span></span>
<span data-ttu-id="00fa3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00fa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00fa3-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="00fa3-115">-StatusCode</span></span>
<span data-ttu-id="00fa3-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="00fa3-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="00fa3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fa3-117">CommonParameters</span></span>
<span data-ttu-id="00fa3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fa3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fa3-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fa3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fa3-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00fa3-120">INPUTS</span></span>

### <span data-ttu-id="00fa3-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00fa3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00fa3-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00fa3-122">OUTPUTS</span></span>

### <span data-ttu-id="00fa3-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="00fa3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="00fa3-124">NOTES</span></span>

## <span data-ttu-id="00fa3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00fa3-125">RELATED LINKS</span></span>

[<span data-ttu-id="00fa3-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00fa3-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00fa3-128">Neu – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="00fa3-129">Satz-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="00fa3-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
