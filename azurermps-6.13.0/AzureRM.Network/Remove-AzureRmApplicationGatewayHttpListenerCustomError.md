---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479485"
---
# <span data-ttu-id="99e82-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="99e82-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="99e82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99e82-102">SYNOPSIS</span></span>
<span data-ttu-id="99e82-103">Entfernt einen benutzerdefinierten Fehler aus einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="99e82-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99e82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e82-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99e82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99e82-105">DESCRIPTION</span></span>
<span data-ttu-id="99e82-106">Mit dem Cmdlet **Remove-AzureRmApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler aus einem HTTP-Listener eines Anwendungs Gateways entfernt.</span><span class="sxs-lookup"><span data-stu-id="99e82-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="99e82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99e82-107">EXAMPLES</span></span>

### <span data-ttu-id="99e82-108">Beispiel 1: entfernt benutzerdefinierten Fehler aus einem HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="99e82-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="99e82-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 502 vom HTTP-Listener $Listener 01 entfernt, und der aktualisierte Listener wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99e82-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="99e82-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e82-110">PARAMETERS</span></span>

### <span data-ttu-id="99e82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e82-111">-DefaultProfile</span></span>
<span data-ttu-id="99e82-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99e82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e82-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="99e82-113">-HttpListener</span></span>
<span data-ttu-id="99e82-114">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="99e82-114">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e82-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="99e82-115">-StatusCode</span></span>
<span data-ttu-id="99e82-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="99e82-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e82-117">CommonParameters</span></span>
<span data-ttu-id="99e82-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99e82-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e82-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e82-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99e82-120">INPUTS</span></span>

### <span data-ttu-id="99e82-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="99e82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="99e82-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99e82-122">OUTPUTS</span></span>

### <span data-ttu-id="99e82-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="99e82-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="99e82-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="99e82-124">NOTES</span></span>

## <span data-ttu-id="99e82-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99e82-125">RELATED LINKS</span></span>
