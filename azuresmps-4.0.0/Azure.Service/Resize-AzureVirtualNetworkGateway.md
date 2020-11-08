---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AD5F4D69-45AF-46FB-ADF0-59CEF9908EF7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d63ac418d2dcee97afef9ae5f351fb2c1eebece0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006292"
---
# <span data-ttu-id="db770-101">Resize-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db770-101">Resize-AzureVirtualNetworkGateway</span></span>

## <span data-ttu-id="db770-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db770-102">SYNOPSIS</span></span>
<span data-ttu-id="db770-103">Ändert die Größe eines virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="db770-103">Resizes a virtual network gateway.</span></span>

## <span data-ttu-id="db770-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db770-104">SYNTAX</span></span>

```
Resize-AzureVirtualNetworkGateway -GatewayId <String> -GatewaySKU <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="db770-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db770-105">DESCRIPTION</span></span>
<span data-ttu-id="db770-106">Das Resize-AzureVirtualNetworkGateway-Cmdlet ändert die Größe eines virtuellen Netzwerkgateways.</span><span class="sxs-lookup"><span data-stu-id="db770-106">The Resize-AzureVirtualNetworkGateway cmdlet resizes a virtual network gateway.</span></span>

## <span data-ttu-id="db770-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db770-107">EXAMPLES</span></span>

## <span data-ttu-id="db770-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db770-108">PARAMETERS</span></span>

### <span data-ttu-id="db770-109">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="db770-109">-GatewayId</span></span>
<span data-ttu-id="db770-110">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="db770-110">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db770-111">-GatewaySKU</span><span class="sxs-lookup"><span data-stu-id="db770-111">-GatewaySKU</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db770-112">-Profil</span><span class="sxs-lookup"><span data-stu-id="db770-112">-Profile</span></span>
<span data-ttu-id="db770-113">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="db770-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="db770-114">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="db770-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db770-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db770-115">CommonParameters</span></span>
<span data-ttu-id="db770-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db770-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db770-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db770-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db770-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db770-118">INPUTS</span></span>

## <span data-ttu-id="db770-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db770-119">OUTPUTS</span></span>

## <span data-ttu-id="db770-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="db770-120">NOTES</span></span>

## <span data-ttu-id="db770-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db770-121">RELATED LINKS</span></span>

[<span data-ttu-id="db770-122">Get-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db770-122">Get-AzureVirtualNetworkGateway</span></span>](./Get-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="db770-123">Neu – AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db770-123">New-AzureVirtualNetworkGateway</span></span>](./New-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="db770-124">Remove-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db770-124">Remove-AzureVirtualNetworkGateway</span></span>](./Remove-AzureVirtualNetworkGateway.md)

[<span data-ttu-id="db770-125">Reset-AzureVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db770-125">Reset-AzureVirtualNetworkGateway</span></span>](./Reset-AzureVirtualNetworkGateway.md)


