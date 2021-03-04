---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: a1c28622a4bb3a43d9d91b2f991c402a3572a3f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924768"
---
# <span data-ttu-id="5f416-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="5f416-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="5f416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f416-102">SYNOPSIS</span></span>
<span data-ttu-id="5f416-103">Listet die verfügbaren Endpunktdienste für den Standort auf.</span><span class="sxs-lookup"><span data-stu-id="5f416-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="5f416-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f416-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f416-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5f416-105">DESCRIPTION</span></span>
<span data-ttu-id="5f416-106">Get-AzVirtualNetworkAvailableEndpointService listet Endpunktdienste auf, die am angegebenen Speicherort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5f416-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="5f416-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5f416-107">EXAMPLES</span></span>

### <span data-ttu-id="5f416-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5f416-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="5f416-109">Ruft verfügbare Endpunktdienste in der Region Westus ab.</span><span class="sxs-lookup"><span data-stu-id="5f416-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="5f416-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5f416-110">PARAMETERS</span></span>

### <span data-ttu-id="5f416-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f416-111">-DefaultProfile</span></span>
<span data-ttu-id="5f416-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f416-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f416-113">-Location</span><span class="sxs-lookup"><span data-stu-id="5f416-113">-Location</span></span>
<span data-ttu-id="5f416-114">Der Speicherort zum Abrufen der Endpunktdienste.</span><span class="sxs-lookup"><span data-stu-id="5f416-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f416-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f416-115">CommonParameters</span></span>
<span data-ttu-id="5f416-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f416-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f416-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f416-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f416-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5f416-118">INPUTS</span></span>

### <span data-ttu-id="5f416-119">System.String</span><span class="sxs-lookup"><span data-stu-id="5f416-119">System.String</span></span>

## <span data-ttu-id="5f416-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5f416-120">OUTPUTS</span></span>

### <span data-ttu-id="5f416-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="5f416-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="5f416-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5f416-122">NOTES</span></span>

## <span data-ttu-id="5f416-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5f416-123">RELATED LINKS</span></span>
