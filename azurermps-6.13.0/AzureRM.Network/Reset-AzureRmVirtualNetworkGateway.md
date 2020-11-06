---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: c5d77619fa5f89c60ce20a097e096709e9a48bae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503486"
---
# <span data-ttu-id="2701c-101">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-101">Reset-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="2701c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2701c-102">SYNOPSIS</span></span>
<span data-ttu-id="2701c-103">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="2701c-103">Resets the Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2701c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2701c-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2701c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2701c-105">DESCRIPTION</span></span>
<span data-ttu-id="2701c-106">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="2701c-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="2701c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2701c-107">EXAMPLES</span></span>

### <span data-ttu-id="2701c-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2701c-108">Example 1:</span></span>
```
$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="2701c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2701c-109">PARAMETERS</span></span>

### <span data-ttu-id="2701c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2701c-110">-AsJob</span></span>
<span data-ttu-id="2701c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2701c-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2701c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2701c-112">-DefaultProfile</span></span>
<span data-ttu-id="2701c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2701c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2701c-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="2701c-114">-GatewayVip</span></span>
<span data-ttu-id="2701c-115">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2701c-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="2701c-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="2701c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2701c-117">CommonParameters</span></span>
<span data-ttu-id="2701c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2701c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2701c-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2701c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2701c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2701c-120">INPUTS</span></span>

### <span data-ttu-id="2701c-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="2701c-122">Parameter: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2701c-122">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="2701c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2701c-123">System.String</span></span>
<span data-ttu-id="2701c-124">Parameter: GatewayVip (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2701c-124">Parameters: GatewayVip (ByValue)</span></span>

## <span data-ttu-id="2701c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2701c-125">OUTPUTS</span></span>

### <span data-ttu-id="2701c-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2701c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2701c-127">NOTES</span></span>

## <span data-ttu-id="2701c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2701c-128">RELATED LINKS</span></span>

[<span data-ttu-id="2701c-129">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-129">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2701c-130">Neu – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-130">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2701c-131">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-131">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2701c-132">Größe ändern – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-132">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2701c-133">Satz-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2701c-133">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)


