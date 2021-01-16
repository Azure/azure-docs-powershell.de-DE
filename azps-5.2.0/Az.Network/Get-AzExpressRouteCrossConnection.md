---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293387"
---
# <span data-ttu-id="cf3cf-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf3cf-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cf3cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf3cf-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3cf-103">Ruft eine Azure -ExpressRoute-Kreuzverbindung aus Azure ab.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="cf3cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf3cf-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3cf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cf3cf-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3cf-106">Das **Cmdlet "Get-AzExpressRouteCrossConnection"** wird verwendet, um ein ExpressRoute-Verbindungsobjekt aus Ihrem Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="cf3cf-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf3cf-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cf3cf-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cf3cf-108">EXAMPLES</span></span>

### <span data-ttu-id="cf3cf-109">Beispiel 1: Herstellen der ExpressRoute-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="cf3cf-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="cf3cf-110">Beispiel 2: Auflisten der ExpressRoute-Kreuzverbindungen mithilfe eines Filters</span><span class="sxs-lookup"><span data-stu-id="cf3cf-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="cf3cf-111">Dieses Cmdlet listet alle ExpressRoute-Kreuzverbindungen auf, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="cf3cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf3cf-112">PARAMETERS</span></span>

### <span data-ttu-id="cf3cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3cf-113">-DefaultProfile</span></span>
<span data-ttu-id="cf3cf-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3cf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cf3cf-115">-Name</span></span>
<span data-ttu-id="cf3cf-116">Der Name der ExpressRoute-Kreuzverbindung.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="cf3cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf3cf-118">Der Name der Ressourcengruppe, die die ExpressRoute-Kreuzverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="cf3cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3cf-119">CommonParameters</span></span>
<span data-ttu-id="cf3cf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3cf-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf3cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3cf-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3cf-122">INPUTS</span></span>

### <span data-ttu-id="cf3cf-123">Keine</span><span class="sxs-lookup"><span data-stu-id="cf3cf-123">None</span></span>
<span data-ttu-id="cf3cf-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cf3cf-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf3cf-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cf3cf-125">OUTPUTS</span></span>

### <span data-ttu-id="cf3cf-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf3cf-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="cf3cf-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cf3cf-127">NOTES</span></span>

## <span data-ttu-id="cf3cf-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cf3cf-128">RELATED LINKS</span></span>

[<span data-ttu-id="cf3cf-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="cf3cf-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)