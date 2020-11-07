---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: afa217565dc90bed1f047bc18b9407141b98dd0c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822348"
---
# <span data-ttu-id="c9608-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c9608-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c9608-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9608-102">SYNOPSIS</span></span>
<span data-ttu-id="c9608-103">Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="c9608-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="c9608-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9608-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9608-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9608-105">DESCRIPTION</span></span>
<span data-ttu-id="c9608-106">Das Cmdlet " **Get-AzExpressRouteServiceProvider** " Ruft eine Liste Express Route Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="c9608-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="c9608-107">Attribute sind Standort-und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="c9608-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="c9608-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9608-108">EXAMPLES</span></span>

### <span data-ttu-id="c9608-109">Beispiel 1: Abrufen einer Liste des Dienstanbieters mit Speicherorten in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="c9608-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="c9608-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9608-110">PARAMETERS</span></span>

### <span data-ttu-id="c9608-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9608-111">-DefaultProfile</span></span>
<span data-ttu-id="c9608-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9608-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9608-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9608-113">CommonParameters</span></span>
<span data-ttu-id="c9608-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9608-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9608-115">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9608-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9608-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9608-116">INPUTS</span></span>

### <span data-ttu-id="c9608-117">Keine</span><span class="sxs-lookup"><span data-stu-id="c9608-117">None</span></span>

## <span data-ttu-id="c9608-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9608-118">OUTPUTS</span></span>

### <span data-ttu-id="c9608-119">Microsoft. Azure. Commands. Network. Models. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c9608-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c9608-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9608-120">NOTES</span></span>

## <span data-ttu-id="c9608-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9608-121">RELATED LINKS</span></span>

[<span data-ttu-id="c9608-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c9608-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c9608-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c9608-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c9608-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c9608-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c9608-125">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c9608-125">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
