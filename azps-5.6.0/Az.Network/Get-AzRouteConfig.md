---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DBD40431-DD7A-42CB-83AA-568B1065A468
online version: https://docs.microsoft.com/powershell/module/az.network/get-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteConfig.md
ms.openlocfilehash: 892d160decb7bc595e25f2f0512996fe2bdce5da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919664"
---
# <span data-ttu-id="5a307-101">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a307-101">Get-AzRouteConfig</span></span>

## <span data-ttu-id="5a307-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a307-102">SYNOPSIS</span></span>
<span data-ttu-id="5a307-103">Ruft Routen aus einer Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="5a307-103">Gets routes from a route table.</span></span>

## <span data-ttu-id="5a307-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a307-104">SYNTAX</span></span>

```
Get-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a307-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a307-105">DESCRIPTION</span></span>
<span data-ttu-id="5a307-106">Das **Get-AzRouteConfig-Cmdlet** ruft Routen aus einer Azure-Routentabelle ab.</span><span class="sxs-lookup"><span data-stu-id="5a307-106">The **Get-AzRouteConfig** cmdlet gets routes from an Azure route table.</span></span>
<span data-ttu-id="5a307-107">Sie können eine Route nach Name angeben.</span><span class="sxs-lookup"><span data-stu-id="5a307-107">You can specify a route by name.</span></span>

## <span data-ttu-id="5a307-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a307-108">EXAMPLES</span></span>

### <span data-ttu-id="5a307-109">Beispiel 1: Erstellen einer Routentabelle</span><span class="sxs-lookup"><span data-stu-id="5a307-109">Example 1: Get a route table</span></span>
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

<span data-ttu-id="5a307-110">Dieser Befehl ruft die Routentabelle mit dem Namen RouteTable01 mithilfe des **Get-AzRouteTable-Cmdlets** ab.</span><span class="sxs-lookup"><span data-stu-id="5a307-110">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="5a307-111">Der Befehl übergibt diese Tabelle mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a307-111">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5a307-112">Das aktuelle Cmdlet ruft die Route mit dem Namen Route07 in der Routentabelle mit dem Namen RouteTable01 ab.</span><span class="sxs-lookup"><span data-stu-id="5a307-112">The current cmdlet gets the route named Route07 in the route table named RouteTable01.</span></span>

## <span data-ttu-id="5a307-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5a307-113">PARAMETERS</span></span>

### <span data-ttu-id="5a307-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a307-114">-DefaultProfile</span></span>
<span data-ttu-id="5a307-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5a307-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a307-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5a307-116">-Name</span></span>
<span data-ttu-id="5a307-117">Gibt den Namen der Route an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5a307-117">Specifies the name of the route that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5a307-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5a307-118">-RouteTable</span></span>
<span data-ttu-id="5a307-119">Gibt die Routentabelle an, aus der dieses Cmdlet Routen erhält.</span><span class="sxs-lookup"><span data-stu-id="5a307-119">Specifies the route table from which this cmdlet gets routes.</span></span>

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

### <span data-ttu-id="5a307-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a307-120">CommonParameters</span></span>
<span data-ttu-id="5a307-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a307-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a307-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a307-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a307-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a307-123">INPUTS</span></span>

### <span data-ttu-id="5a307-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a307-124">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="5a307-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a307-125">OUTPUTS</span></span>

### <span data-ttu-id="5a307-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span><span class="sxs-lookup"><span data-stu-id="5a307-126">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="5a307-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5a307-127">NOTES</span></span>

## <span data-ttu-id="5a307-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5a307-128">RELATED LINKS</span></span>

[<span data-ttu-id="5a307-129">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a307-129">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="5a307-130">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a307-130">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="5a307-131">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a307-131">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="5a307-132">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a307-132">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="5a307-133">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="5a307-133">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


