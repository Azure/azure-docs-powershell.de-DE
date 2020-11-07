---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662356"
---
# <span data-ttu-id="1c345-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="1c345-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1c345-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c345-102">SYNOPSIS</span></span>
<span data-ttu-id="1c345-103">Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="1c345-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c345-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c345-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c345-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c345-105">DESCRIPTION</span></span>
<span data-ttu-id="1c345-106">Das Cmdlet " **Get-AzureRmExpressRouteServiceProvider** " Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="1c345-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="1c345-107">Attribute sind Standort-und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="1c345-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="1c345-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c345-108">EXAMPLES</span></span>

### <span data-ttu-id="1c345-109">Beispiel 1: Abrufen einer Liste des Dienstanbieters mit Speicherorten in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="1c345-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="1c345-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c345-110">PARAMETERS</span></span>

### <span data-ttu-id="1c345-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c345-111">-DefaultProfile</span></span>
<span data-ttu-id="1c345-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c345-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c345-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c345-113">CommonParameters</span></span>
<span data-ttu-id="1c345-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c345-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c345-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c345-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c345-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c345-116">INPUTS</span></span>

### <span data-ttu-id="1c345-117">Keine</span><span class="sxs-lookup"><span data-stu-id="1c345-117">None</span></span>
<span data-ttu-id="1c345-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1c345-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c345-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c345-119">OUTPUTS</span></span>

### <span data-ttu-id="1c345-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="1c345-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="1c345-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c345-121">NOTES</span></span>

## <span data-ttu-id="1c345-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c345-122">RELATED LINKS</span></span>

[<span data-ttu-id="1c345-123">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="1c345-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="1c345-124">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="1c345-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="1c345-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="1c345-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="1c345-126">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="1c345-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
