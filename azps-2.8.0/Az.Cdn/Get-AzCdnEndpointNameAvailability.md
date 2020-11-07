---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: f21c8303f1ec156132653a5d05c1149ef10a9ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652312"
---
# <span data-ttu-id="77cf1-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="77cf1-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="77cf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="77cf1-103">Ruft den Verfügbarkeitsstatus des CDN-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="77cf1-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="77cf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77cf1-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77cf1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="77cf1-106">Das Cmdlet " **Get-AzCdnEndpointNameAvailability** " Ruft den Verfügbarkeitsstatus des Azure Content Delivery Network (CDN)-Endpunkts ab.</span><span class="sxs-lookup"><span data-stu-id="77cf1-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="77cf1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77cf1-107">EXAMPLES</span></span>

## <span data-ttu-id="77cf1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="77cf1-108">PARAMETERS</span></span>

### <span data-ttu-id="77cf1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cf1-109">-DefaultProfile</span></span>
<span data-ttu-id="77cf1-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="77cf1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77cf1-111">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="77cf1-111">-EndpointName</span></span>
<span data-ttu-id="77cf1-112">Gibt den Namen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="77cf1-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="77cf1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cf1-113">CommonParameters</span></span>
<span data-ttu-id="77cf1-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cf1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cf1-115">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77cf1-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cf1-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77cf1-116">INPUTS</span></span>

### <span data-ttu-id="77cf1-117">Keine</span><span class="sxs-lookup"><span data-stu-id="77cf1-117">None</span></span>

## <span data-ttu-id="77cf1-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77cf1-118">OUTPUTS</span></span>

### <span data-ttu-id="77cf1-119">Microsoft. Azure. Commands. CDN. Models. EndPoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="77cf1-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="77cf1-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="77cf1-120">NOTES</span></span>

## <span data-ttu-id="77cf1-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77cf1-121">RELATED LINKS</span></span>
