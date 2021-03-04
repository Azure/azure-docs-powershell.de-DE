---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: c813f5d5921f0291174a77cf6cdc4b0a1f7ee6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921696"
---
# <span data-ttu-id="4bd4d-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="4bd4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd4d-103">Setzt das skalierbare P2S-VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="4bd4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bd4d-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd4d-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4bd4d-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bd4d-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4bd4d-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bd4d-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd4d-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd4d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bd4d-108">DESCRIPTION</span></span>
<span data-ttu-id="4bd4d-109">Setzt das P2SVpnGateway zurück.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="4bd4d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bd4d-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd4d-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="4bd4d-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="4bd4d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bd4d-112">PARAMETERS</span></span>

### <span data-ttu-id="4bd4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bd4d-113">-AsJob</span></span>
<span data-ttu-id="4bd4d-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4bd4d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bd4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd4d-115">-DefaultProfile</span></span>
<span data-ttu-id="4bd4d-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd4d-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="4bd4d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd4d-118">CommonParameters</span></span>
<span data-ttu-id="4bd4d-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd4d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd4d-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd4d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd4d-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bd4d-121">INPUTS</span></span>

### <span data-ttu-id="4bd4d-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="4bd4d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4bd4d-123">System.String</span></span>

## <span data-ttu-id="4bd4d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bd4d-124">OUTPUTS</span></span>

### <span data-ttu-id="4bd4d-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="4bd4d-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bd4d-126">NOTES</span></span>

## <span data-ttu-id="4bd4d-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bd4d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4bd4d-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="4bd4d-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="4bd4d-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="4bd4d-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4d-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
