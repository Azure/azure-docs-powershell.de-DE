---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: cdea7cba3dea72df80b8571198bb50d5e337b14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146625"
---
# <span data-ttu-id="7e6f6-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="7e6f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6f6-103">Setzt das skalierbare P2S-VPN-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="7e6f6-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="7e6f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e6f6-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e6f6-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e6f6-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e6f6-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7e6f6-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e6f6-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7e6f6-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e6f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e6f6-108">DESCRIPTION</span></span>
<span data-ttu-id="7e6f6-109">Setzt das P2SVpnGateway zurück.</span><span class="sxs-lookup"><span data-stu-id="7e6f6-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="7e6f6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e6f6-110">EXAMPLES</span></span>

### <span data-ttu-id="7e6f6-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="7e6f6-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="7e6f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e6f6-112">PARAMETERS</span></span>

### <span data-ttu-id="7e6f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e6f6-113">-AsJob</span></span>
<span data-ttu-id="7e6f6-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7e6f6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e6f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6f6-115">-DefaultProfile</span></span>
<span data-ttu-id="7e6f6-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e6f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e6f6-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-117">-P2SVpnGateway</span></span>
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

### <span data-ttu-id="7e6f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6f6-118">CommonParameters</span></span>
<span data-ttu-id="7e6f6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6f6-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6f6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6f6-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e6f6-121">INPUTS</span></span>

### <span data-ttu-id="7e6f6-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="7e6f6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7e6f6-123">System.String</span></span>

## <span data-ttu-id="7e6f6-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e6f6-124">OUTPUTS</span></span>

### <span data-ttu-id="7e6f6-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="7e6f6-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7e6f6-126">NOTES</span></span>

## <span data-ttu-id="7e6f6-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7e6f6-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e6f6-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="7e6f6-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="7e6f6-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="7e6f6-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7e6f6-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
