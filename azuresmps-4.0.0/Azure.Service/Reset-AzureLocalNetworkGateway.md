---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0E4D44EE-BF28-46FE-B2FA-D35C1651016F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3940a5e6fc69ebee02f3e0de963bc87f790f8860
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005678"
---
# <span data-ttu-id="68dc7-101">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="68dc7-101">Reset-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="68dc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="68dc7-103">Setzt ein lokales Netzwerkgateway zurück.</span><span class="sxs-lookup"><span data-stu-id="68dc7-103">Resets a local network gateway.</span></span>

## <span data-ttu-id="68dc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68dc7-104">SYNTAX</span></span>

```
Reset-AzureLocalNetworkGateway -GatewayId <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68dc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="68dc7-106">Das Cmdlet **Reset-AzureLocalNetworkGateway** setzt ein lokales Netzwerkgateway zurück.</span><span class="sxs-lookup"><span data-stu-id="68dc7-106">The **Reset-AzureLocalNetworkGateway** cmdlet resets a local network gateway.</span></span>

## <span data-ttu-id="68dc7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68dc7-107">EXAMPLES</span></span>

## <span data-ttu-id="68dc7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68dc7-108">PARAMETERS</span></span>

### <span data-ttu-id="68dc7-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="68dc7-109">-AddressSpace</span></span>
<span data-ttu-id="68dc7-110">Gibt den Adressraum an.</span><span class="sxs-lookup"><span data-stu-id="68dc7-110">Specifies the address space.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68dc7-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="68dc7-111">-Asn</span></span>
<span data-ttu-id="68dc7-112">Gibt die autonome Systemnummer an (ASN).</span><span class="sxs-lookup"><span data-stu-id="68dc7-112">Specifies the autonomous system number (ASN).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68dc7-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="68dc7-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="68dc7-114">Gibt die Peering-Adresse des Border Gateway Protocol (BGP) an.</span><span class="sxs-lookup"><span data-stu-id="68dc7-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="68dc7-115">-Gatewayserver</span><span class="sxs-lookup"><span data-stu-id="68dc7-115">-GatewayId</span></span>
<span data-ttu-id="68dc7-116">Gibt die ID des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="68dc7-116">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="68dc7-117">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="68dc7-117">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68dc7-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="68dc7-118">-Profile</span></span>
<span data-ttu-id="68dc7-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="68dc7-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="68dc7-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="68dc7-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="68dc7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dc7-121">CommonParameters</span></span>
<span data-ttu-id="68dc7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68dc7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dc7-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68dc7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dc7-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68dc7-124">INPUTS</span></span>

## <span data-ttu-id="68dc7-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68dc7-125">OUTPUTS</span></span>

## <span data-ttu-id="68dc7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="68dc7-126">NOTES</span></span>

## <span data-ttu-id="68dc7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68dc7-127">RELATED LINKS</span></span>

[<span data-ttu-id="68dc7-128">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="68dc7-128">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="68dc7-129">Neu – AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="68dc7-129">New-AzureLocalNetworkGateway</span></span>](./New-AzureLocalNetworkGateway.md)

[<span data-ttu-id="68dc7-130">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="68dc7-130">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)


