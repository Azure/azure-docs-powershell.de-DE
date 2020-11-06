---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500925"
---
# <span data-ttu-id="bcb91-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bcb91-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="bcb91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcb91-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb91-103">Ruft den Verfügbarkeitsstatus des CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="bcb91-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcb91-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcb91-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb91-106">Das Cmdlet " **Get-AzureRmCdnEndpointNameAvailability** " Ruft den Verfügbarkeitsstatus des Azure Content Delivery Network (CDN)-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="bcb91-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bcb91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcb91-107">EXAMPLES</span></span>

## <span data-ttu-id="bcb91-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcb91-108">PARAMETERS</span></span>

### <span data-ttu-id="bcb91-109">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="bcb91-109">-EndpointName</span></span>
<span data-ttu-id="bcb91-110">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="bcb91-110">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="bcb91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb91-111">-DefaultProfile</span></span>
<span data-ttu-id="bcb91-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcb91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcb91-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb91-113">CommonParameters</span></span>
<span data-ttu-id="bcb91-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb91-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb91-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb91-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb91-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcb91-116">INPUTS</span></span>

## <span data-ttu-id="bcb91-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcb91-117">OUTPUTS</span></span>

### <span data-ttu-id="bcb91-118">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="bcb91-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="bcb91-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcb91-119">NOTES</span></span>

## <span data-ttu-id="bcb91-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcb91-120">RELATED LINKS</span></span>

