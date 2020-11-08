---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179751"
---
# <span data-ttu-id="46f68-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="46f68-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="46f68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46f68-102">SYNOPSIS</span></span>
<span data-ttu-id="46f68-103">Ruft den Verfügbarkeitsstatus des CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="46f68-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="46f68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46f68-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46f68-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46f68-105">DESCRIPTION</span></span>
<span data-ttu-id="46f68-106">Das Cmdlet " **Get-AzCdnEndpointNameAvailability** " Ruft den Verfügbarkeitsstatus des Azure Content Delivery Network (CDN)-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="46f68-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="46f68-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46f68-107">EXAMPLES</span></span>

## <span data-ttu-id="46f68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="46f68-108">PARAMETERS</span></span>

### <span data-ttu-id="46f68-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f68-109">-DefaultProfile</span></span>
<span data-ttu-id="46f68-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46f68-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46f68-111">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="46f68-111">-EndpointName</span></span>
<span data-ttu-id="46f68-112">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="46f68-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="46f68-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f68-113">CommonParameters</span></span>
<span data-ttu-id="46f68-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f68-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f68-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46f68-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f68-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46f68-116">INPUTS</span></span>

### <span data-ttu-id="46f68-117">Keine</span><span class="sxs-lookup"><span data-stu-id="46f68-117">None</span></span>

## <span data-ttu-id="46f68-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46f68-118">OUTPUTS</span></span>

### <span data-ttu-id="46f68-119">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="46f68-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="46f68-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="46f68-120">NOTES</span></span>

## <span data-ttu-id="46f68-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46f68-121">RELATED LINKS</span></span>
