---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479493"
---
# <span data-ttu-id="ebbd0-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ebbd0-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ebbd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbd0-103">Entfernt einen benutzerdefinierten Fehler aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebbd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebbd0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebbd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebbd0-105">DESCRIPTION</span></span>
<span data-ttu-id="ebbd0-106">Mit dem Cmdlet **Remove-AzureRmApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler aus einem Anwendungsgateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="ebbd0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebbd0-107">EXAMPLES</span></span>

### <span data-ttu-id="ebbd0-108">Beispiel 1: Entfernen von benutzerdefiniertem Fehler aus einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="ebbd0-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="ebbd0-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 502 aus dem Application Gateway $appgw entfernt, und das aktualisierte Gateway wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="ebbd0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebbd0-110">PARAMETERS</span></span>

### <span data-ttu-id="ebbd0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebbd0-111">-ApplicationGateway</span></span>
<span data-ttu-id="ebbd0-112">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="ebbd0-112">The Application Gateway</span></span>

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

### <span data-ttu-id="ebbd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbd0-113">-DefaultProfile</span></span>
<span data-ttu-id="ebbd0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="ebbd0-115">-StatusCode</span></span>
<span data-ttu-id="ebbd0-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="ebbd0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbd0-117">CommonParameters</span></span>
<span data-ttu-id="ebbd0-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebbd0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbd0-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbd0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbd0-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebbd0-120">INPUTS</span></span>

### <span data-ttu-id="ebbd0-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebbd0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebbd0-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebbd0-122">OUTPUTS</span></span>

### <span data-ttu-id="ebbd0-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebbd0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebbd0-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebbd0-124">NOTES</span></span>

## <span data-ttu-id="ebbd0-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebbd0-125">RELATED LINKS</span></span>
