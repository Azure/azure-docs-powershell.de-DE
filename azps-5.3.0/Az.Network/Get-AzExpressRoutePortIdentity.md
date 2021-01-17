---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 246675a2473bb20e5040f3898b6931f1b3ee6933
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469311"
---
# <span data-ttu-id="58b5e-101">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="58b5e-101">Get-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="58b5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="58b5e-103">Get identity assigned to an ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="58b5e-103">Get identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="58b5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58b5e-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="58b5e-106">Das **Cmdlet "Get-AzExpressRoutePortIdentity"** wird einem lokalen Azure ExpressRoutePort-Objekt zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="58b5e-106">The **Get-AzExpressRoutePortIdentity** cmdlet gets identity assigned to a local Azure ExpressRoutePort object.</span></span>

## <span data-ttu-id="58b5e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58b5e-107">EXAMPLES</span></span>

### <span data-ttu-id="58b5e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58b5e-108">Example 1</span></span>
```powershell
PS C:\> $exrPort = Get-AzExpressRoutePort -Name $exrPortName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzExpressRoutePortIdentity -ExpressRoutePort $exrPort
```

## <span data-ttu-id="58b5e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58b5e-109">PARAMETERS</span></span>

### <span data-ttu-id="58b5e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b5e-110">-DefaultProfile</span></span>
<span data-ttu-id="58b5e-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58b5e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58b5e-112">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="58b5e-112">-ExpressRoutePort</span></span>
<span data-ttu-id="58b5e-113">Der ExpressRoute-Port</span><span class="sxs-lookup"><span data-stu-id="58b5e-113">The ExpressRoute Port</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58b5e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b5e-114">CommonParameters</span></span>
<span data-ttu-id="58b5e-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b5e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b5e-116">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58b5e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b5e-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58b5e-117">INPUTS</span></span>

### <span data-ttu-id="58b5e-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="58b5e-118">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="58b5e-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58b5e-119">OUTPUTS</span></span>

### <span data-ttu-id="58b5e-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="58b5e-120">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="58b5e-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="58b5e-121">NOTES</span></span>

## <span data-ttu-id="58b5e-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="58b5e-122">RELATED LINKS</span></span>
[<span data-ttu-id="58b5e-123">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="58b5e-123">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="58b5e-124">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="58b5e-124">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="58b5e-125">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="58b5e-125">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)