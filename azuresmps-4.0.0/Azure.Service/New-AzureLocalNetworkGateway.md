---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9F9E4639-A557-4BD8-88C2-894F6C848C4A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa54a7bd236bb561b3de4b9c2a3c0a2710deb61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006213"
---
# <span data-ttu-id="87976-101">New-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87976-101">New-AzureLocalNetworkGateway</span></span>

## <span data-ttu-id="87976-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87976-102">SYNOPSIS</span></span>
<span data-ttu-id="87976-103">erstellt ein Azure-lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="87976-103">creates an Azure local network gateway.</span></span>

## <span data-ttu-id="87976-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87976-104">SYNTAX</span></span>

```
New-AzureLocalNetworkGateway -GatewayName <String> -IpAddress <String>
 -AddressSpace <System.Collections.Generic.List`1[System.String]> [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87976-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87976-105">DESCRIPTION</span></span>
<span data-ttu-id="87976-106">Mit dem Cmdlet **New-AzureLocalNetworkGateway** wird ein lokales Azure-Netzwerkgateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="87976-106">The **New-AzureLocalNetworkGateway** cmdlet creates an Azure local network gateway.</span></span>

## <span data-ttu-id="87976-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87976-107">EXAMPLES</span></span>

## <span data-ttu-id="87976-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="87976-108">PARAMETERS</span></span>

### <span data-ttu-id="87976-109">-AddressSpace</span><span class="sxs-lookup"><span data-stu-id="87976-109">-AddressSpace</span></span>
<span data-ttu-id="87976-110">Gibt den Adressraum an.</span><span class="sxs-lookup"><span data-stu-id="87976-110">Specifies the address space.</span></span>

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

### <span data-ttu-id="87976-111">-ASN</span><span class="sxs-lookup"><span data-stu-id="87976-111">-Asn</span></span>
<span data-ttu-id="87976-112">Gibt die autonome Systemnummer an (ASN).</span><span class="sxs-lookup"><span data-stu-id="87976-112">Specifies the autonomous system number (ASN).</span></span>

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

### <span data-ttu-id="87976-113">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="87976-113">-BgpPeeringAddress</span></span>
<span data-ttu-id="87976-114">Gibt die Peering-Adresse des Border Gateway Protocol (BGP) an.</span><span class="sxs-lookup"><span data-stu-id="87976-114">Specifies the Border Gateway Protocol (BGP) peering address.</span></span>

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

### <span data-ttu-id="87976-115">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="87976-115">-GatewayName</span></span>
<span data-ttu-id="87976-116">Gibt den Namen des Gateways an.</span><span class="sxs-lookup"><span data-stu-id="87976-116">Specifies the name of the gateway.</span></span>

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

### <span data-ttu-id="87976-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="87976-117">-IpAddress</span></span>
<span data-ttu-id="87976-118">Gibt die IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="87976-118">Specifies the IP address.</span></span>

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

### <span data-ttu-id="87976-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="87976-119">-PeerWeight</span></span>
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

### <span data-ttu-id="87976-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="87976-120">-Profile</span></span>
<span data-ttu-id="87976-121">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="87976-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="87976-122">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="87976-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87976-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87976-123">CommonParameters</span></span>
<span data-ttu-id="87976-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87976-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87976-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87976-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87976-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87976-126">INPUTS</span></span>

## <span data-ttu-id="87976-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87976-127">OUTPUTS</span></span>

## <span data-ttu-id="87976-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="87976-128">NOTES</span></span>

## <span data-ttu-id="87976-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87976-129">RELATED LINKS</span></span>

[<span data-ttu-id="87976-130">Get-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87976-130">Get-AzureLocalNetworkGateway</span></span>](./Get-AzureLocalNetworkGateway.md)

[<span data-ttu-id="87976-131">Remove-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87976-131">Remove-AzureLocalNetworkGateway</span></span>](./Remove-AzureLocalNetworkGateway.md)

[<span data-ttu-id="87976-132">Reset-AzureLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="87976-132">Reset-AzureLocalNetworkGateway</span></span>](./Reset-AzureLocalNetworkGateway.md)


