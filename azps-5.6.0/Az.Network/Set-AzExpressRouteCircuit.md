---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 71571d9fe6eccee73efda01015a877014c67c9ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918643"
---
# <span data-ttu-id="7fca2-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="7fca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fca2-102">SYNOPSIS</span></span>
<span data-ttu-id="7fca2-103">Ändert einen ExpressRoute-Schaltkreis.</span><span class="sxs-lookup"><span data-stu-id="7fca2-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7fca2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fca2-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fca2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fca2-105">DESCRIPTION</span></span>
<span data-ttu-id="7fca2-106">Das **Cmdlet Set-AzExpressRouteCircuit** speichert den geänderten ExpressRoute-Schaltkreis in Azure.</span><span class="sxs-lookup"><span data-stu-id="7fca2-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="7fca2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7fca2-107">EXAMPLES</span></span>

### <span data-ttu-id="7fca2-108">Beispiel 1: Ändern des Dienstschlüssels eines ExpressRoute-Schaltkreises</span><span class="sxs-lookup"><span data-stu-id="7fca2-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="7fca2-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7fca2-109">PARAMETERS</span></span>

### <span data-ttu-id="7fca2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fca2-110">-AsJob</span></span>
<span data-ttu-id="7fca2-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7fca2-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fca2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fca2-112">-DefaultProfile</span></span>
<span data-ttu-id="7fca2-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fca2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fca2-114">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7fca2-115">Gibt das **ExpressRouteCircuit-Objekt** an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7fca2-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fca2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fca2-116">CommonParameters</span></span>
<span data-ttu-id="7fca2-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fca2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fca2-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fca2-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fca2-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7fca2-119">INPUTS</span></span>

### <span data-ttu-id="7fca2-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7fca2-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7fca2-121">OUTPUTS</span></span>

### <span data-ttu-id="7fca2-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7fca2-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7fca2-123">NOTES</span></span>

## <span data-ttu-id="7fca2-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7fca2-124">RELATED LINKS</span></span>

[<span data-ttu-id="7fca2-125">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7fca2-126">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="7fca2-127">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="7fca2-128">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7fca2-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
