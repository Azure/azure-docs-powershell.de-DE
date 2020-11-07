---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: ce3d4e42c6644cd3181ec9389a7b571c7f6ca51a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841643"
---
# <span data-ttu-id="59dd1-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="59dd1-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="59dd1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="59dd1-103">Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="59dd1-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="59dd1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59dd1-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59dd1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59dd1-105">DESCRIPTION</span></span>
<span data-ttu-id="59dd1-106">Das Cmdlet " **Get-AzExpressRouteServiceProvider** " Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="59dd1-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="59dd1-107">Attribute sind Standort-und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="59dd1-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="59dd1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59dd1-108">EXAMPLES</span></span>

### <span data-ttu-id="59dd1-109">Beispiel 1: Abrufen einer Liste des Dienstanbieters mit Speicherorten in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="59dd1-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="59dd1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59dd1-110">PARAMETERS</span></span>

### <span data-ttu-id="59dd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59dd1-111">-DefaultProfile</span></span>
<span data-ttu-id="59dd1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59dd1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59dd1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59dd1-113">CommonParameters</span></span>
<span data-ttu-id="59dd1-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59dd1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59dd1-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59dd1-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59dd1-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59dd1-116">INPUTS</span></span>

## <span data-ttu-id="59dd1-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59dd1-117">OUTPUTS</span></span>

### <span data-ttu-id="59dd1-118">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="59dd1-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="59dd1-119">Notizen</span><span class="sxs-lookup"><span data-stu-id="59dd1-119">NOTES</span></span>

## <span data-ttu-id="59dd1-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59dd1-120">RELATED LINKS</span></span>

[<span data-ttu-id="59dd1-121">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="59dd1-121">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="59dd1-122">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="59dd1-122">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="59dd1-123">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="59dd1-123">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="59dd1-124">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="59dd1-124">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
