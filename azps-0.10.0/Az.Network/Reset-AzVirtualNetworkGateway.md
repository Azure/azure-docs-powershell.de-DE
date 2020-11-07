---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843728"
---
# <span data-ttu-id="921c5-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="921c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="921c5-102">SYNOPSIS</span></span>

## <span data-ttu-id="921c5-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="921c5-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="921c5-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="921c5-104">DESCRIPTION</span></span>

## <span data-ttu-id="921c5-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="921c5-105">EXAMPLES</span></span>

### <span data-ttu-id="921c5-106">1:</span><span class="sxs-lookup"><span data-stu-id="921c5-106">1:</span></span>
```

```

## <span data-ttu-id="921c5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="921c5-107">PARAMETERS</span></span>

### <span data-ttu-id="921c5-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="921c5-108">-AsJob</span></span>
<span data-ttu-id="921c5-109">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="921c5-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="921c5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921c5-110">-DefaultProfile</span></span>
<span data-ttu-id="921c5-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="921c5-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="921c5-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="921c5-112">-GatewayVip</span></span>
<span data-ttu-id="921c5-113">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="921c5-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921c5-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-114">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921c5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921c5-115">CommonParameters</span></span>
<span data-ttu-id="921c5-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921c5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921c5-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="921c5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921c5-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="921c5-118">INPUTS</span></span>

### <span data-ttu-id="921c5-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="921c5-119">String</span></span>
<span data-ttu-id="921c5-120">Der Parameter "GatewayVip" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="921c5-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="921c5-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="921c5-122">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="921c5-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="921c5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="921c5-123">OUTPUTS</span></span>

### <span data-ttu-id="921c5-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="921c5-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="921c5-125">NOTES</span></span>

## <span data-ttu-id="921c5-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="921c5-126">RELATED LINKS</span></span>

[<span data-ttu-id="921c5-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="921c5-128">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="921c5-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="921c5-130">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="921c5-131">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="921c5-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


