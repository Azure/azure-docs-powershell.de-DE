---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821492"
---
# <span data-ttu-id="1b6b8-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1b6b8-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="1b6b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6b8-103">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="1b6b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b6b8-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6b8-106">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="1b6b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b6b8-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b6b8-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="1b6b8-109">Das obige wird ein virtuelles Hub-Routing-Objekt erstellen, das in die virtuelle Hub-Route-Tabelle aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="1b6b8-110">Die virtuelle Hub-Route ist ein in-Memory-Objekt, das zum Erstellen eines VirtualHubRouteTable-Objekts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="1b6b8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b6b8-111">PARAMETERS</span></span>

### <span data-ttu-id="1b6b8-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1b6b8-112">-AddressPrefix</span></span>
<span data-ttu-id="1b6b8-113">Liste der Adresspräfixe</span><span class="sxs-lookup"><span data-stu-id="1b6b8-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6b8-114">-DefaultProfile</span></span>
<span data-ttu-id="1b6b8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6b8-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="1b6b8-116">-NextHopIpAddress</span></span>
<span data-ttu-id="1b6b8-117">Die IPAddress für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="1b6b8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6b8-118">CommonParameters</span></span>
<span data-ttu-id="1b6b8-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6b8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6b8-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6b8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6b8-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b6b8-121">INPUTS</span></span>

### <span data-ttu-id="1b6b8-122">Keine</span><span class="sxs-lookup"><span data-stu-id="1b6b8-122">None</span></span>

## <span data-ttu-id="1b6b8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b6b8-123">OUTPUTS</span></span>

### <span data-ttu-id="1b6b8-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1b6b8-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="1b6b8-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b6b8-125">NOTES</span></span>

## <span data-ttu-id="1b6b8-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b6b8-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b6b8-127">Neu – AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="1b6b8-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
