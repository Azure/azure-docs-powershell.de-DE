---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174534"
---
# <span data-ttu-id="afecf-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="afecf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afecf-102">SYNOPSIS</span></span>
<span data-ttu-id="afecf-103">Aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="afecf-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="afecf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afecf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afecf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afecf-105">DESCRIPTION</span></span>
<span data-ttu-id="afecf-106">Das Cmdlet " **Satz-AzApplicationGatewayCustomError** " aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="afecf-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="afecf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afecf-107">EXAMPLES</span></span>

### <span data-ttu-id="afecf-108">Beispiel 1: Aktualisieren des benutzerdefinierten Fehlers in einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="afecf-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="afecf-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler des HTTP-Statuscodes 502 im Application Gateway $appgw und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="afecf-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="afecf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afecf-110">PARAMETERS</span></span>

### <span data-ttu-id="afecf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afecf-111">-ApplicationGateway</span></span>
<span data-ttu-id="afecf-112">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="afecf-112">The Application Gateway</span></span>

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

### <span data-ttu-id="afecf-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="afecf-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="afecf-114">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="afecf-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="afecf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afecf-115">-DefaultProfile</span></span>
<span data-ttu-id="afecf-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="afecf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afecf-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="afecf-117">-StatusCode</span></span>
<span data-ttu-id="afecf-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="afecf-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="afecf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afecf-119">CommonParameters</span></span>
<span data-ttu-id="afecf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afecf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afecf-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afecf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afecf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afecf-122">INPUTS</span></span>

### <span data-ttu-id="afecf-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afecf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="afecf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afecf-124">OUTPUTS</span></span>

### <span data-ttu-id="afecf-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="afecf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="afecf-126">NOTES</span></span>

## <span data-ttu-id="afecf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afecf-127">RELATED LINKS</span></span>

[<span data-ttu-id="afecf-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="afecf-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="afecf-130">Neu – AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="afecf-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="afecf-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
