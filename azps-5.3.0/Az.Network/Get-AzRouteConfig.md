---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 0d941289f0798854a3647bcb5fbf4d1e6be1053d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472602"
---
# <span data-ttu-id="d69cb-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d69cb-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="d69cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d69cb-102">SYNOPSIS</span></span>
<span data-ttu-id="d69cb-103">Ruft Routen aus einer Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d69cb-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="d69cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d69cb-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d69cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d69cb-105">DESCRIPTION</span></span>
<span data-ttu-id="d69cb-106">Das **Cmdlet "Get-AzRouteConfig"** ruft Routen aus einer Azure-Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="d69cb-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="d69cb-107">Sie können eine Route nach Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="d69cb-107">You can specify a route by name.</span></span>

## <span data-ttu-id="d69cb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d69cb-108">EXAMPLES</span></span>

### <span data-ttu-id="d69cb-109">Beispiel 1: Erstellen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="d69cb-109">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Get-AzRouteConfig -Name "Route07"
Name              : route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="d69cb-110">Dieser Befehl ruft die Routentabelle mit dem Cmdlet **"Get-AzRouteTable"** mit dem Namen "RouteTable01" ab.</span><span class="sxs-lookup"><span data-stu-id="d69cb-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="d69cb-111">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d69cb-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d69cb-112">Das aktuelle Cmdlet ruft die Route namens "Route07" in der Routentabelle mit dem Namen "RouteTable01" ab.</span><span class="sxs-lookup"><span data-stu-id="d69cb-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="d69cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d69cb-113">PARAMETERS</span></span>

### <span data-ttu-id="d69cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69cb-114">-DefaultProfile</span></span>
<span data-ttu-id="d69cb-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d69cb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d69cb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d69cb-116">-Name</span></span>
<span data-ttu-id="d69cb-117">Gibt den Namen der Route an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="d69cb-117">Specifies the name of the route that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69cb-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="d69cb-118">-RouteTable</span></span>
<span data-ttu-id="d69cb-119">Gibt die Routentabelle an, aus der dieses Cmdlet Routen erhält.</span><span class="sxs-lookup"><span data-stu-id="d69cb-119">Specifies the route table from which this cmdlet gets routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d69cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69cb-120">CommonParameters</span></span>
<span data-ttu-id="d69cb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69cb-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d69cb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69cb-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d69cb-123">INPUTS</span></span>

### <span data-ttu-id="d69cb-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="d69cb-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="d69cb-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d69cb-125">OUTPUTS</span></span>

### <span data-ttu-id="d69cb-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="d69cb-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="d69cb-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d69cb-127">NOTES</span></span>

## <span data-ttu-id="d69cb-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d69cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="d69cb-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d69cb-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="d69cb-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="d69cb-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="d69cb-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d69cb-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="d69cb-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d69cb-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="d69cb-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="d69cb-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


