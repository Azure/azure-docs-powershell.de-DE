---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997243"
---
# <span data-ttu-id="8a66b-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8a66b-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="8a66b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a66b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a66b-103">Erstellt ein VirtualHubRoute-Objekt, das als Parameter an den Befehl Add-AzVirtualHubRouteTable übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a66b-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="8a66b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a66b-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a66b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a66b-105">DESCRIPTION</span></span>
<span data-ttu-id="8a66b-106">Erstellt ein VirtualHubRoute-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a66b-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="8a66b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a66b-107">EXAMPLES</span></span>

### <span data-ttu-id="8a66b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a66b-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="8a66b-109">Der obige Befehl erstellt ein VirtualHubRoute-Objekt, das einer VirtualHubRouteTable-Ressource hinzugefügt und auf einen VirtualHub-Wert gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a66b-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="8a66b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a66b-110">PARAMETERS</span></span>

### <span data-ttu-id="8a66b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a66b-111">-DefaultProfile</span></span>
<span data-ttu-id="8a66b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a66b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a66b-113">-Ziel</span><span class="sxs-lookup"><span data-stu-id="8a66b-113">-Destination</span></span>
<span data-ttu-id="8a66b-114">Liste der Ziele.</span><span class="sxs-lookup"><span data-stu-id="8a66b-114">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a66b-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="8a66b-115">-DestinationType</span></span>
<span data-ttu-id="8a66b-116">Art der Ziele.</span><span class="sxs-lookup"><span data-stu-id="8a66b-116">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a66b-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="8a66b-117">-NextHop</span></span>
<span data-ttu-id="8a66b-118">Liste der nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="8a66b-118">List of Next hops.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a66b-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="8a66b-119">-NextHopType</span></span>
<span data-ttu-id="8a66b-120">Der nächste Hop-Typ.</span><span class="sxs-lookup"><span data-stu-id="8a66b-120">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a66b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a66b-121">CommonParameters</span></span>
<span data-ttu-id="8a66b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a66b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a66b-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a66b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a66b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a66b-124">INPUTS</span></span>

### <span data-ttu-id="8a66b-125">Keine</span><span class="sxs-lookup"><span data-stu-id="8a66b-125">None</span></span>

## <span data-ttu-id="8a66b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a66b-126">OUTPUTS</span></span>

### <span data-ttu-id="8a66b-127">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="8a66b-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="8a66b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a66b-128">NOTES</span></span>

## <span data-ttu-id="8a66b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a66b-129">RELATED LINKS</span></span>
