---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178737"
---
# <span data-ttu-id="2072f-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2072f-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="2072f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2072f-102">SYNOPSIS</span></span>
<span data-ttu-id="2072f-103">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="2072f-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="2072f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2072f-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2072f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2072f-105">DESCRIPTION</span></span>
<span data-ttu-id="2072f-106">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="2072f-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="2072f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2072f-107">EXAMPLES</span></span>

### <span data-ttu-id="2072f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2072f-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="2072f-109">Das obige wird ein virtuelles Hub-Routing-Objekt erstellen, das in die virtuelle Hub-Route-Tabelle aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2072f-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="2072f-110">Die virtuelle Hub-Route ist ein in-Memory-Objekt, das zum Erstellen eines VirtualHubRouteTable-Objekts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2072f-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="2072f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2072f-111">PARAMETERS</span></span>

### <span data-ttu-id="2072f-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2072f-112">-AddressPrefix</span></span>
<span data-ttu-id="2072f-113">Liste der Adresspräfixe</span><span class="sxs-lookup"><span data-stu-id="2072f-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="2072f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2072f-114">-DefaultProfile</span></span>
<span data-ttu-id="2072f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2072f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2072f-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="2072f-116">-NextHopIpAddress</span></span>
<span data-ttu-id="2072f-117">Die IPAddress für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="2072f-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="2072f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2072f-118">CommonParameters</span></span>
<span data-ttu-id="2072f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2072f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2072f-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2072f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2072f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2072f-121">INPUTS</span></span>

### <span data-ttu-id="2072f-122">Keine</span><span class="sxs-lookup"><span data-stu-id="2072f-122">None</span></span>

## <span data-ttu-id="2072f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2072f-123">OUTPUTS</span></span>

### <span data-ttu-id="2072f-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2072f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="2072f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="2072f-125">NOTES</span></span>

## <span data-ttu-id="2072f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2072f-126">RELATED LINKS</span></span>

[<span data-ttu-id="2072f-127">Neu – AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2072f-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
