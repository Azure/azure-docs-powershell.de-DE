---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f01fd5c1c6694c8d16ab34e6aad9f6a52463c726
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850316"
---
# <span data-ttu-id="0fe1d-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="0fe1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0fe1d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe1d-103">Ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="0fe1d-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fe1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fe1d-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fe1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fe1d-105">DESCRIPTION</span></span>
<span data-ttu-id="0fe1d-106">Das Cmdlet " **Satz-AzureRmLocalNetworkGateway** " ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="0fe1d-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="0fe1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fe1d-107">EXAMPLES</span></span>

### <span data-ttu-id="0fe1d-108">1:</span><span class="sxs-lookup"><span data-stu-id="0fe1d-108">1:</span></span>
```

```

## <span data-ttu-id="0fe1d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fe1d-109">PARAMETERS</span></span>

### <span data-ttu-id="0fe1d-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0fe1d-110">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fe1d-111">-AsJob</span></span>
<span data-ttu-id="0fe1d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0fe1d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="0fe1d-113">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="0fe1d-114">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe1d-115">-DefaultProfile</span></span>
<span data-ttu-id="0fe1d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0fe1d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fe1d-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="0fe1d-118">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe1d-119">CommonParameters</span></span>
<span data-ttu-id="0fe1d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fe1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe1d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe1d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe1d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0fe1d-122">INPUTS</span></span>

### <span data-ttu-id="0fe1d-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="0fe1d-124">Der Parameter "LocalNetworkGateway" akzeptiert den Wert vom Typ "PSLocalNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0fe1d-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="0fe1d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0fe1d-125">OUTPUTS</span></span>

### <span data-ttu-id="0fe1d-126">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="0fe1d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0fe1d-127">NOTES</span></span>

## <span data-ttu-id="0fe1d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0fe1d-128">RELATED LINKS</span></span>

[<span data-ttu-id="0fe1d-129">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-129">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0fe1d-130">Neu – AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-130">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="0fe1d-131">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0fe1d-131">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


