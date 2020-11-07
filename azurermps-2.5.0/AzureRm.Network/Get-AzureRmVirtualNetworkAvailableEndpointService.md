---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848772"
---
# <span data-ttu-id="61d10-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="61d10-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="61d10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61d10-102">SYNOPSIS</span></span>
<span data-ttu-id="61d10-103">Listet verfügbare Endpunkt Dienste für den Standort auf.</span><span class="sxs-lookup"><span data-stu-id="61d10-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61d10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61d10-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61d10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61d10-105">DESCRIPTION</span></span>
<span data-ttu-id="61d10-106">Get-AzureRmVirtualNetworkAvailableEndpointService listet die am angegebenen Speicherort verfügbaren Endpunkt Dienste auf.</span><span class="sxs-lookup"><span data-stu-id="61d10-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="61d10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61d10-107">EXAMPLES</span></span>

### <span data-ttu-id="61d10-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61d10-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="61d10-109">Ruft verfügbare Endpunkt Dienste in westus-Region ab.</span><span class="sxs-lookup"><span data-stu-id="61d10-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="61d10-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61d10-110">PARAMETERS</span></span>

### <span data-ttu-id="61d10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d10-111">-DefaultProfile</span></span>
<span data-ttu-id="61d10-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61d10-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61d10-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="61d10-113">-Location</span></span>
<span data-ttu-id="61d10-114">Der Speicherort, aus dem die Endpunkt Dienste abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61d10-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61d10-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d10-115">CommonParameters</span></span>
<span data-ttu-id="61d10-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d10-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d10-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61d10-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d10-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61d10-118">INPUTS</span></span>

### <span data-ttu-id="61d10-119">System. String</span><span class="sxs-lookup"><span data-stu-id="61d10-119">System.String</span></span>

## <span data-ttu-id="61d10-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61d10-120">OUTPUTS</span></span>

### <span data-ttu-id="61d10-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="61d10-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="61d10-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="61d10-122">NOTES</span></span>

## <span data-ttu-id="61d10-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61d10-123">RELATED LINKS</span></span>

