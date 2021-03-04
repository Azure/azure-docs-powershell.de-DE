---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: daea57cb0e8c910fca4fedabad0e4583354c4072
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928339"
---
# <span data-ttu-id="38463-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="38463-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="38463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38463-102">SYNOPSIS</span></span>
<span data-ttu-id="38463-103">Ruft den Verfügbarkeitsstatus des CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="38463-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="38463-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38463-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38463-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38463-105">DESCRIPTION</span></span>
<span data-ttu-id="38463-106">Das **Cmdlet Get-AzCdnEndpointNameAvailability** erhält den Verfügbarkeitsstatus des Azure Content Delivery Network (CDN)-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="38463-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="38463-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38463-107">EXAMPLES</span></span>

## <span data-ttu-id="38463-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="38463-108">PARAMETERS</span></span>

### <span data-ttu-id="38463-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38463-109">-DefaultProfile</span></span>
<span data-ttu-id="38463-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="38463-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38463-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="38463-111">-EndpointName</span></span>
<span data-ttu-id="38463-112">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="38463-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="38463-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38463-113">CommonParameters</span></span>
<span data-ttu-id="38463-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38463-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38463-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38463-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38463-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38463-116">INPUTS</span></span>

### <span data-ttu-id="38463-117">Keine</span><span class="sxs-lookup"><span data-stu-id="38463-117">None</span></span>

## <span data-ttu-id="38463-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38463-118">OUTPUTS</span></span>

### <span data-ttu-id="38463-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="38463-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="38463-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="38463-120">NOTES</span></span>

## <span data-ttu-id="38463-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="38463-121">RELATED LINKS</span></span>
