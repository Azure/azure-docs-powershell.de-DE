---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRouteTable.md
ms.openlocfilehash: b04585705cb50a9f0acc7b3987fdfbb0a6c64cb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663355"
---
# <span data-ttu-id="fa196-101">New-AzureRmVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa196-101">New-AzureRmVirtualHubRouteTable</span></span>

## <span data-ttu-id="fa196-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa196-102">SYNOPSIS</span></span>
<span data-ttu-id="fa196-103">Erstellt ein Azure Virtual Hub-Routingtabellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="fa196-103">Creates an Azure Virtual Hub Route Table object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa196-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa196-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa196-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa196-105">DESCRIPTION</span></span>
<span data-ttu-id="fa196-106">Erstellt ein Azure Virtual Hub-Routingtabellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="fa196-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="fa196-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa196-107">EXAMPLES</span></span>

### <span data-ttu-id="fa196-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa196-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzureRmVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzureRmVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzureRmVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

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

<span data-ttu-id="fa196-109">Im obigen wird eine Route-Tabelle erstellt, die aus mehreren Routen besteht und an einen neuen virtuellen Hub angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="fa196-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="fa196-110">Hierbei handelt es sich um ein speicherresidentes Objekt, das zum Hinzufügen einer Routentabelle zu einem neuen oder vorhandenen VirtualHub verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa196-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="fa196-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa196-111">PARAMETERS</span></span>

### <span data-ttu-id="fa196-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa196-112">-DefaultProfile</span></span>
<span data-ttu-id="fa196-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa196-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa196-114">-Route</span><span class="sxs-lookup"><span data-stu-id="fa196-114">-Route</span></span>
<span data-ttu-id="fa196-115">Liste der virtuellen Hub-Routen</span><span class="sxs-lookup"><span data-stu-id="fa196-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="fa196-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa196-116">CommonParameters</span></span>
<span data-ttu-id="fa196-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa196-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa196-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa196-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa196-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa196-119">INPUTS</span></span>

### <span data-ttu-id="fa196-120">Keine</span><span class="sxs-lookup"><span data-stu-id="fa196-120">None</span></span>

## <span data-ttu-id="fa196-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa196-121">OUTPUTS</span></span>

### <span data-ttu-id="fa196-122">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fa196-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="fa196-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa196-123">NOTES</span></span>

## <span data-ttu-id="fa196-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa196-124">RELATED LINKS</span></span>
