---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 09642B94-E888-4A22-9E8E-62109DB9394E
online version: ''
schema: 2.0.0
ms.openlocfilehash: f42a788f29f8546e6f402f1685f4c91aa3d7e5cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006295"
---
# <span data-ttu-id="9d52d-101">Reset-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9d52d-101">Reset-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="9d52d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d52d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d52d-103">Setzt eine virtuelle Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="9d52d-103">Resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="9d52d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d52d-104">SYNTAX</span></span>

```
Reset-AzureVirtualNetworkGatewayConnection -GatewayId <String> -ConnectedEntityId <String>
 -RoutingWeight <Int32> [-SharedKey <String>] [-EnableBgp <Boolean>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d52d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d52d-105">DESCRIPTION</span></span>
<span data-ttu-id="9d52d-106">Das Cmdlet **Reset-AzureVirtualNetworkGatewayConnection** setzt eine virtuelle Netzwerkgateway-Verbindung zurück.</span><span class="sxs-lookup"><span data-stu-id="9d52d-106">The **Reset-AzureVirtualNetworkGatewayConnection** cmdlet resets a virtual network gateway connection.</span></span>

## <span data-ttu-id="9d52d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d52d-107">EXAMPLES</span></span>

## <span data-ttu-id="9d52d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d52d-108">PARAMETERS</span></span>

### <span data-ttu-id="9d52d-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="9d52d-109">-ConnectedEntityId</span></span>
<span data-ttu-id="9d52d-110">Gibt die ID einer verbundenen Entität an.</span><span class="sxs-lookup"><span data-stu-id="9d52d-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="9d52d-111">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="9d52d-111">-EnableBgp</span></span>
<span data-ttu-id="9d52d-112">Aktiviert das Border Gateway Protocol (BGP).</span><span class="sxs-lookup"><span data-stu-id="9d52d-112">Enables Border Gateway Protocol (BGP).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d52d-113">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="9d52d-113">-GatewayId</span></span>
<span data-ttu-id="9d52d-114">Gibt die ID eines Gateways an.</span><span class="sxs-lookup"><span data-stu-id="9d52d-114">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="9d52d-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d52d-115">-Profile</span></span>
<span data-ttu-id="9d52d-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9d52d-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9d52d-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9d52d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d52d-118">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="9d52d-118">-RoutingWeight</span></span>
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

### <span data-ttu-id="9d52d-119">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="9d52d-119">-SharedKey</span></span>
<span data-ttu-id="9d52d-120">Gibt einen freigegebenen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="9d52d-120">Specifies a shared key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d52d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d52d-121">CommonParameters</span></span>
<span data-ttu-id="9d52d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d52d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d52d-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d52d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d52d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d52d-124">INPUTS</span></span>

## <span data-ttu-id="9d52d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d52d-125">OUTPUTS</span></span>

## <span data-ttu-id="9d52d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d52d-126">NOTES</span></span>

## <span data-ttu-id="9d52d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d52d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9d52d-128">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9d52d-128">Get-AzureVirtualNetworkGatewayConnection</span></span>](./Get-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9d52d-129">Neu – AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9d52d-129">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="9d52d-130">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="9d52d-130">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)


