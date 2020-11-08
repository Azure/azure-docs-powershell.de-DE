---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 15f918214a71fe38c850126b31f93d14940fa602
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004141"
---
# <span data-ttu-id="6c59b-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6c59b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c59b-102">SYNOPSIS</span></span>
<span data-ttu-id="6c59b-103">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="6c59b-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="6c59b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c59b-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c59b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c59b-105">DESCRIPTION</span></span>
<span data-ttu-id="6c59b-106">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="6c59b-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="6c59b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c59b-107">EXAMPLES</span></span>

### <span data-ttu-id="6c59b-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="6c59b-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="6c59b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c59b-109">PARAMETERS</span></span>

### <span data-ttu-id="6c59b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c59b-110">-AsJob</span></span>
<span data-ttu-id="6c59b-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6c59b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c59b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c59b-112">-DefaultProfile</span></span>
<span data-ttu-id="6c59b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c59b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c59b-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="6c59b-114">-GatewayVip</span></span>
<span data-ttu-id="6c59b-115">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c59b-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="6c59b-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="6c59b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c59b-117">CommonParameters</span></span>
<span data-ttu-id="6c59b-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c59b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c59b-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c59b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c59b-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c59b-120">INPUTS</span></span>

### <span data-ttu-id="6c59b-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6c59b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6c59b-122">System.String</span></span>

## <span data-ttu-id="6c59b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c59b-123">OUTPUTS</span></span>

### <span data-ttu-id="6c59b-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="6c59b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c59b-125">NOTES</span></span>

## <span data-ttu-id="6c59b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c59b-126">RELATED LINKS</span></span>

[<span data-ttu-id="6c59b-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6c59b-128">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6c59b-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6c59b-130">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="6c59b-131">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6c59b-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
