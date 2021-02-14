---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 15aed0e5a4cca1b67c85cbe651453d64cecc13ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154425"
---
# <span data-ttu-id="263d0-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="263d0-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="263d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="263d0-102">SYNOPSIS</span></span>
<span data-ttu-id="263d0-103">Ruft eine ExpressRoute-übergreifende Peeringkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="263d0-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="263d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="263d0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="263d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="263d0-105">DESCRIPTION</span></span>
<span data-ttu-id="263d0-106">Das **Cmdlet "Get-AzExpressRouteCrossConnectionPeering"** ruft die Konfiguration einer Peeringbeziehung für eine ExpressRoute-Kreuzverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="263d0-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="263d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="263d0-107">EXAMPLES</span></span>

### <span data-ttu-id="263d0-108">Beispiel 1: Anzeigen der Peeringkonfiguration für eine ExpressRoute-Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="263d0-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="263d0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="263d0-109">PARAMETERS</span></span>

### <span data-ttu-id="263d0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263d0-110">-DefaultProfile</span></span>
<span data-ttu-id="263d0-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="263d0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="263d0-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="263d0-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="263d0-113">Das ExpressRoute-Kreuzverbindungsobjekt, das die Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="263d0-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263d0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="263d0-114">-Name</span></span>
<span data-ttu-id="263d0-115">Der Name der abzurufenden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="263d0-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263d0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263d0-116">CommonParameters</span></span>
<span data-ttu-id="263d0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263d0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263d0-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="263d0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263d0-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="263d0-119">INPUTS</span></span>

### <span data-ttu-id="263d0-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="263d0-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="263d0-121">Der Parameter 'ExpressRouteCrossConnection' akzeptiert den Wert des Typs 'PSExpressRouteCrossConnection' aus der Pipeline</span><span class="sxs-lookup"><span data-stu-id="263d0-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="263d0-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="263d0-122">OUTPUTS</span></span>

### <span data-ttu-id="263d0-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="263d0-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="263d0-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="263d0-124">NOTES</span></span>

## <span data-ttu-id="263d0-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="263d0-125">RELATED LINKS</span></span>

[<span data-ttu-id="263d0-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="263d0-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="263d0-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="263d0-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="263d0-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="263d0-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="263d0-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="263d0-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
