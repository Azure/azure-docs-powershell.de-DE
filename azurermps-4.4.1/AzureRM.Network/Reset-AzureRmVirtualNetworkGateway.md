---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 2b2947ec86e928506624aea49b380db3c4f24bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664473"
---
# <span data-ttu-id="73af8-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="73af8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73af8-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73af8-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="73af8-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73af8-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73af8-104">DESCRIPTION</span></span>

## <span data-ttu-id="73af8-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73af8-105">EXAMPLES</span></span>

## <span data-ttu-id="73af8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73af8-106">PARAMETERS</span></span>

### <span data-ttu-id="73af8-107">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="73af8-107">-GatewayVip</span></span>
<span data-ttu-id="73af8-108">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="73af8-108">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73af8-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73af8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73af8-110">-DefaultProfile</span></span>
<span data-ttu-id="73af8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73af8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73af8-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73af8-112">CommonParameters</span></span>
<span data-ttu-id="73af8-113">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73af8-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73af8-114">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73af8-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73af8-115">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73af8-115">INPUTS</span></span>

### <span data-ttu-id="73af8-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73af8-116">String</span></span>
<span data-ttu-id="73af8-117">Der Parameter "GatewayVip" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="73af8-117">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="73af8-118">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-118">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="73af8-119">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="73af8-119">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="73af8-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73af8-120">OUTPUTS</span></span>

### <span data-ttu-id="73af8-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="73af8-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="73af8-122">NOTES</span></span>

## <span data-ttu-id="73af8-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73af8-123">RELATED LINKS</span></span>

[<span data-ttu-id="73af8-124">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-124">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="73af8-125">Neu – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-125">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="73af8-126">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-126">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="73af8-127">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-127">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="73af8-128">Satz-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="73af8-128">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


