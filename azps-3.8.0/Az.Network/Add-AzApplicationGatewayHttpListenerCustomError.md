---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995526"
---
# <span data-ttu-id="8cfcf-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8cfcf-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="8cfcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfcf-103">Fügt einen benutzerdefinierten Fehler zu einem HTTP-Listener eines Anwendungs Gateways hinzu.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="8cfcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cfcf-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cfcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cfcf-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfcf-106">Mit dem Cmdlet **Add-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler zu einem HTTP-Listener eines Anwendungs Gateways hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="8cfcf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cfcf-107">EXAMPLES</span></span>

### <span data-ttu-id="8cfcf-108">Beispiel 1: Hinzufügen eines benutzerdefinierten Fehlers zur HTTP-Listener-Ebene</span><span class="sxs-lookup"><span data-stu-id="8cfcf-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="8cfcf-109">Dieser Befehl fügt dem HTTP-Listener $Listener 01 einen benutzerdefinierten Fehler des HTTP-Statuscodes 502 hinzu und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="8cfcf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cfcf-110">PARAMETERS</span></span>

### <span data-ttu-id="8cfcf-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="8cfcf-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="8cfcf-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8cfcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfcf-113">-DefaultProfile</span></span>
<span data-ttu-id="8cfcf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cfcf-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="8cfcf-115">-HttpListener</span></span>
<span data-ttu-id="8cfcf-116">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="8cfcf-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="8cfcf-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="8cfcf-117">-StatusCode</span></span>
<span data-ttu-id="8cfcf-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8cfcf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfcf-119">CommonParameters</span></span>
<span data-ttu-id="8cfcf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cfcf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfcf-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfcf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfcf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cfcf-122">INPUTS</span></span>

### <span data-ttu-id="8cfcf-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8cfcf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="8cfcf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cfcf-124">OUTPUTS</span></span>

### <span data-ttu-id="8cfcf-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="8cfcf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="8cfcf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cfcf-126">NOTES</span></span>

## <span data-ttu-id="8cfcf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cfcf-127">RELATED LINKS</span></span>

[<span data-ttu-id="8cfcf-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8cfcf-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="8cfcf-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8cfcf-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="8cfcf-130">Satz-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8cfcf-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
