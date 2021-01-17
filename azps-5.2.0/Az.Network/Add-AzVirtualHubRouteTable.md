---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359693"
---
# <span data-ttu-id="a6f5c-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6f5c-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="a6f5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6f5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f5c-103">Erstellt eine Ressource der Virtuellen Hubroute-Tabelle, die ein untergeordnetes Teil von VirtualHub ist.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="a6f5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6f5c-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f5c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6f5c-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f5c-106">Die Ressource für die Tabelle für virtuelle Hubrouten enthält die Liste der Routen und eine Liste der Verbindungen, an die sie angefügt werden kann und die zum Routen von Datenverkehr in einem virtuellen Hub verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="a6f5c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6f5c-107">EXAMPLES</span></span>

### <span data-ttu-id="a6f5c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6f5c-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="a6f5c-109">Mit dem oben angegebenen Befehl wird eine Ressource der Tabelle "Virtual Hub Route" aus den an sie übergebenen Routen erstellt, und dieses Objekt kann für das Routing von Datenverkehr in einem virtuellen Hub verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="a6f5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6f5c-110">PARAMETERS</span></span>

### <span data-ttu-id="a6f5c-111">-Connection</span><span class="sxs-lookup"><span data-stu-id="a6f5c-111">-Connection</span></span>
<span data-ttu-id="a6f5c-112">Liste der Verbindungen, an die diese Routentabelle angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="a6f5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f5c-113">-DefaultProfile</span></span>
<span data-ttu-id="a6f5c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f5c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a6f5c-115">-Name</span></span>
<span data-ttu-id="a6f5c-116">Name der Routentabelle.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-116">Name of the route table.</span></span>

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

### <span data-ttu-id="a6f5c-117">-Route</span><span class="sxs-lookup"><span data-stu-id="a6f5c-117">-Route</span></span>
<span data-ttu-id="a6f5c-118">Liste der virtuellen Hubrouten.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6f5c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f5c-119">CommonParameters</span></span>
<span data-ttu-id="a6f5c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f5c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f5c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6f5c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f5c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6f5c-122">INPUTS</span></span>

### <span data-ttu-id="a6f5c-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a6f5c-123">None</span></span>

## <span data-ttu-id="a6f5c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6f5c-124">OUTPUTS</span></span>

### <span data-ttu-id="a6f5c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6f5c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="a6f5c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6f5c-126">NOTES</span></span>

## <span data-ttu-id="a6f5c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6f5c-127">RELATED LINKS</span></span>
