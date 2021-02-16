---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160793"
---
# <span data-ttu-id="7ba20-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7ba20-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="7ba20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba20-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba20-103">Erstellt ein Azure Virtual Hub Route-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba20-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="7ba20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ba20-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba20-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ba20-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba20-106">Erstellt ein Azure Virtual Hub Route-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba20-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="7ba20-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7ba20-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ba20-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="7ba20-109">Im vorstehenden Beispiel wird ein virtuelles Hubroutenobjekt erstellt, das in der Tabelle für die virtuelle Hubroute enthalten sein kann.</span><span class="sxs-lookup"><span data-stu-id="7ba20-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="7ba20-110">Die virtuelle Hubroute ist ein Speicherobjekt, das zum Erstellen eines VirtualHubRouteTable-Objekts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ba20-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="7ba20-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ba20-111">PARAMETERS</span></span>

### <span data-ttu-id="7ba20-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7ba20-112">-AddressPrefix</span></span>
<span data-ttu-id="7ba20-113">Liste der Adresspräfixe.</span><span class="sxs-lookup"><span data-stu-id="7ba20-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="7ba20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba20-114">-DefaultProfile</span></span>
<span data-ttu-id="7ba20-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ba20-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba20-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ba20-116">-NextHopIpAddress</span></span>
<span data-ttu-id="7ba20-117">Die IpAddress des nächsten Hops.</span><span class="sxs-lookup"><span data-stu-id="7ba20-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="7ba20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba20-118">CommonParameters</span></span>
<span data-ttu-id="7ba20-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba20-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba20-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba20-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7ba20-121">INPUTS</span></span>

### <span data-ttu-id="7ba20-122">Keine</span><span class="sxs-lookup"><span data-stu-id="7ba20-122">None</span></span>

## <span data-ttu-id="7ba20-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7ba20-123">OUTPUTS</span></span>

### <span data-ttu-id="7ba20-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7ba20-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="7ba20-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7ba20-125">NOTES</span></span>

## <span data-ttu-id="7ba20-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7ba20-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ba20-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7ba20-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
