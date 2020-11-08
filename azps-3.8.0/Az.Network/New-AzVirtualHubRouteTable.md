---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 9648eb1561ae15501f7a395846f7fda71cf5a1f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003445"
---
# <span data-ttu-id="87c3d-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="87c3d-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="87c3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="87c3d-103">Erstellt ein Azure Virtual Hub-Routingtabellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="87c3d-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="87c3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87c3d-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87c3d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="87c3d-106">Erstellt ein Azure Virtual Hub-Routingtabellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="87c3d-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="87c3d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="87c3d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87c3d-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="87c3d-109">Im obigen wird eine Route-Tabelle erstellt, die aus mehreren Routen besteht und an einen neuen virtuellen Hub angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="87c3d-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="87c3d-110">Hierbei handelt es sich um ein speicherresidentes Objekt, das zum Hinzufügen einer Routentabelle zu einem neuen oder vorhandenen VirtualHub verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="87c3d-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="87c3d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="87c3d-111">PARAMETERS</span></span>

### <span data-ttu-id="87c3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c3d-112">-DefaultProfile</span></span>
<span data-ttu-id="87c3d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87c3d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c3d-114">-Route</span><span class="sxs-lookup"><span data-stu-id="87c3d-114">-Route</span></span>
<span data-ttu-id="87c3d-115">Liste der virtuellen Hub-Routen</span><span class="sxs-lookup"><span data-stu-id="87c3d-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c3d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c3d-116">CommonParameters</span></span>
<span data-ttu-id="87c3d-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c3d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c3d-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c3d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c3d-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87c3d-119">INPUTS</span></span>

### <span data-ttu-id="87c3d-120">Keine</span><span class="sxs-lookup"><span data-stu-id="87c3d-120">None</span></span>

## <span data-ttu-id="87c3d-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87c3d-121">OUTPUTS</span></span>

### <span data-ttu-id="87c3d-122">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="87c3d-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="87c3d-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="87c3d-123">NOTES</span></span>

## <span data-ttu-id="87c3d-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87c3d-124">RELATED LINKS</span></span>

[<span data-ttu-id="87c3d-125">Neu – AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="87c3d-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
