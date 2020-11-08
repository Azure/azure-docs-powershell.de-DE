---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179831"
---
# <span data-ttu-id="66d33-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="66d33-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="66d33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66d33-102">SYNOPSIS</span></span>
<span data-ttu-id="66d33-103">Aktualisiert einen benutzerdefinierten Fehler in einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="66d33-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="66d33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66d33-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66d33-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66d33-105">DESCRIPTION</span></span>
<span data-ttu-id="66d33-106">Das Cmdlet " **Satz-AzApplicationGatewayCustomError** " aktualisiert einen benutzerdefinierten Fehler in einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="66d33-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="66d33-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66d33-107">EXAMPLES</span></span>

### <span data-ttu-id="66d33-108">Beispiel 1: aktualisiert einen benutzerdefinierten Fehler von einem HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="66d33-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="66d33-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler des HTTP-Statuscodes 502 im http-Listener $Listener 01 und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="66d33-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="66d33-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66d33-110">PARAMETERS</span></span>

### <span data-ttu-id="66d33-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="66d33-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="66d33-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="66d33-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="66d33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d33-113">-DefaultProfile</span></span>
<span data-ttu-id="66d33-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66d33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66d33-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="66d33-115">-HttpListener</span></span>
<span data-ttu-id="66d33-116">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="66d33-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="66d33-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="66d33-117">-StatusCode</span></span>
<span data-ttu-id="66d33-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="66d33-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="66d33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d33-119">CommonParameters</span></span>
<span data-ttu-id="66d33-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d33-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d33-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d33-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66d33-122">INPUTS</span></span>

### <span data-ttu-id="66d33-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66d33-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="66d33-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66d33-124">OUTPUTS</span></span>

### <span data-ttu-id="66d33-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="66d33-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="66d33-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="66d33-126">NOTES</span></span>

## <span data-ttu-id="66d33-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66d33-127">RELATED LINKS</span></span>

[<span data-ttu-id="66d33-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="66d33-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="66d33-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="66d33-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="66d33-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="66d33-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
