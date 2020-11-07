---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843620"
---
# <span data-ttu-id="4a4dc-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="4a4dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4dc-103">Ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="4a4dc-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="4a4dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4dc-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a4dc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="4a4dc-106">Das Cmdlet " **Satz-AzLocalNetworkGateway** " ändert ein lokales Netzwerkgateway.</span><span class="sxs-lookup"><span data-stu-id="4a4dc-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="4a4dc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="4a4dc-108">1:</span><span class="sxs-lookup"><span data-stu-id="4a4dc-108">1:</span></span>
```

```

## <span data-ttu-id="4a4dc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a4dc-109">PARAMETERS</span></span>

### <span data-ttu-id="4a4dc-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4a4dc-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="4a4dc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a4dc-111">-AsJob</span></span>
<span data-ttu-id="4a4dc-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4a4dc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a4dc-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="4a4dc-113">-Asn</span></span>
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

### <span data-ttu-id="4a4dc-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="4a4dc-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="4a4dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4dc-115">-DefaultProfile</span></span>
<span data-ttu-id="4a4dc-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a4dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4dc-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-117">-LocalNetworkGateway</span></span>
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

### <span data-ttu-id="4a4dc-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="4a4dc-118">-PeerWeight</span></span>
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

### <span data-ttu-id="4a4dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4dc-119">CommonParameters</span></span>
<span data-ttu-id="4a4dc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4dc-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4dc-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4dc-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a4dc-122">INPUTS</span></span>

### <span data-ttu-id="4a4dc-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="4a4dc-124">Der Parameter "LocalNetworkGateway" akzeptiert den Wert vom Typ "PSLocalNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a4dc-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="4a4dc-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a4dc-125">OUTPUTS</span></span>

### <span data-ttu-id="4a4dc-126">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="4a4dc-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a4dc-127">NOTES</span></span>

## <span data-ttu-id="4a4dc-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a4dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="4a4dc-129">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="4a4dc-130">Neu – AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="4a4dc-131">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a4dc-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)


