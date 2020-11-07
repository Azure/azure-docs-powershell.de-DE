---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 815f7d3fdc0f058f2abfce5687b129054814adab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664630"
---
# <span data-ttu-id="57246-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="57246-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57246-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57246-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="57246-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57246-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57246-104">DESCRIPTION</span></span>

## <span data-ttu-id="57246-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57246-105">EXAMPLES</span></span>

## <span data-ttu-id="57246-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57246-106">PARAMETERS</span></span>

### <span data-ttu-id="57246-107">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57246-107">-AsJob</span></span>
<span data-ttu-id="57246-108">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="57246-108">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57246-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57246-109">-DefaultProfile</span></span>
<span data-ttu-id="57246-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57246-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57246-111">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="57246-111">-GatewayVip</span></span>
<span data-ttu-id="57246-112">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="57246-112">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="57246-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="57246-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57246-114">CommonParameters</span></span>
<span data-ttu-id="57246-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57246-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57246-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57246-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57246-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57246-117">INPUTS</span></span>

### <span data-ttu-id="57246-118">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="57246-118">String</span></span>
<span data-ttu-id="57246-119">Der Parameter "GatewayVip" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="57246-119">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="57246-120">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-120">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="57246-121">Der Parameter "VirtualNetworkGateway" akzeptiert den Wert vom Typ "PSVirtualNetworkGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="57246-121">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="57246-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57246-122">OUTPUTS</span></span>

### <span data-ttu-id="57246-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="57246-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="57246-124">NOTES</span></span>

## <span data-ttu-id="57246-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57246-125">RELATED LINKS</span></span>

[<span data-ttu-id="57246-126">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-126">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57246-127">Neu – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-127">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57246-128">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-128">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57246-129">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-129">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="57246-130">Satz-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="57246-130">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


