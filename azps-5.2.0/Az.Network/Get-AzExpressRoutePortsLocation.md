---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296644"
---
# <span data-ttu-id="32580-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="32580-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="32580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32580-102">SYNOPSIS</span></span>
<span data-ttu-id="32580-103">Ruft die Speicherorte ab, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32580-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="32580-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32580-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32580-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="32580-105">DESCRIPTION</span></span>
<span data-ttu-id="32580-106">Das **Cmdlet "Get-AzExpressRoutePortsLocation"** wird verwendet, um die Speicherorte abzurufen, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32580-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="32580-107">An einer bestimmten Position als Eingabe zeigt das Cmdlet die Details dieses Speicherorts an, d. h. eine Liste der verfügbaren Bandbreiten an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="32580-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="32580-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="32580-108">EXAMPLES</span></span>

### <span data-ttu-id="32580-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32580-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="32580-110">Listet die Speicherorte auf, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="32580-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="32580-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32580-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="32580-112">Listet die expressRoutePort-Bandbreiten auf, die am Standort $loc.</span><span class="sxs-lookup"><span data-stu-id="32580-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="32580-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32580-113">PARAMETERS</span></span>

### <span data-ttu-id="32580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32580-114">-DefaultProfile</span></span>
<span data-ttu-id="32580-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32580-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32580-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="32580-116">-LocationName</span></span>
<span data-ttu-id="32580-117">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="32580-117">The name of the location.</span></span>

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

### <span data-ttu-id="32580-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32580-118">CommonParameters</span></span>
<span data-ttu-id="32580-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32580-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32580-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32580-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32580-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="32580-121">INPUTS</span></span>

### <span data-ttu-id="32580-122">System.String</span><span class="sxs-lookup"><span data-stu-id="32580-122">System.String</span></span>

## <span data-ttu-id="32580-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="32580-123">OUTPUTS</span></span>

### <span data-ttu-id="32580-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="32580-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="32580-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="32580-125">NOTES</span></span>

## <span data-ttu-id="32580-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="32580-126">RELATED LINKS</span></span>
