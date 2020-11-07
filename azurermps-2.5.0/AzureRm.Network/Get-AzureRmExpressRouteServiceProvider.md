---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849215"
---
# <span data-ttu-id="10735-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="10735-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="10735-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10735-102">SYNOPSIS</span></span>
<span data-ttu-id="10735-103">Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="10735-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10735-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10735-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10735-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10735-105">DESCRIPTION</span></span>
<span data-ttu-id="10735-106">Das Cmdlet " **Get-AzureRmExpressRouteServiceProvider** " Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="10735-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="10735-107">Attribute sind Standort-und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="10735-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="10735-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10735-108">EXAMPLES</span></span>

### <span data-ttu-id="10735-109">Beispiel 1: Abrufen einer Liste des Dienstanbieters mit Speicherorten in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="10735-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="10735-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10735-110">PARAMETERS</span></span>

### <span data-ttu-id="10735-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10735-111">-DefaultProfile</span></span>
<span data-ttu-id="10735-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10735-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10735-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10735-113">CommonParameters</span></span>
<span data-ttu-id="10735-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10735-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10735-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10735-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10735-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10735-116">INPUTS</span></span>

## <span data-ttu-id="10735-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10735-117">OUTPUTS</span></span>

### <span data-ttu-id="10735-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="10735-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="10735-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="10735-119">NOTES</span></span>

## <span data-ttu-id="10735-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10735-120">RELATED LINKS</span></span>

[<span data-ttu-id="10735-121">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="10735-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="10735-122">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="10735-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="10735-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10735-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="10735-124">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="10735-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
