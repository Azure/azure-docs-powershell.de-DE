---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303736"
---
# <span data-ttu-id="8787d-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8787d-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="8787d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8787d-102">SYNOPSIS</span></span>
<span data-ttu-id="8787d-103">Erstellt eine virtuelle Hub-Route-Tabellen Ressource, die ein untergeordnetes Element von VirtualHub ist.</span><span class="sxs-lookup"><span data-stu-id="8787d-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="8787d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8787d-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8787d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8787d-105">DESCRIPTION</span></span>
<span data-ttu-id="8787d-106">Die Ressource für virtuelle Hub-Routingtabelle enthält die Liste der Routen sowie eine Liste der Verbindungen, an die Sie angefügt werden kann, und wird verwendet, um den Datenverkehr in einem virtuellen Hub weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="8787d-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="8787d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8787d-107">EXAMPLES</span></span>

### <span data-ttu-id="8787d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8787d-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="8787d-109">Mit dem obigen Befehl wird eine virtuelle Hub-Route-Tabellen Ressource aus den an Sie übergebenen Routen erstellt, und dieses Objekt kann zum Weiterleiten von Datenverkehr in einem virtuellen Hub verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8787d-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="8787d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8787d-110">PARAMETERS</span></span>

### <span data-ttu-id="8787d-111">-Connection</span><span class="sxs-lookup"><span data-stu-id="8787d-111">-Connection</span></span>
<span data-ttu-id="8787d-112">Liste der Verbindungen, an die diese Arbeitsplan Tabelle angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="8787d-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="8787d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8787d-113">-DefaultProfile</span></span>
<span data-ttu-id="8787d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8787d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8787d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8787d-115">-Name</span></span>
<span data-ttu-id="8787d-116">Name der Arbeitsplan Tabelle</span><span class="sxs-lookup"><span data-stu-id="8787d-116">Name of the route table.</span></span>

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

### <span data-ttu-id="8787d-117">-Route</span><span class="sxs-lookup"><span data-stu-id="8787d-117">-Route</span></span>
<span data-ttu-id="8787d-118">Liste der virtuellen Hub-Routen</span><span class="sxs-lookup"><span data-stu-id="8787d-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="8787d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8787d-119">CommonParameters</span></span>
<span data-ttu-id="8787d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8787d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8787d-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8787d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8787d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8787d-122">INPUTS</span></span>

### <span data-ttu-id="8787d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="8787d-123">None</span></span>

## <span data-ttu-id="8787d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8787d-124">OUTPUTS</span></span>

### <span data-ttu-id="8787d-125">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="8787d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="8787d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8787d-126">NOTES</span></span>

## <span data-ttu-id="8787d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8787d-127">RELATED LINKS</span></span>
