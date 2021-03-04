---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932379"
---
# <span data-ttu-id="67239-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="67239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67239-102">SYNOPSIS</span></span>
<span data-ttu-id="67239-103">Setzt das skalierbare VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="67239-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="67239-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67239-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67239-105">ByVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="67239-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67239-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="67239-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67239-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="67239-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67239-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67239-108">DESCRIPTION</span></span>
<span data-ttu-id="67239-109">Setzt das VpnGateway zurück.</span><span class="sxs-lookup"><span data-stu-id="67239-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="67239-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="67239-110">EXAMPLES</span></span>

### <span data-ttu-id="67239-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="67239-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="67239-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="67239-112">PARAMETERS</span></span>

### <span data-ttu-id="67239-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67239-113">-AsJob</span></span>
<span data-ttu-id="67239-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="67239-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67239-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67239-115">-DefaultProfile</span></span>
<span data-ttu-id="67239-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67239-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67239-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-117">-VpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67239-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67239-118">CommonParameters</span></span>
<span data-ttu-id="67239-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67239-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67239-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67239-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67239-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="67239-121">INPUTS</span></span>

### <span data-ttu-id="67239-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="67239-123">System.String</span><span class="sxs-lookup"><span data-stu-id="67239-123">System.String</span></span>

## <span data-ttu-id="67239-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="67239-124">OUTPUTS</span></span>

### <span data-ttu-id="67239-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="67239-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="67239-126">NOTES</span></span>

## <span data-ttu-id="67239-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="67239-127">RELATED LINKS</span></span>

[<span data-ttu-id="67239-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="67239-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="67239-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="67239-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="67239-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
