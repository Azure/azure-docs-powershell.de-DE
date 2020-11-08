---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995678"
---
# <span data-ttu-id="6352d-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="6352d-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="6352d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6352d-102">SYNOPSIS</span></span>
<span data-ttu-id="6352d-103">Ruft den Verfügbarkeitsstatus des CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="6352d-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="6352d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6352d-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6352d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6352d-105">DESCRIPTION</span></span>
<span data-ttu-id="6352d-106">Das Cmdlet " **Get-AzCdnEndpointNameAvailability** " Ruft den Verfügbarkeitsstatus des Azure Content Delivery Network (CDN)-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="6352d-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6352d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6352d-107">EXAMPLES</span></span>

## <span data-ttu-id="6352d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6352d-108">PARAMETERS</span></span>

### <span data-ttu-id="6352d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6352d-109">-DefaultProfile</span></span>
<span data-ttu-id="6352d-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6352d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6352d-111">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="6352d-111">-EndpointName</span></span>
<span data-ttu-id="6352d-112">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="6352d-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="6352d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6352d-113">CommonParameters</span></span>
<span data-ttu-id="6352d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6352d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6352d-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6352d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6352d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6352d-116">INPUTS</span></span>

### <span data-ttu-id="6352d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="6352d-117">None</span></span>

## <span data-ttu-id="6352d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6352d-118">OUTPUTS</span></span>

### <span data-ttu-id="6352d-119">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="6352d-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="6352d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="6352d-120">NOTES</span></span>

## <span data-ttu-id="6352d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6352d-121">RELATED LINKS</span></span>
