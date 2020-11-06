---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495857"
---
# <span data-ttu-id="78012-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="78012-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="78012-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78012-102">SYNOPSIS</span></span>
<span data-ttu-id="78012-103">Aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="78012-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78012-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78012-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78012-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78012-105">DESCRIPTION</span></span>
<span data-ttu-id="78012-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayCustomError** " aktualisiert einen benutzerdefinierten Fehler in einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="78012-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="78012-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78012-107">EXAMPLES</span></span>

### <span data-ttu-id="78012-108">Beispiel 1: Aktualisieren des benutzerdefinierten Fehlers in einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="78012-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="78012-109">Dieser Befehl aktualisiert den benutzerdefinierten Fehler des HTTP-Statuscodes 502 im Application Gateway $appgw und gibt das aktualisierte Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="78012-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="78012-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78012-110">PARAMETERS</span></span>

### <span data-ttu-id="78012-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78012-111">-ApplicationGateway</span></span>
<span data-ttu-id="78012-112">Das Anwendungs Gateway</span><span class="sxs-lookup"><span data-stu-id="78012-112">The Application Gateway</span></span>

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

### <span data-ttu-id="78012-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="78012-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="78012-114">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="78012-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="78012-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78012-115">-DefaultProfile</span></span>
<span data-ttu-id="78012-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78012-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78012-117">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="78012-117">-StatusCode</span></span>
<span data-ttu-id="78012-118">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="78012-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="78012-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78012-119">CommonParameters</span></span>
<span data-ttu-id="78012-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78012-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78012-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78012-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78012-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78012-122">INPUTS</span></span>

### <span data-ttu-id="78012-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78012-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78012-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78012-124">OUTPUTS</span></span>

### <span data-ttu-id="78012-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78012-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78012-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="78012-126">NOTES</span></span>

## <span data-ttu-id="78012-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78012-127">RELATED LINKS</span></span>
