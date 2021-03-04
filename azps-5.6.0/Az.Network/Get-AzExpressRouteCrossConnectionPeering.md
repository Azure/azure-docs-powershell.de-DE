---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 415c084ebf6c1c83872a16d01ce4eb556f688103
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932424"
---
# <span data-ttu-id="0c511-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c511-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="0c511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c511-102">SYNOPSIS</span></span>
<span data-ttu-id="0c511-103">Ruft eine ExpressRoute-Verbindungs-Peeringkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="0c511-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="0c511-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c511-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c511-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c511-105">DESCRIPTION</span></span>
<span data-ttu-id="0c511-106">Das **Get-AzExpressRouteCrossConnectionPeering-Cmdlet** ruft die Konfiguration einer Peeringbeziehung für eine ExpressRoute-Kreuzverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="0c511-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0c511-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c511-107">EXAMPLES</span></span>

### <span data-ttu-id="0c511-108">Beispiel 1: Anzeigen der Peeringkonfiguration für eine ExpressRoute-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="0c511-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="0c511-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c511-109">PARAMETERS</span></span>

### <span data-ttu-id="0c511-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c511-110">-DefaultProfile</span></span>
<span data-ttu-id="0c511-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c511-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c511-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c511-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0c511-113">Das ExpressRoute-Verbindungsobjekt, das die Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0c511-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

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

### <span data-ttu-id="0c511-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0c511-114">-Name</span></span>
<span data-ttu-id="0c511-115">Der Name der abzurufenden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c511-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="0c511-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c511-116">CommonParameters</span></span>
<span data-ttu-id="0c511-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c511-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c511-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c511-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c511-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c511-119">INPUTS</span></span>

### <span data-ttu-id="0c511-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c511-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="0c511-121">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c511-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="0c511-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c511-122">OUTPUTS</span></span>

### <span data-ttu-id="0c511-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="0c511-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="0c511-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0c511-124">NOTES</span></span>

## <span data-ttu-id="0c511-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0c511-125">RELATED LINKS</span></span>

[<span data-ttu-id="0c511-126">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c511-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="0c511-127">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="0c511-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="0c511-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c511-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="0c511-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0c511-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
