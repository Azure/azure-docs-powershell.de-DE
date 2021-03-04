---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926523"
---
# <span data-ttu-id="c4c85-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4c85-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c4c85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c85-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c85-103">Ruft eine Azure ExpressRoute-Querverbindung aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="c4c85-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="c4c85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4c85-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4c85-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4c85-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c85-106">Das **Get-AzExpressRouteCrossConnection-Cmdlet** wird verwendet, um ein ExpressRoute-Verbindungsobjekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c4c85-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="c4c85-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4c85-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c4c85-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4c85-108">EXAMPLES</span></span>

### <span data-ttu-id="c4c85-109">Beispiel 1: Herstellen der ExpressRoute-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="c4c85-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="c4c85-110">Beispiel 2: Auflisten der ExpressRoute-Verbindungen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="c4c85-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="c4c85-111">In diesem Cmdlet werden alle ExpressRoute-Kreuzverbindungen aufgeführt, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="c4c85-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="c4c85-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4c85-112">PARAMETERS</span></span>

### <span data-ttu-id="c4c85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c85-113">-DefaultProfile</span></span>
<span data-ttu-id="c4c85-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4c85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4c85-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c4c85-115">-Name</span></span>
<span data-ttu-id="c4c85-116">Der Name der ExpressRoute-Querverbindung.</span><span class="sxs-lookup"><span data-stu-id="c4c85-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c4c85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4c85-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4c85-118">Der Name der Ressourcengruppe, die die ExpressRoute-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="c4c85-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="c4c85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c85-119">CommonParameters</span></span>
<span data-ttu-id="c4c85-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c85-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4c85-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c85-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4c85-122">INPUTS</span></span>

### <span data-ttu-id="c4c85-123">Keine</span><span class="sxs-lookup"><span data-stu-id="c4c85-123">None</span></span>
<span data-ttu-id="c4c85-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c4c85-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4c85-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4c85-125">OUTPUTS</span></span>

### <span data-ttu-id="c4c85-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4c85-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c4c85-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c4c85-127">NOTES</span></span>

## <span data-ttu-id="c4c85-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c4c85-128">RELATED LINKS</span></span>

[<span data-ttu-id="c4c85-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c4c85-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)