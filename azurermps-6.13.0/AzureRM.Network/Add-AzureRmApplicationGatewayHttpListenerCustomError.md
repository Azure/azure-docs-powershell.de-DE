---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 23cb65073f25f65a4e09f3b4a28891cff4e49c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664561"
---
# <span data-ttu-id="6573a-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6573a-101">Add-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="6573a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6573a-102">SYNOPSIS</span></span>
<span data-ttu-id="6573a-103">Fügt einen benutzerdefinierten Fehler zu einem HTTP-Listener eines Anwendungs Gateways hinzu.</span><span class="sxs-lookup"><span data-stu-id="6573a-103">Adds a custom error to a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6573a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6573a-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6573a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6573a-105">DESCRIPTION</span></span>
<span data-ttu-id="6573a-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler zu einem HTTP-Listener eines Anwendungs Gateways hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6573a-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="6573a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6573a-107">EXAMPLES</span></span>

### <span data-ttu-id="6573a-108">Beispiel 1: Hinzufügen eines benutzerdefinierten Fehlers zur HTTP-Listener-Ebene</span><span class="sxs-lookup"><span data-stu-id="6573a-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="6573a-109">Dieser Befehl fügt dem HTTP-Listener $Listener 01 einen benutzerdefinierten Fehler des HTTP-Statuscodes 502 hinzu und gibt den aktualisierten Listener zurück.</span><span class="sxs-lookup"><span data-stu-id="6573a-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="6573a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6573a-110">PARAMETERS</span></span>

### <span data-ttu-id="6573a-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="6573a-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="6573a-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="6573a-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6573a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6573a-113">-DefaultProfile</span></span>
<span data-ttu-id="6573a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6573a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6573a-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6573a-115">-HttpListener</span></span>
<span data-ttu-id="6573a-116">Der HTTP-Listener für Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6573a-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="6573a-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="6573a-117">-StatusCode</span></span>
<span data-ttu-id="6573a-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="6573a-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="6573a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6573a-119">CommonParameters</span></span>
<span data-ttu-id="6573a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6573a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6573a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6573a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6573a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6573a-122">INPUTS</span></span>

### <span data-ttu-id="6573a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6573a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6573a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6573a-124">OUTPUTS</span></span>

### <span data-ttu-id="6573a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6573a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6573a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6573a-126">NOTES</span></span>

## <span data-ttu-id="6573a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6573a-127">RELATED LINKS</span></span>
