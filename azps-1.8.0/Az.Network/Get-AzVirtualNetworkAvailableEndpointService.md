---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660691"
---
# <span data-ttu-id="53698-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="53698-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="53698-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53698-102">SYNOPSIS</span></span>
<span data-ttu-id="53698-103">Listet verfügbare Endpunkt Dienste für den Standort auf.</span><span class="sxs-lookup"><span data-stu-id="53698-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="53698-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53698-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53698-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53698-105">DESCRIPTION</span></span>
<span data-ttu-id="53698-106">Get-AzVirtualNetworkAvailableEndpointService listet die am angegebenen Speicherort verfügbaren Endpunkt Dienste auf.</span><span class="sxs-lookup"><span data-stu-id="53698-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="53698-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53698-107">EXAMPLES</span></span>

### <span data-ttu-id="53698-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53698-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="53698-109">Ruft verfügbare Endpunkt Dienste in westus-Region ab.</span><span class="sxs-lookup"><span data-stu-id="53698-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="53698-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="53698-110">PARAMETERS</span></span>

### <span data-ttu-id="53698-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53698-111">-DefaultProfile</span></span>
<span data-ttu-id="53698-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53698-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53698-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="53698-113">-Location</span></span>
<span data-ttu-id="53698-114">Der Speicherort, aus dem die Endpunkt Dienste abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="53698-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="53698-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53698-115">CommonParameters</span></span>
<span data-ttu-id="53698-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53698-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53698-117">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53698-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53698-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53698-118">INPUTS</span></span>

### <span data-ttu-id="53698-119">System. String</span><span class="sxs-lookup"><span data-stu-id="53698-119">System.String</span></span>

## <span data-ttu-id="53698-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53698-120">OUTPUTS</span></span>

### <span data-ttu-id="53698-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="53698-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="53698-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="53698-122">NOTES</span></span>

## <span data-ttu-id="53698-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53698-123">RELATED LINKS</span></span>
