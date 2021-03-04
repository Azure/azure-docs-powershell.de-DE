---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921104"
---
# <span data-ttu-id="edf2f-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="edf2f-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="edf2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf2f-102">SYNOPSIS</span></span>
<span data-ttu-id="edf2f-103">Ruft die Speicherorte ab, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="edf2f-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="edf2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edf2f-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="edf2f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edf2f-105">DESCRIPTION</span></span>
<span data-ttu-id="edf2f-106">Das **Get-AzExpressRoutePortsLocation-Cmdlet** wird verwendet, um die Speicherorte abzurufen, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="edf2f-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="edf2f-107">Bei einer bestimmten Position als Eingabe zeigt das Cmdlet die Details dieses Speicherorts an, d. h. eine Liste der verfügbaren Bandbreiten an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="edf2f-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="edf2f-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edf2f-108">EXAMPLES</span></span>

### <span data-ttu-id="edf2f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="edf2f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="edf2f-110">Listet die Speicherorte auf, an denen ExpressRoutePort-Ressourcen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="edf2f-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="edf2f-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="edf2f-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="edf2f-112">Listet die expressRoutePort-Bandbreiten auf, die am Standort $loc.</span><span class="sxs-lookup"><span data-stu-id="edf2f-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="edf2f-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="edf2f-113">PARAMETERS</span></span>

### <span data-ttu-id="edf2f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf2f-114">-DefaultProfile</span></span>
<span data-ttu-id="edf2f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edf2f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf2f-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="edf2f-116">-LocationName</span></span>
<span data-ttu-id="edf2f-117">Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="edf2f-117">The name of the location.</span></span>

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

### <span data-ttu-id="edf2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf2f-118">CommonParameters</span></span>
<span data-ttu-id="edf2f-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf2f-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edf2f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf2f-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edf2f-121">INPUTS</span></span>

### <span data-ttu-id="edf2f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="edf2f-122">System.String</span></span>

## <span data-ttu-id="edf2f-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edf2f-123">OUTPUTS</span></span>

### <span data-ttu-id="edf2f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="edf2f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="edf2f-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="edf2f-125">NOTES</span></span>

## <span data-ttu-id="edf2f-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="edf2f-126">RELATED LINKS</span></span>
