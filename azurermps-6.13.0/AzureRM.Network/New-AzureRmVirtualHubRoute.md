---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500190"
---
# <span data-ttu-id="b91a9-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b91a9-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="b91a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b91a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b91a9-103">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="b91a9-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b91a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b91a9-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b91a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b91a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b91a9-106">Erstellt ein Azure Virtual Hub-Routing Objekt.</span><span class="sxs-lookup"><span data-stu-id="b91a9-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="b91a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b91a9-107">EXAMPLES</span></span>

### <span data-ttu-id="b91a9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b91a9-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="b91a9-109">Das obige wird ein virtuelles Hub-Routing-Objekt erstellen, das in die virtuelle Hub-Route-Tabelle aufgenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b91a9-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="b91a9-110">Die virtuelle Hub-Route ist ein in-Memory-Objekt, das zum Erstellen eines VirtualHubRouteTable-Objekts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b91a9-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="b91a9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b91a9-111">PARAMETERS</span></span>

### <span data-ttu-id="b91a9-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b91a9-112">-AddressPrefix</span></span>
<span data-ttu-id="b91a9-113">Liste der Adresspräfixe</span><span class="sxs-lookup"><span data-stu-id="b91a9-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="b91a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91a9-114">-DefaultProfile</span></span>
<span data-ttu-id="b91a9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b91a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b91a9-116">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b91a9-116">-NextHopIpAddress</span></span>
<span data-ttu-id="b91a9-117">Die IPAddress für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b91a9-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="b91a9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91a9-118">CommonParameters</span></span>
<span data-ttu-id="b91a9-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b91a9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91a9-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91a9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91a9-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b91a9-121">INPUTS</span></span>

### <span data-ttu-id="b91a9-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b91a9-122">None</span></span>

## <span data-ttu-id="b91a9-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b91a9-123">OUTPUTS</span></span>

### <span data-ttu-id="b91a9-124">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="b91a9-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="b91a9-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b91a9-125">NOTES</span></span>

## <span data-ttu-id="b91a9-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b91a9-126">RELATED LINKS</span></span>
