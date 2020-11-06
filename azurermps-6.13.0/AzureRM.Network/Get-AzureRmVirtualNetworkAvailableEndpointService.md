---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 7499c96ec887673faaf93cf2901e4705b63604b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505745"
---
# <span data-ttu-id="c0818-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="c0818-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="c0818-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0818-102">SYNOPSIS</span></span>
<span data-ttu-id="c0818-103">Listet verfügbare Endpunkt Dienste für den Standort auf.</span><span class="sxs-lookup"><span data-stu-id="c0818-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0818-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0818-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0818-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0818-105">DESCRIPTION</span></span>
<span data-ttu-id="c0818-106">Get-AzureRmVirtualNetworkAvailableEndpointService listet die am angegebenen Speicherort verfügbaren Endpunkt Dienste auf.</span><span class="sxs-lookup"><span data-stu-id="c0818-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="c0818-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0818-107">EXAMPLES</span></span>

### <span data-ttu-id="c0818-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0818-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="c0818-109">Ruft verfügbare Endpunkt Dienste in westus-Region ab.</span><span class="sxs-lookup"><span data-stu-id="c0818-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="c0818-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0818-110">PARAMETERS</span></span>

### <span data-ttu-id="c0818-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0818-111">-DefaultProfile</span></span>
<span data-ttu-id="c0818-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0818-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0818-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="c0818-113">-Location</span></span>
<span data-ttu-id="c0818-114">Der Speicherort, aus dem die Endpunkt Dienste abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0818-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="c0818-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0818-115">CommonParameters</span></span>
<span data-ttu-id="c0818-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0818-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0818-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0818-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0818-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0818-118">INPUTS</span></span>

### <span data-ttu-id="c0818-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c0818-119">System.String</span></span>

## <span data-ttu-id="c0818-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0818-120">OUTPUTS</span></span>

### <span data-ttu-id="c0818-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="c0818-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="c0818-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0818-122">NOTES</span></span>

## <span data-ttu-id="c0818-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0818-123">RELATED LINKS</span></span>
