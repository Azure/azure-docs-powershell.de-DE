---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 59f4a96c324a9743c876cf987e1347bbe0c8d946
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660286"
---
# <span data-ttu-id="09a0e-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="09a0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="09a0e-103">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="09a0e-103">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="09a0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09a0e-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09a0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="09a0e-106">Zurücksetzen des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="09a0e-106">Resets the Virtual Network Gateway</span></span>

## <span data-ttu-id="09a0e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09a0e-107">EXAMPLES</span></span>

### <span data-ttu-id="09a0e-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="09a0e-108">Example 1:</span></span>
```
$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway
```

## <span data-ttu-id="09a0e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="09a0e-109">PARAMETERS</span></span>

### <span data-ttu-id="09a0e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09a0e-110">-AsJob</span></span>
<span data-ttu-id="09a0e-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="09a0e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09a0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a0e-112">-DefaultProfile</span></span>
<span data-ttu-id="09a0e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09a0e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09a0e-114">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="09a0e-114">-GatewayVip</span></span>
<span data-ttu-id="09a0e-115">Das Gateway-VIP-Objekt, um bestimmte Gateway-Instanzen zurückzusetzen (beispielsweise bei Active-Active aktivierten Gateways) Standardmäßig wird die primäre Gateway-Instanz zurückgesetzt, wenn kein Wert übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="09a0e-115">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

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

### <span data-ttu-id="09a0e-116">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-116">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="09a0e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a0e-117">CommonParameters</span></span>
<span data-ttu-id="09a0e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a0e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a0e-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a0e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a0e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09a0e-120">INPUTS</span></span>

### <span data-ttu-id="09a0e-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="09a0e-122">System. String</span><span class="sxs-lookup"><span data-stu-id="09a0e-122">System.String</span></span>

## <span data-ttu-id="09a0e-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09a0e-123">OUTPUTS</span></span>

### <span data-ttu-id="09a0e-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="09a0e-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="09a0e-125">NOTES</span></span>

## <span data-ttu-id="09a0e-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09a0e-126">RELATED LINKS</span></span>

[<span data-ttu-id="09a0e-127">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a0e-128">Neu – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a0e-129">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a0e-130">Größe ändern – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="09a0e-131">Satz-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="09a0e-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
