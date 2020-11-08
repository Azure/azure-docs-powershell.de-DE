---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009658"
---
# <span data-ttu-id="88ac9-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="88ac9-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="88ac9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="88ac9-103">Entfernt einen benutzerdefinierten Fehler aus einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="88ac9-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="88ac9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88ac9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88ac9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="88ac9-106">Mit dem Cmdlet **Remove-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler aus einem HTTP-Listener eines Anwendungs Gateways entfernt.</span><span class="sxs-lookup"><span data-stu-id="88ac9-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="88ac9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="88ac9-108">Beispiel 1: entfernt benutzerdefinierten Fehler aus einem HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="88ac9-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="88ac9-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 502 vom HTTP-Listener $Listener 01 entfernt, und der aktualisierte Listener wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88ac9-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="88ac9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="88ac9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ac9-111">-DefaultProfile</span></span>
<span data-ttu-id="88ac9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88ac9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88ac9-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="88ac9-113">-HttpListener</span></span>
<span data-ttu-id="88ac9-114">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="88ac9-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ac9-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="88ac9-115">-StatusCode</span></span>
<span data-ttu-id="88ac9-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="88ac9-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="88ac9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ac9-117">CommonParameters</span></span>
<span data-ttu-id="88ac9-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ac9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ac9-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ac9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ac9-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88ac9-120">INPUTS</span></span>

### <span data-ttu-id="88ac9-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="88ac9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="88ac9-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88ac9-122">OUTPUTS</span></span>

### <span data-ttu-id="88ac9-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="88ac9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="88ac9-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="88ac9-124">NOTES</span></span>

## <span data-ttu-id="88ac9-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88ac9-125">RELATED LINKS</span></span>

[<span data-ttu-id="88ac9-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="88ac9-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="88ac9-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="88ac9-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="88ac9-128">Satz-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="88ac9-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
