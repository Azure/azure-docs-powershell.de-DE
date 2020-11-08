---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4F1E69B8-15FB-495F-B910-04E450D3215F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a5b53f909b840a761d40f79a311fb61b7e2337b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006294"
---
# <span data-ttu-id="e2aad-101">Reset-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2aad-101">Reset-AzureVirtualNetworkGatewayKey</span></span>

## <span data-ttu-id="e2aad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2aad-102">SYNOPSIS</span></span>
<span data-ttu-id="e2aad-103">Setzt einen virtuellen Netzwerk-Gateway-Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="e2aad-103">Resets a virtual network gateway key.</span></span>

## <span data-ttu-id="e2aad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2aad-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayKey -GatewayId <String> -ConnectedEntityId <String> -keyLength <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2aad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2aad-105">DESCRIPTION</span></span>
<span data-ttu-id="e2aad-106">Das Cmdlet **Reset-AzureVirtualNetworkGatewayKey** setzt einen virtuellen Netzwerk-Gateway-Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="e2aad-106">The **Reset-AzureVirtualNetworkGatewayKey** cmdlet resets a virtual network gateway key.</span></span>

## <span data-ttu-id="e2aad-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2aad-107">EXAMPLES</span></span>

## <span data-ttu-id="e2aad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2aad-108">PARAMETERS</span></span>

### <span data-ttu-id="e2aad-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="e2aad-109">-ConnectedEntityId</span></span>
<span data-ttu-id="e2aad-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="e2aad-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="e2aad-111">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="e2aad-111">-GatewayId</span></span>
<span data-ttu-id="e2aad-112">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="e2aad-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="e2aad-113">-keylength</span><span class="sxs-lookup"><span data-stu-id="e2aad-113">-keyLength</span></span>
<span data-ttu-id="e2aad-114">Gibt die Schlüssellänge an.</span><span class="sxs-lookup"><span data-stu-id="e2aad-114">Specifies the key length.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2aad-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2aad-115">-Profile</span></span>
<span data-ttu-id="e2aad-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e2aad-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2aad-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e2aad-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2aad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2aad-118">CommonParameters</span></span>
<span data-ttu-id="e2aad-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2aad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2aad-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2aad-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2aad-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2aad-121">INPUTS</span></span>

## <span data-ttu-id="e2aad-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2aad-122">OUTPUTS</span></span>

## <span data-ttu-id="e2aad-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2aad-123">NOTES</span></span>

## <span data-ttu-id="e2aad-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2aad-124">RELATED LINKS</span></span>

[<span data-ttu-id="e2aad-125">Get-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2aad-125">Get-AzureVirtualNetworkGatewayKey</span></span>](./Get-AzureVirtualNetworkGatewayKey.md)

[<span data-ttu-id="e2aad-126">Satz-AzureVirtualNetworkGatewayKey</span><span class="sxs-lookup"><span data-stu-id="e2aad-126">Set-AzureVirtualNetworkGatewayKey</span></span>](./Set-AzureVirtualNetworkGatewayKey.md)
