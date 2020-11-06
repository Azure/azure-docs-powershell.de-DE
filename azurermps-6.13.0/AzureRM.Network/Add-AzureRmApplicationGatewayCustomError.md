---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479538"
---
# <span data-ttu-id="385e1-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="385e1-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="385e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="385e1-102">SYNOPSIS</span></span>
<span data-ttu-id="385e1-103">Fügt einen benutzerdefinierten Fehler zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="385e1-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="385e1-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="385e1-105">DESCRIPTION</span></span>
<span data-ttu-id="385e1-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="385e1-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="385e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="385e1-107">EXAMPLES</span></span>

### <span data-ttu-id="385e1-108">Beispiel 1: Hinzufügen von benutzerdefiniertem Fehler zu Application Gateway Level</span><span class="sxs-lookup"><span data-stu-id="385e1-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="385e1-109">Dieser Befehl fügt dem Application Gateway $appgw einen benutzerdefinierten Fehler des HTTP-Statuscodes 502 hinzu und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="385e1-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="385e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="385e1-110">PARAMETERS</span></span>

### <span data-ttu-id="385e1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385e1-111">-ApplicationGateway</span></span>
<span data-ttu-id="385e1-112">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="385e1-112">The Application Gateway</span></span>

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

### <span data-ttu-id="385e1-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="385e1-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="385e1-114">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="385e1-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="385e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385e1-115">-DefaultProfile</span></span>
<span data-ttu-id="385e1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="385e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385e1-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="385e1-117">-StatusCode</span></span>
<span data-ttu-id="385e1-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="385e1-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="385e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385e1-119">CommonParameters</span></span>
<span data-ttu-id="385e1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385e1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385e1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385e1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="385e1-122">INPUTS</span></span>

### <span data-ttu-id="385e1-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385e1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="385e1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="385e1-124">OUTPUTS</span></span>

### <span data-ttu-id="385e1-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="385e1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="385e1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="385e1-126">NOTES</span></span>

## <span data-ttu-id="385e1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="385e1-127">RELATED LINKS</span></span>
