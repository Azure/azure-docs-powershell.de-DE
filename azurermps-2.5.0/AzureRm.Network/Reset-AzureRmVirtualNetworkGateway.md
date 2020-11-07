---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: f4039fb8a616a474a858728b6e222537c2d75c66
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850607"
---
# <span data-ttu-id="8a520-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="8a520-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a520-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a520-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a520-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a520-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a520-104">DESCRIPTION</span></span>

## <span data-ttu-id="8a520-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a520-105">EXAMPLES</span></span>

### <span data-ttu-id="8a520-106">1:</span><span class="sxs-lookup"><span data-stu-id="8a520-106">1:</span></span>
```

```

## <span data-ttu-id="8a520-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a520-107">PARAMETERS</span></span>

### <span data-ttu-id="8a520-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a520-108">-AsJob</span></span>
<span data-ttu-id="8a520-109">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8a520-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a520-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a520-110">-DefaultProfile</span></span>
<span data-ttu-id="8a520-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a520-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a520-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="8a520-112">-GatewayVip</span></span>
<span data-ttu-id="8a520-113">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8a520-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="8a520-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="8a520-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a520-115">CommonParameters</span></span>
<span data-ttu-id="8a520-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a520-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a520-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a520-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a520-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a520-118">INPUTS</span></span>

### <span data-ttu-id="8a520-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8a520-119">String</span></span>
<span data-ttu-id="8a520-120">Der Parameter "GatewayVip" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a520-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8a520-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8a520-122">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a520-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8a520-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a520-123">OUTPUTS</span></span>

### <span data-ttu-id="8a520-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8a520-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a520-125">NOTES</span></span>

## <span data-ttu-id="8a520-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a520-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a520-127">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-127">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8a520-128">Neu – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-128">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8a520-129">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-129">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8a520-130">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-130">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8a520-131">Satz-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8a520-131">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


