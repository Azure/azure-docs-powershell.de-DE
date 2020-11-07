---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662170"
---
# <span data-ttu-id="38103-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="38103-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="38103-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38103-102">SYNOPSIS</span></span>
<span data-ttu-id="38103-103">Aktualisiert einen benutzerdefinierten Fehler in einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="38103-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38103-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38103-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38103-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38103-105">DESCRIPTION</span></span>
<span data-ttu-id="38103-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayCustomError** " aktualisiert einen benutzerdefinierten Fehler in einem HTTP-Listener eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="38103-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="38103-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38103-107">EXAMPLES</span></span>

### <span data-ttu-id="38103-108">Beispiel 1: aktualisiert einen benutzerdefinierten Fehler von einem HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="38103-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="38103-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler des HTTP-Statuscodes 502 im http-Listener $Listener 01 und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="38103-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="38103-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="38103-110">PARAMETERS</span></span>

### <span data-ttu-id="38103-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="38103-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="38103-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="38103-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="38103-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38103-113">-DefaultProfile</span></span>
<span data-ttu-id="38103-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38103-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38103-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="38103-115">-HttpListener</span></span>
<span data-ttu-id="38103-116">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="38103-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="38103-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="38103-117">-StatusCode</span></span>
<span data-ttu-id="38103-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="38103-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="38103-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38103-119">CommonParameters</span></span>
<span data-ttu-id="38103-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38103-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38103-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38103-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38103-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38103-122">INPUTS</span></span>

### <span data-ttu-id="38103-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="38103-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="38103-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38103-124">OUTPUTS</span></span>

### <span data-ttu-id="38103-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="38103-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="38103-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="38103-126">NOTES</span></span>

## <span data-ttu-id="38103-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38103-127">RELATED LINKS</span></span>
